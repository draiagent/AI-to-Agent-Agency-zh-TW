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
| 18 部門 × 約 40 位、逐檔人工校對的繁體中文版 | 不是上游 270 個的全量翻譯 |
| 持續追上游更新（見 [`UPSTREAM.md`](UPSTREAM.md)） | 不保證與上游即時同步 |

搭配課程教材請見姊妹專案：
**[`ai-to-agent-agency-course-zh-TW`](https://github.com/draiagent/ai-to-agent-agency-course-zh-TW)**
（CC BY-SA 4.0，公開教學與課程教案）。

---

## 🗂️ 選錄清單：18 個部門，約 40 位數位員工

把整套 Agency 想成一間公司：**部門（Domain）= 上游 division，數位員工（Sub-agent）= 具體專家角色**。
本 repo 從上游 18 個部門各挑 1–7 位代表性數位員工翻成繁體中文。

選錄標準：① 跨產業可教學 ② 對應到「AI → Agent」能力轉移的關鍵節點 ③ 一般團隊實際用得到。
**已排除**上游行銷部門下所有中國平台專屬角色（抖音／小紅書／微信／微博／B站／百度SEO／跨境電商等 13 個）。

| # | 部門 Domain | 數位員工 Sub-agents | 進度 |
|---|---|---|---|
| 1 | 工程 engineering | backend-architect ✅、frontend-developer ✅、code-reviewer ✅、devops-automator ✅、prompt-engineer ✅、ai-engineer ✅、multi-agent-systems-architect ✅ | **7 / 7 ✅** |
| 2 | 設計 design | ui-designer ✅、ux-researcher ✅ | **2 / 2 ✅** |
| 3 | 產品 product | product-manager ✅、sprint-prioritizer ✅ | **2 / 2 ✅** |
| 4 | 專案管理 project-management | project-manager-senior ✅、meeting-notes-specialist ✅ | **2 / 2 ✅** |
| 5 | 行銷 marketing | content-creator ✅、growth-hacker ✅、seo-specialist ✅、ai-citation-strategist ✅ | **4 / 4 ✅** |
| 6 | 銷售 sales | deal-strategist ✅、outbound-strategist ✅ | **2 / 2 ✅** |
| 7 | 財務 finance | financial-analyst ✅、bookkeeper-controller ✅ | **2 / 2 ✅** |
| 8 | 付費媒體 paid-media | ppc-strategist ✅、creative-strategist ✅ | **2 / 2 ✅** |
| 9 | 安全 security | appsec-engineer ✅、penetration-tester ✅ | **2 / 2 ✅** |
| 10 | 測試 testing | test-automation-engineer ✅、accessibility-auditor ✅ | **2 / 2 ✅** |
| 11 | 客戶支援 support | support-responder、analytics-reporter | ⬜ |
| 12 | 研究 research | synthesist | ⬜ |
| 13 | 學術 academic | psychologist、statistician | ⬜ |
| 14 | 醫療 healthcare | clinical-evidence-agent | ⬜ |
| 15 | 遊戲開發 game-development | game-designer、narrative-designer | ⬜ |
| 16 | GIS gis | analyst（垂直示範） | ⬜ |
| 17 | 空間運算 spatial-computing | xr-immersive-developer（垂直示範） | ⬜ |
| 18 | 跨域專業 specialized | business-strategist、mcp-builder | ⬜ |

> ✅ = 已完成並校對　⬜ = 尚未開始　　完成度以 [`CHANGELOG.md`](CHANGELOG.md) 為準。
> `agents/` 目錄依部門分子資料夾（沿用上游 division 名稱），可整包或分部門 drop-in。

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
- 因為只維護約 40 個檔案，同步成本可控；預計每季檢視一次。
- 若上游某 Agent 被移除或大改，本 repo 會在 `CHANGELOG.md` 註記並保留舊版一個週期。

---

## 📄 授權

MIT License。原始英文內容著作權歸 Michael Sitarzewski / AgentLand Contributors，
繁體中文翻譯與在地化著作權歸 dr.aiagent（draiagent）。完整條款見 [`LICENSE`](LICENSE)，
逐檔來源見 [`ATTRIBUTION.md`](ATTRIBUTION.md)。

使用本 repo 的 Agent 檔案時，請一併保留上述著作權與致謝資訊。
