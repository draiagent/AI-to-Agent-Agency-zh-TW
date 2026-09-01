# 貢獻指南（CONTRIBUTING）

## 翻譯原則

1. **從英文上游翻譯**，不做簡繁轉換。簡體社群版僅供對照。
2. **frontmatter**：翻譯 `name` / `description` / `vibe`；`color` / `emoji` 不動；
   維持欄位順序與 `---` 圍籬結構，讓檔案仍可 drop-in。
3. **保留不譯**：程式碼區塊本體、行內程式碼、檔案路徑、指令名稱（`git`、`npm`、`docker`…）、
   通用英文技術縮寫（RAG、MLOps、LLM、API、OAuth、SOC 2、OWASP、REST、GraphQL、
   Kubernetes、CI/CD…）。程式碼區塊內的**註解**可譯為繁體中文。
4. **術語一致**：一律查 [`docs/術語對照表.md`](docs/術語對照表.md)。新術語先加進對照表再用。
5. **語域**：寫給資深軟體工作者看的專業技術文體，避免逐字直譯與中國大陸用語
   （影片非视频、軟體非软件、品質非质量、程式碼非代码、預設非默认、佇列非队列）。
6. **Agent 的自我稱述**（"You are an X"）用繁體中文 AI 系統提示的自然語氣（「你是……」）。

## 流程

1. 認領一個選錄清單上的 Agent（見 `README.md`）。
2. `git -C upstream-ref show HEAD:<上游路徑>` 取得英文原文。
3. 翻譯 → 存到 `agents/<模組>/<slug>.md`。
4. 更新 `ATTRIBUTION.md` 逐檔對應表、`CHANGELOG.md`。
5. 自我檢查：frontmatter 結構完整、術語一致、程式碼未被誤譯。
6. 開 PR，一個 Agent 一個 PR，方便審。

## 有錯就修

發現既有翻譯有誤（術語、語意、漏譯、frontmatter 壞掉）時，直接開 PR 修正，
並在 `CHANGELOG.md` 的「修正」區記一列。
