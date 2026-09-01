# AI-to-Agent-Agency-zh-TW

> **繁體中文（zh-TW）版 AI 專家 Agent 角色庫** — 精選自開源專案
> [The Agency (`agency-agents`)](https://github.com/msitarzewski/agency-agents)，
> 逐檔重新翻譯為台灣用語、可直接 drop-in 到 Claude Code / Cursor / Copilot 等工具的
> `agents/` 目錄。

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![上游](https://img.shields.io/badge/upstream-msitarzewski%2Fagency--agents-blue)](https://github.com/msitarzewski/agency-agents)
[![語言](https://img.shields.io/badge/lang-zh--TW%20%E7%B9%81%E9%AB%94%E4%B8%AD%E6%96%87-brightgreen)](#)

---

## 🙏 致謝原創作者與原版

本專案**不是原創**。所有 Agent 的角色設定、專業流程與方法論，皆來自：

- **原始專案**：[The Agency — `agency-agents`](https://github.com/msitarzewski/agency-agents)
- **原始作者**：Michael Sitarzewski（[@msitarzewski](https://github.com/msitarzewski)）與 AgentLand Contributors
- **原始授權**：MIT License

本專案所做的事，只有三件：

1. **篩選** — 從上游約 270 個 Agent 中，精選與「AI to Agent」教學最相關的一小組。
2. **翻譯** — 從**英文上游**逐檔重新翻譯為**繁體中文（台灣用語）**，而非簡體轉繁體。
3. **在地化** — 統一技術術語（見 [`docs/術語對照表.md`](docs/術語對照表.md)），保留程式碼、路徑、
   CLI 名稱與通用英文技術縮寫（RAG、LLM、API、OAuth、CI/CD 等）不譯。

我們也感謝簡體中文社群版 [`jnMetaCode/agency-agents-zh`](https://github.com/jnMetaCode/agency-agents-zh)
在先——它的存在讓我們確認「繁體 + 教學導向」仍是一塊值得補的空白。

逐檔對應（哪個檔案來自上游哪個路徑、對應哪個快照）請見 [`ATTRIBUTION.md`](ATTRIBUTION.md)。

---

## 📦 這個 repo 是什麼、不是什麼

| 是 | 不是 |
|---|---|
| 純 Agent 定義檔（`.md`），frontmatter 結構與上游完全一致 | 不含課程、講義、練習題 |
| 可直接複製到 `~/.claude/agents/` 等目錄使用 | 不是桌面 App、不是 CLI 工具 |
| 精選 20–30 個、逐檔人工校對的繁體中文版 | 不是上游 270 個的全量翻譯 |
| 持續追上游更新（見 [`UPSTREAM.md`](UPSTREAM.md)） | 不保證與上游即時同步 |

搭配課程教材請見姊妹專案：
**[`ai-to-agent-agency-course-zh-TW`](https://github.com/draiagent/ai-to-agent-agency-course-zh-TW)**
（CC BY-SA 4.0，公開教學與課程教案）。

---

## 🗂️ 選錄清單（規劃中，逐一批次進行）

選錄標準：① 跨產業可教學 ② 對應到「AI → Agent」能力轉移的關鍵節點 ③ 一般團隊實際用得到。

| 模組 | Agent | 狀態 |
|---|---|---|
| 1 打地基：Agent 是什麼 | prompt-engineer、ai-engineer、multi-agent-systems-architect、rapid-prototyper | ⬜ 規劃 |
| 2 工程實作四人組 | **backend-architect** ✅、**frontend-developer** ✅、**code-reviewer** ✅、devops-automator、senior-developer | 🔄 進行中 |
| 3 產品與交付 | product-manager、sprint-prioritizer、design-ux-researcher、design-ui-designer | ⬜ 規劃 |
| 4 內容與成長 | marketing-content-creator、marketing-growth-hacker、marketing-ai-citation-strategist、marketing-linkedin-content-creator | ⬜ 規劃 |
| 5 品質・安全・治理 | security-engineer、test-writer、technical-writer、legal-contract-reviewer | ⬜ 規劃 |
| 6 選修：中國平台 | douyin-strategist、xiaohongshu 系列、wechat-official-account | ⬜ 規劃 |

> ✅ = 已完成並校對　🔄 = 進行中　⬜ = 尚未開始
> 目前完成度請以 [`CHANGELOG.md`](CHANGELOG.md) 為準。

---

## 🚀 安裝與使用

### Claude Code

```bash
git clone https://github.com/draiagent/AI-to-Agent-Agency-zh-TW.git
mkdir -p ~/.claude/agents
cp AI-to-Agent-Agency-zh-TW/agents/**/*.md ~/.claude/agents/
```

（PowerShell）

```powershell
git clone https://github.com/draiagent/AI-to-Agent-Agency-zh-TW.git
New-Item -ItemType Directory -Force ~/.claude/agents | Out-Null
Get-ChildItem AI-to-Agent-Agency-zh-TW/agents -Recurse -Filter *.md |
  Copy-Item -Destination ~/.claude/agents/
```

重新啟動 Claude Code 會話後，即可用 `/<agent-name>` 呼叫，或讓模型自動挑選。

### 其他工具

frontmatter 結構與上游一致，因此上游 [`agency-agents` 的 `scripts/install.sh`](https://github.com/msitarzewski/agency-agents/blob/main/scripts/install.sh)
也能用來安裝本 repo 的檔案（把本 repo 當作 repo 根目錄執行）。Cursor / Copilot / Gemini CLI 等
請參考上游說明。

---

## 🔄 與上游的關係與更新政策

- 本 repo **釘選**一個上游快照（commit / 日期），記錄於 [`UPSTREAM.md`](UPSTREAM.md)。
- 上游有實質更新時，**逐檔比對 diff** 後再決定是否同步，不自動 merge。
- 因為只維護 20–30 個檔案，同步成本可控；預計每季檢視一次。
- 若上游某 Agent 被移除或大改，本 repo 會在 `CHANGELOG.md` 註記並保留舊版一個週期。

---

## 📄 授權

MIT License。原始英文內容著作權歸 Michael Sitarzewski / AgentLand Contributors，
繁體中文翻譯與在地化著作權歸 dr.aiagent（draiagent）。完整條款見 [`LICENSE`](LICENSE)，
逐檔來源見 [`ATTRIBUTION.md`](ATTRIBUTION.md)。

使用本 repo 的 Agent 檔案時，請一併保留上述著作權與致謝資訊。
