# AI-to-Agent-Agency-zh-TW

**繁體中文（zh-TW）AI 專家 Agent 角色庫**

精選自開源專案 [The Agency（`agency-agents`）](https://github.com/msitarzewski/agency-agents)，
自英文上游逐檔重新翻譯為台灣用語，並因應在地教學需求原創擴充。
所有檔案可直接部署至 Claude Code、Cursor、GitHub Copilot 等工具的 `agents/` 目錄。

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Upstream](https://img.shields.io/badge/upstream-msitarzewski%2Fagency--agents-blue)](https://github.com/msitarzewski/agency-agents)
[![Language](https://img.shields.io/badge/lang-zh--TW%20%E7%B9%81%E9%AB%94%E4%B8%AD%E6%96%87-brightgreen)](#)
[![Agents](https://img.shields.io/badge/agents-46%20(41%2B5)-informational)](#選錄清單18-個部門46-位數位員工)

---

## 目錄

- [關於本專案](#關於本專案)
- [專案範圍](#專案範圍)
- [選錄清單：18 個部門，46 位數位員工](#選錄清單18-個部門46-位數位員工)
- [在地化與翻譯原則](#在地化與翻譯原則)
- [安裝與使用](#安裝與使用)
- [團隊配方（`rosters/`）](#團隊配方rosters)
- [與上游的關係與更新政策](#與上游的關係與更新政策)
- [致謝](#致謝)
- [授權](#授權)
- [維護者](#維護者)

---

## 關於本專案

本專案是一套可直接投入使用的**繁體中文 AI Agent 角色定義庫**，服務兩類需求：

1. **實務導入** — 讓中文團隊在 Claude Code 等代理式（agentic）開發環境中，
   以母語調用結構完整、責任邊界清楚的專家角色。
2. **教學示範** — 作為姊妹課程專案
   [`ai-to-agent-agency-course-zh-TW`](https://github.com/draiagent/ai-to-agent-agency-course-zh-TW)
   的教材本體，示範「從單次使用 AI，到編派一支 AI Agent 團隊」的能力轉移路徑。

角色定義的來源為開源專案 The Agency。本專案在其基礎上完成三項工作：**篩選**（自上游約
270 個角色中精選 41 位）、**翻譯**（自英文原文逐檔重譯為台灣用語，非簡繁轉換）、
**在地化擴充**（因應在地治理與產業情境原創新增 5 位角色）。逐檔來源、對應的上游路徑與
快照版本，完整記錄於 [`ATTRIBUTION.md`](ATTRIBUTION.md)。

---

## 專案範圍

| 本專案提供 | 本專案不提供 |
|---|---|
| 純 Agent 定義檔（`.md`），YAML frontmatter 結構與上游完全一致 | 課程、講義、練習題（見姊妹課程專案） |
| 可直接複製至 `~/.claude/agents/` 等目錄使用 | 桌面應用程式或命令列工具 |
| 18 個部門 × 46 位角色（41 位翻譯 + 5 位原創），逐檔人工校對 | 上游 270 個角色的全量翻譯 |
| 跨部門「團隊配方」示範檔（[`rosters/`](rosters/)） | 與上游的即時同步保證 |
| 依上游更新逐檔比對後同步（見 [`UPSTREAM.md`](UPSTREAM.md)） | 中國平台專屬行銷角色（已刻意排除 13 個） |

---

## 選錄清單：18 個部門，46 位數位員工

本專案以「組織」為隱喻：**部門（Domain）對應上游的 division，數位員工（Sub-agent）
對應具體的專家職能角色**。選錄標準為：① 跨產業皆可教學 ② 對應「AI → Agent」能力轉移的
關鍵節點 ③ 一般團隊確有實際需求。

| # | 部門 Domain | 數位員工 Sub-agents | 數量 |
|---|---|---|---|
| 1 | 工程 engineering | backend-architect、frontend-developer、code-reviewer、devops-automator、prompt-engineer、ai-engineer、multi-agent-systems-architect | 7 |
| 2 | 設計 design | ui-designer、ux-researcher | 2 |
| 3 | 產品 product | product-manager、sprint-prioritizer | 2 |
| 4 | 專案管理 project-management | project-manager-senior、meeting-notes-specialist | 2 |
| 5 | 行銷 marketing | content-creator、growth-hacker、seo-specialist、ai-citation-strategist、ecommerce-operator 🆕 | 5 |
| 6 | 銷售 sales | deal-strategist、outbound-strategist | 2 |
| 7 | 財務 finance | financial-analyst、bookkeeper-controller | 2 |
| 8 | 付費媒體 paid-media | ppc-strategist、creative-strategist | 2 |
| 9 | 安全 security | appsec-engineer、penetration-tester | 2 |
| 10 | 測試 testing | test-automation-engineer、accessibility-auditor | 2 |
| 11 | 客戶支援 support | support-responder、analytics-reporter | 2 |
| 12 | 研究 research | synthesist | 1 |
| 13 | 學術 academic | psychologist、statistician | 2 |
| 14 | 醫療 healthcare | clinical-evidence-agent | 1 |
| 15 | 遊戲開發 game-development | game-designer、narrative-designer | 2 |
| 16 | GIS gis | analyst（垂直示範） | 1 |
| 17 | 空間運算 spatial-computing | xr-immersive-developer（垂直示範） | 1 |
| 18 | 跨域專業 specialized | business-strategist、mcp-builder、esg-sustainability-officer、pricing-analyst、animal-welfare-advocate 🆕、public-policy-advocate 🆕、agent-ops-manager 🆕、business-continuity-planner 🆕 | 8 |

> 🆕 標示者為本專案**原創新增角色**（非上游衍生），著作權歸維護者，同依 MIT 釋出。
> `agents/` 目錄依部門分子資料夾（沿用上游 division 名稱），可整包或分部門部署。
> 完成度與版本異動以 [`CHANGELOG.md`](CHANGELOG.md) 為準。

### 原創新增角色

| 角色 | 部門 | 新增緣由 |
|---|---|---|
| 電商營運專員 `ecommerce-operator` | marketing | 上游僅有中國平台版與跨境出口版，均不符台灣本地自營 DTC／多通路情境 |
| 動物福利代言人 `animal-welfare-advocate` | specialized | 為無法自我陳述、無法給知情同意的非人類利害關係人設立代表席位 |
| 政府關係與公共政策 `public-policy-advocate` | specialized | 企業對外影響（政策倡議／PAC／政治獻金）的邊界功能，內建法規與揭露護欄 |
| 數位員工長 `agent-ops-manager` | specialized | 治理 AI Agent 團隊本身——版本控管、最小權限、稽核軌跡、成本歸屬、事故回滾 |
| 營運持續規劃師 `business-continuity-planner` | specialized | 非資安型中斷（天災、斷鏈、關鍵人員流失、基礎設施停擺）的營運持續與危機應變 |

---

## 在地化與翻譯原則

1. **來源** — 一律自英文上游逐檔翻譯，不採用簡體中文版本轉換。
2. **保留原文** — 程式碼區塊、檔案路徑、CLI 名稱、通用英文技術縮寫（RAG、LLM、API、
   OAuth、CI/CD、WCAG、OWASP 等）維持原文；僅翻譯註解、docstring 與填空範本內文。
3. **frontmatter** — `name`、`description`、`vibe` 翻譯；`color`、`emoji`、`tools` 不變，
   確保與上游安裝腳本相容。
4. **術語一致** — 統一技術術語與台灣慣用譯法，對照表見 [`docs/術語對照表.md`](docs/術語對照表.md)。
5. **人工校對** — 每一檔皆經人工逐段校對，不採機器翻譯直出。

---

## 安裝與使用

### Claude Code（macOS / Linux）

```bash
git clone https://github.com/draiagent/AI-to-Agent-Agency-zh-TW.git
mkdir -p ~/.claude/agents
cp AI-to-Agent-Agency-zh-TW/agents/**/*.md ~/.claude/agents/
```

### Claude Code（Windows PowerShell）

```powershell
git clone https://github.com/draiagent/AI-to-Agent-Agency-zh-TW.git
New-Item -ItemType Directory -Force ~/.claude/agents | Out-Null
Get-ChildItem AI-to-Agent-Agency-zh-TW/agents -Recurse -Filter *.md |
  Copy-Item -Destination ~/.claude/agents/
```

重新啟動 Claude Code 會話後，即可以 `/<agent-name>` 呼叫，或交由模型自動挑選。

### 其他工具

frontmatter 結構與上游一致，可直接沿用上游
[`agency-agents` 的 `scripts/install.sh`](https://github.com/msitarzewski/agency-agents/blob/main/scripts/install.sh)
（以本專案為 repo 根目錄執行）。Cursor、GitHub Copilot、Gemini CLI 等請參照上游說明。

---

## 團隊配方（`rosters/`）

[`rosters/`](rosters/) 收錄「將既有角色依真實情境編組為跨部門團隊」的配方檔（原創內容，MIT）。

| 檔案 | 情境 |
|---|---|
| [`rosters/益生寵愛-寵物餐廳-O2O與OEM團隊.md`](rosters/益生寵愛-寵物餐廳-O2O與OEM團隊.md) | 中小型寵物餐廳的「資源整合 → 價值共創 → 線上線下整合 → B2C 電商與 B2B OEM/ODM 雙軌商業模式」，跨 8 個部門、約 14 位數位員工，含非人類利害關係人代表線。對應教學模組見姊妹課程專案。 |
| [`rosters/企業-AI-to-Agent-導入與治理團隊.md`](rosters/企業-AI-to-Agent-導入與治理團隊.md) | 跨產業企業導入配方：以最小可行核心團隊完成 Discover → VAD → VAC → Build → Verify → Govern → Reuse 七階段閉環，包含角色責任、階段閘門、90 天節奏、治理護欄與 KPI 儀表板。 |

---

## 與上游的關係與更新政策

- 本專案**釘選**一個上游快照（commit 與日期），記錄於 [`UPSTREAM.md`](UPSTREAM.md)。
- 上游有實質更新時，**逐檔比對差異**後再決定是否同步，不進行自動 merge。
- 維護檔案約 46 個，同步成本可控，預計每季檢視一次；5 位原創角色不受上游同步影響。
- 上游角色若被移除或大幅改寫，將於 [`CHANGELOG.md`](CHANGELOG.md) 註記，並保留舊版一個週期。

---

## 致謝

本專案的多數角色設定、專業流程與方法論源自下列開源專案，謹此致謝：

- **原始專案**：[The Agency — `agency-agents`](https://github.com/msitarzewski/agency-agents)
- **原始作者**：Michael Sitarzewski（[@msitarzewski](https://github.com/msitarzewski)）與 AgentLand Contributors
- **原始授權**：MIT License

亦感謝簡體中文社群版 [`jnMetaCode/agency-agents-zh`](https://github.com/jnMetaCode/agency-agents-zh)
在先——其存在讓我們確認「繁體中文 + 教學導向」仍是一塊值得投入的空白。

---

## 授權

MIT License。原始英文內容著作權歸 Michael Sitarzewski 與 AgentLand Contributors；
繁體中文翻譯、在地化，以及 5 位原創新增角色（電商營運專員、動物福利代言人、
政府關係與公共政策、數位員工長、營運持續規劃師）之著作權歸維護者，同依 MIT 釋出。
完整條款見 [`LICENSE`](LICENSE)，逐檔來源與原創標記見 [`ATTRIBUTION.md`](ATTRIBUTION.md)。

使用本專案的 Agent 檔案時，請一併保留上述著作權與致謝資訊。

---

## 維護者

**AI Coach 益力康陳董｜2026 AI to Agent**

- 姊妹課程專案：[`ai-to-agent-agency-course-zh-TW`](https://github.com/draiagent/ai-to-agent-agency-course-zh-TW)（CC BY-SA 4.0）
- 貢獻方式：見 [`CONTRIBUTING.md`](CONTRIBUTING.md)；上游同步政策見 [`UPSTREAM.md`](UPSTREAM.md)
- 議題與 PR：請透過本 repo 的 Issues 與 Pull Requests

> 「2026 AI to Agent」是本年度的方法論主張：從「會用 AI」邁向「讓 AI 自主完成工作」。
> 本專案是該主張的公開實作與教學素材之一。
