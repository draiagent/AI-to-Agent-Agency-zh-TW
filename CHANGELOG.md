# 更新紀錄（CHANGELOG）

本檔案記錄選錄、翻譯與上游同步的異動。日期為絕對日期（YYYY-MM-DD）。

維護：**AI Coach 益力康陳董｜2026 AI to Agent**（draiagent）。

## [未發佈] — 原創新增 2 位治理席位（→ 46 位）

### 原創新增（非上游衍生，著作權歸 dr.aiagent，MIT）
- `specialized/agent-ops-manager` — 數位員工長。治理「數位員工團隊本身」：agent 定義檔的
  版本控管、最小權限與存取核准、稽核軌跡、成本歸屬、事故回滾、生命週期關卡。是能力光譜
  L4「會養」的載體。結構參照 `appsec-engineer`、`bookkeeper-controller`。
- `specialized/business-continuity-planner` — 營運持續規劃師。面對非資安型中斷（天災、
  斷鏈、關鍵人員流失、基礎設施停擺、傳染病人力短缺）的營運持續與危機應變：業務衝擊分析、
  RTO／RPO、單點故障盤點、情境劇本、危機溝通、桌上演練。與 `security/` 的事件處理職能互補。

### 文件
- `README.md`、`ATTRIBUTION.md` 更新為「41 翻譯 + 5 原創 = 46 位」；specialized 部門 8 / 8。

## [未發佈] — 補收錄 2 位 + 原創新增 3 位（→ 44 位）

### 補收錄（翻譯自上游 `3c95888`）
- `specialized/esg-sustainability-officer` — ESG 永續長；因應集團永續報告書需求。
  法規追蹤表末新增「台灣」一列為在地化補充（金管會永續報告書規範），已於 `ATTRIBUTION.md` 標註。
- `specialized/pricing-analyst` — 定價分析師；B2C 產品線與 B2B 代工報價共用。

### 原創新增（非上游衍生，著作權歸 dr.aiagent，MIT）
- `specialized/animal-welfare-advocate` — 動物福利代言人。為無法自我陳述、無法給知情同意的
  非人類共創者（動物）設一個代表席位；對商業最佳化有福利護欄／否決權。結構參照 `accessibility-auditor`。
- `specialized/public-policy-advocate` — 政府關係與公共政策。企業對外影響（政策倡議／PAC／
  政治獻金）的邊界功能，內建硬性法規與揭露護欄。結構參照 `clinical-evidence-agent`、`penetration-tester`。
- `marketing/ecommerce-operator` — 電商營運專員。自營 DTC 與台灣本地多通路（momo／蝦皮台灣／
  自架站／LINE），聚焦會員回購與檔期損益。上游僅有中國平台版與跨境出口版，皆不適用。

### 文件
- `ATTRIBUTION.md` 新增「原創新增角色（非上游衍生）」章節。
- `README.md`、`LICENSE` 說明更新為「41 翻譯 + 3 原創 = 44 位」。
- 新增 `rosters/` 目錄與第一份團隊配方
  `rosters/益生寵愛-寵物餐廳-O2O與OEM團隊.md`（原創教學文件，MIT）：以中小型寵物餐廳為例，
  用資源整合／價值共創／線上線下整合／商業模式創新四主軸，把既有角色編成跨部門雙軌經營團隊。

## [未發佈] — 首版：18 部門 39 位數位員工

### 🎉 里程碑：Repo A 全 18 部門完成

上游釘選 `3c9588880b7cafaec325a104899fd8bbe27e7d72`（2026-08-26）。
所有 agent 皆由**英文上游逐檔重新翻譯**為繁體中文（台灣用語），非簡繁轉換，已人工校對。
程式碼區塊（TS/Python/SQL/YAML/HCL/CSS 等）保留原文，僅翻譯註解、docstring 與填空範本內文。
frontmatter 結構與上游一致（`color` hex、`tools:` 等欄位原樣保留），可直接 drop-in。

| # | 部門 | 數位員工 |
|---|---|---|
| 1 | 工程 engineering (7) | backend-architect、frontend-developer、code-reviewer、devops-automator、prompt-engineer、ai-engineer、multi-agent-systems-architect |
| 2 | 設計 design (2) | ui-designer、ux-researcher |
| 3 | 產品 product (2) | product-manager、sprint-prioritizer |
| 4 | 專案管理 project-management (2) | project-manager-senior、meeting-notes-specialist |
| 5 | 行銷 marketing (4) | content-creator、growth-hacker、seo-specialist、ai-citation-strategist |
| 6 | 銷售 sales (2) | deal-strategist（MEDDPICC）、outbound-strategist（訊號驅動外撥） |
| 7 | 財務 finance (2) | financial-analyst、bookkeeper-controller |
| 8 | 付費媒體 paid-media (2) | ppc-strategist、creative-strategist |
| 9 | 安全 security (2) | appsec-engineer、penetration-tester（均為授權情境） |
| 10 | 測試 testing (2) | test-automation-engineer、accessibility-auditor |
| 11 | 客戶支援 support (2) | support-responder、analytics-reporter |
| 12 | 研究 research (1) | synthesist |
| 13 | 學術 academic (2) | psychologist、statistician |
| 14 | 醫療 healthcare (1) | clinical-evidence-agent |
| 15 | 遊戲開發 game-development (2) | game-designer、narrative-designer |
| 16 | GIS gis (1) | analyst（垂直示範） |
| 17 | 空間運算 spatial-computing (1) | xr-immersive-developer（垂直示範） |
| 18 | 跨域專業 specialized (2) | business-strategist、mcp-builder |

**已排除**上游行銷部門下所有中國平台專屬角色（抖音／小紅書／微信／微博／B站／
百度SEO／跨境電商等 13 個）。

### 新增
- 專案骨架：`README.md`、`LICENSE`（MIT）、`ATTRIBUTION.md`、`UPSTREAM.md`、`CONTRIBUTING.md`。
- `docs/術語對照表.md` — 約 350 條，10 大類：資訊通用、架構與後端、前端與 Web、
  LLM 與提示工程、機器學習與 MLOps、多代理系統與協調、設計與 UX 研究、
  產品管理與敏捷、行銷/SEO/AEO-GEO、（其餘散見各檔）。
- `agents/` 39 個 zh-TW 定義檔，依上游 division 名稱分子資料夾。

### 待辦
- 依 `UPSTREAM.md` 同步政策，每季檢視上游更新。
- 姊妹 repo `ai-to-agent-agency-course-zh-TW` 的教案目前涵蓋工程／設計／產品／行銷
  4 部門，其餘 14 部門教案分批補（定義檔已在本 repo）。
