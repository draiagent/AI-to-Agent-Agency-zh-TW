# 貢獻指南（CONTRIBUTING）

維護：**AI Coach 益力康陳董｜2026 AI to Agent**（draiagent）。
本 repo 只放 Agent 定義檔；教材（教學導引、Lab、課綱）請到姊妹 repo
[`ai-to-agent-agency-course-zh-TW`](https://github.com/draiagent/ai-to-agent-agency-course-zh-TW)。

貢獻分兩類：**（A）翻譯／校對上游角色**、**（B）原創新增在地角色**。兩者流程不同，見下。

## A. 翻譯原則

1. **從英文上游翻譯**，不做簡繁轉換。簡體社群版僅供對照。
2. **frontmatter**：翻譯 `name` / `description` / `vibe`；`color` / `emoji` / `tools` 不動；
   維持欄位順序與 `---` 圍籬結構，讓檔案仍可 drop-in。
3. **保留不譯**：程式碼區塊本體、行內程式碼、檔案路徑、指令名稱（`git`、`npm`、`docker`…）、
   通用英文技術縮寫（RAG、MLOps、LLM、API、OAuth、SOC 2、OWASP、REST、GraphQL、
   Kubernetes、CI/CD…）。程式碼區塊內的**註解**可譯為繁體中文。
4. **術語一致**：一律查 [`docs/術語對照表.md`](docs/術語對照表.md)。新術語先加進對照表再用。
5. **語域**：寫給資深軟體工作者看的專業技術文體，避免逐字直譯與中國大陸用語
   （影片非视频、軟體非软件、品質非质量、程式碼非代码、預設非默认、佇列非队列）。
6. **Agent 的自我稱述**（"You are an X"）用繁體中文 AI 系統提示的自然語氣（「你是……」）。

### A 流程

1. 認領一個選錄清單上的 Agent（見 `README.md`）。
2. 取得英文原文：`git -C upstream-ref show HEAD:<上游路徑>`
   （`upstream-ref` 為 `msitarzewski/agency-agents` 的本地 clone，釘選 commit 見 `UPSTREAM.md`）。
3. 翻譯 → 存到 `agents/<模組>/<slug>.md`。
4. 更新 `ATTRIBUTION.md` 逐檔對應表、`CHANGELOG.md`。
5. 自我檢查：frontmatter 結構完整、術語一致、程式碼未被誤譯。
6. 開 PR，一個 Agent 一個 PR，方便審。

## B. 原創新增角色

當某個在地需求（產業情境、治理席位、非人類利害關係人）在上游找不到對應角色時，
可原創新增。目前已有 5 位（見 `ATTRIBUTION.md`「原創新增角色」章節）。

### B 流程

1. 先開 issue 說明：缺口是什麼、為什麼不適合用現有角色、擬參照哪一個上游角色的結構。
2. 撰寫 `agents/<模組>/<slug>.md`，frontmatter 與正文結構比照上游同類角色
   （身分與記憶、關鍵規則／硬底線、交付物、工作流程、溝通風格、成功指標、
   「這個 Agent 不做什麼」）。
3. 對「影響力／權限」類角色（政策倡議、滲透測試、數位員工治理等）**必須**內建硬性護欄段落。
4. 更新 `ATTRIBUTION.md`「原創新增角色（非上游衍生）」表、`README.md` 選錄清單（標 🆕）、
   `CHANGELOG.md`；著作權歸維護者，同依 MIT 釋出。
5. 一個角色一個 PR。

## 有錯就修

發現既有翻譯或角色有誤（術語、語意、漏譯、frontmatter 壞掉）時，直接開 PR 修正，
並在 `CHANGELOG.md` 記一列。
