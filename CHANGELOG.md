# 更新紀錄（CHANGELOG）

本檔案記錄選錄、翻譯與上游同步的異動。日期為絕對日期（YYYY-MM-DD）。

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
