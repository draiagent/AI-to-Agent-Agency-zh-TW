# 團隊配方：企業 AI to Agent 導入與治理團隊

> **這是什麼**：一份可跨產業套用的「數位員工團隊配方」。它把本 repo 既有角色，
> 編成一支能完成需求盤點、VAD 視覺化、VAC 任務規格、Agent 執行、Verify 驗證與
> Reuse 知識複利的企業導入團隊。
>
> **核心主張**：企業導入 AI，不是一次叫出 46 位 Agent，而是先用最小可行團隊完成一條
> 可量測、可稽核、可回滾的工作流程，再依需求增加專業席位。
>
> **授權**：本檔為原創教學文件，MIT，著作權 dr.aiagent。所引用角色見各自定義檔。
>
> **品牌方法論**：AI Coach 益力康陳董｜2026 AI to Agent。

---

## 0. 企業命題：從「會使用 AI」走向「讓 Agent 穩定完成工作」

傳統 AI 導入常停在個人提示詞與單次成果；企業真正需要的是能留下來的組織能力：

| 階段 | 核心問題 | 主要產出 |
|---|---|---|
| VAD — Visual Agent Design | 工作、資料、角色與流程是否看得見？ | 現況圖、目標流程圖、責任邊界 |
| VAC — Visual Agent Card | Agent 是否知道要做什麼、做到什麼程度？ | 目標、輸入、步驟、輸出、限制、驗收 |
| Agent Execution | 誰負責執行、如何交接與升級？ | 任務紀錄、工具呼叫、例外處理 |
| Verify | 產出是否正確、安全、可追溯？ | 測試、證據、人工核准、稽核紀錄 |
| Reuse | 成功方法能否變成企業資產？ | 版本化 VAC、團隊配方、知識庫與指標基準 |

> **人的角色不是離場，而是升級成 AI Golfer**：設定目標、選擇球具（模型／工具）、
> 判斷風險並承擔最終決策。Agent 是數位員工，不是法律責任主體。

---

## 1. 最小可行核心團隊（MVT）

先以 10 位數位員工完成第一條企業流程。沒有明確需求時，不要一次召集全部角色。

| 席位 | 數位員工 | 核心責任 | 必交付成果 |
|---|---|---|---|
| 企業贊助人 | **真人主管／流程 Owner** | 決定目標、預算、資料邊界、風險容忍度與 Go／No-Go | 專案章程、最終核准 |
| 策略收斂 | [business-strategist](../agents/specialized/business-strategist.md) | 將企業痛點連到策略價值，刪除低價值需求 | 問題陳述、價值假設 |
| 使用者研究 | [ux-researcher](../agents/design/ux-researcher.md) | 訪談實際使用者，找出工作摩擦與例外 | 現況旅程、需求證據 |
| 產品負責 | [product-manager](../agents/product/product-manager.md) | 定義使用情境、成功指標與範圍 | PRD、KPI、非目標 |
| 導入統籌 | [project-manager-senior](../agents/project-management/project-manager-senior.md) | 排程、依賴、Owner、風險與跨部門交接 | 里程碑、RACI、風險表 |
| 多 Agent 架構 | [multi-agent-systems-architect](../agents/engineering/multi-agent-systems-architect.md) | 決定單 Agent／多 Agent、路由、交接與失敗策略 | Agent 拓撲、狀態流 |
| AI 實作 | [ai-engineer](../agents/engineering/ai-engineer.md) | 模型、RAG、評估與部署的工程落地 | 可運行原型、評估集 |
| 系統連接 | [mcp-builder](../agents/specialized/mcp-builder.md) | 將 Agent 安全連接企業資料與工具 | MCP／API 規格、權限表 |
| 品質驗證 | [test-automation-engineer](../agents/testing/test-automation-engineer.md) | 將 VAC 驗收條件轉成可重跑測試 | 測試案例、回歸報告 |
| Agent 治理 | [agent-ops-manager](../agents/specialized/agent-ops-manager.md) | 版本、權限、成本、稽核、事故回滾與退役 | Agent Registry、稽核軌跡 |
| 成效分析 | [analytics-reporter](../agents/support/analytics-reporter.md) | 建立導入前基準與上線後成效儀表板 | KPI Dashboard、改善建議 |

---

## 2. 七階段閉環與角色編組

### 階段一：Discover — 找對問題，不急著自動化

**主責**：business-strategist、ux-researcher、product-manager  
**支援**：financial-analyst、meeting-notes-specialist

工作：

1. 定義流程 Owner、使用者與利害關係人。
2. 量出目前工時、等待、錯誤、返工與人工作業成本。
3. 找出高頻、規則明確、資料可取得、風險可控的任務。
4. 排除「低頻但高風險」或沒有可驗收標準的偽需求。

**階段閘門**：若沒有基準值、Owner 或可衡量結果，不進入開發。

### 階段二：VAD — 把需求、資料與流程畫出來

**主責**：ux-researcher、product-manager  
**支援**：ui-designer、project-manager-senior

VAD 至少要看見：

- 觸發事件：什麼條件啟動任務？
- 輸入資料：來源、格式、敏感等級與更新頻率。
- 工作節點：人做什麼、Agent 做什麼、何時交接。
- 決策點：哪些可自動決定，哪些必須人工核准。
- 例外路徑：資料不足、工具失敗、低信心或超出授權時怎麼辦。
- 成功終點：何謂完成，證據存放在哪裡。

**階段閘門**：真人流程 Owner 能沿圖說清楚正常路徑與三種主要例外。

### 階段三：VAC — 把成功標準寫成 Agent 可執行的契約

**主責**：product-manager、prompt-engineer、project-manager-senior  
**支援**：sprint-prioritizer、agent-ops-manager

每張 VAC 應包含：

| 欄位 | 必答問題 |
|---|---|
| 目標 Goal | 要解決哪個問題？對誰產生什麼價值？ |
| 素材 Input | 可用哪些資料？來源與版本是什麼？ |
| 角色 Role | 由哪位 Agent 主責？可呼叫誰？ |
| 工具 Tools | 可使用哪些系統？讀寫權限到哪裡？ |
| 步驟 Steps | 正常流程、判斷點與交接順序為何？ |
| 限制 Guardrails | 哪些事不得做？何時必須停止或升級真人？ |
| 輸出 Output | 格式、欄位、存放位置與命名規則為何？ |
| 驗收 Verify | 正確率、時效、完整性、品牌／法規標準為何？ |
| 例外 Exception | 缺資料、矛盾、工具失敗或低信心時如何處理？ |
| 複用 Reuse | 通過驗收後如何版本化並納入企業能力庫？ |

**階段閘門**：另一位未參與規劃的人，能依 VAC 判斷通過或退回。

### 階段四：Build — 組裝 Agent、Memory、Workflow 與 MCP

**主責**：multi-agent-systems-architect、ai-engineer、mcp-builder  
**支援**：backend-architect、prompt-engineer、devops-automator

設計原則：

1. **先單後多**：單一 Agent 能完成就不增加協調成本。
2. **最小權限**：預設唯讀；寫入、刪除、付款、發佈需額外核准。
3. **模型可替換**：VAC 與驗收標準不綁定單一模型品牌。
4. **記憶分層**：任務暫存、專案記憶與企業知識分開管理。
5. **全程留痕**：輸入來源、模型／Agent 版本、工具行為與核准者可追溯。
6. **可停止、可回滾**：每條自動化都要有人工接管與復原路徑。

**階段閘門**：原型能在隔離資料與受控權限下跑完端到端流程。

### 階段五：Verify — 不是看起來不錯，而是證明它可靠

**主責**：test-automation-engineer、agent-ops-manager  
**支援**：code-reviewer、appsec-engineer、statistician、accessibility-auditor

驗證矩陣：

| 面向 | 驗證內容 | 建議證據 |
|---|---|---|
| 任務品質 | 正確、完整、格式一致 | 黃金測試集、人工抽查 |
| 穩定性 | 重跑一致、例外可處理 | 回歸測試、失敗率 |
| 安全性 | 無越權、敏感資料受控 | 權限測試、稽核紀錄 |
| 可解釋性 | 結論能回到來源 | 引用、資料血緣 |
| 成本與速度 | 相較基準是否改善 | Token／API 成本、處理時間 |
| 使用者價值 | 是否降低負擔與返工 | 採用率、滿意度、退回率 |

**階段閘門**：高風險失敗案例未通過，不得用平均分數掩蓋後上線。

### 階段六：Deploy & Govern — 小範圍上線，持續治理

**主責**：agent-ops-manager、project-manager-senior  
**支援**：devops-automator、bookkeeper-controller、appsec-engineer、
business-continuity-planner

上線採三段式：

1. **Shadow Mode**：Agent 產出但不執行，由真人比較。
2. **Human-in-the-loop**：Agent 執行低風險步驟，關鍵動作需核准。
3. **Bounded Autonomy**：只在明確範圍、金額、資料與時間限制內自主執行。

最低治理要求：

- Agent Owner、版本、模型、工具、權限與成本中心有登記。
- 關鍵寫入與對外發佈有審批與撤回機制。
- 有異常警示、停機開關、回滾方案與營運持續計畫。
- 每月檢查錯誤、漂移、成本、使用率與未授權行為。

### 階段七：Reuse — 把一次成功變成企業複利

**主責**：agent-ops-manager、synthesist  
**支援**：meeting-notes-specialist、content-creator、analytics-reporter

通過驗收後沉澱：

- VAC 最終版與版本紀錄。
- 測試資料集、失敗案例與修正決策。
- Agent／模型／工具相容矩陣。
- 標準團隊配方與責任邊界。
- 導入前後 KPI、ROI／SROI 基準。
- 可供下一部門複製的 Playbook 與教學素材。

> **真正的企業資產不是某一個模型，而是需求規格、驗收標準、流程記憶與治理紀律。**

---

## 3. 按需增加的專業席位

核心團隊不應假裝懂所有領域；遇到以下情境才加席位：

| 情境 | 加入的數位員工 | 主要護欄 |
|---|---|---|
| 財務預測、成本或投資判斷 | [financial-analyst](../agents/finance/financial-analyst.md)、[bookkeeper-controller](../agents/finance/bookkeeper-controller.md) | 假設透明、可追溯、真人簽核 |
| 醫療／健康內容 | [clinical-evidence-agent](../agents/healthcare/clinical-evidence-agent.md) | 證據等級、禁越診斷界線 |
| ESG 與揭露 | [esg-sustainability-officer](../agents/specialized/esg-sustainability-officer.md) | 不漂綠、保留證據鏈 |
| 政策與公共倡議 | [public-policy-advocate](../agents/specialized/public-policy-advocate.md) | 法規、揭露與倫理邊界 |
| 對外系統與敏感資料 | [appsec-engineer](../agents/security/appsec-engineer.md) | 最小權限、威脅模型 |
| 高可用與營運中斷 | [business-continuity-planner](../agents/specialized/business-continuity-planner.md) | RTO／RPO、桌上演練 |
| 電商流程 | [ecommerce-operator](../agents/marketing/ecommerce-operator.md) | 毛利、庫存、退款與權限 |
| 銷售流程 | [deal-strategist](../agents/sales/deal-strategist.md) | 不虛構客戶訊號或承諾 |
| 數據實驗與因果判斷 | [statistician](../agents/academic/statistician.md) | 樣本、偏誤、不確定性 |
| 顧客服務 | [support-responder](../agents/support/support-responder.md) | 隱私、升級規則、口徑一致 |

---

## 4. 企業 AI to Agent 導入優先矩陣

每個候選流程以 1–5 分評估：

| 指標 | 低分（1） | 高分（5） |
|---|---|---|
| 頻率 | 偶發 | 每日大量重複 |
| 規則清晰度 | 高度依賴默會判斷 | 步驟與條件明確 |
| 資料可得性 | 分散、缺漏、無權限 | 結構清楚、可合法取得 |
| 驗收可能性 | 好壞難判斷 | 有明確答案或門檻 |
| 商業價值 | 影響小 | 顯著省時、降錯或增收 |
| 風險（反向計分） | 法規／財務／人身風險高 | 低風險、可回復 |

**建議優先**：總分高、風險低、能在 4–8 週形成閉環的流程。  
**不建議首案**：沒有 Owner、沒有基準值、涉及不可逆決策，或必須依賴未授權敏感資料的流程。

---

## 5. 90 天落地節奏

| 時間 | 目標 | 主要活動 | 出口條件 |
|---|---|---|---|
| Day 1–30 | 選對首案 | 基準量測、VAD、VAC、風險分級 | Owner 核准 VAC 與資料邊界 |
| Day 31–60 | 做出受控原型 | Agent／MCP 串接、測試集、Shadow Mode | 端到端測試通過 |
| Day 61–90 | 小範圍營運 | Human-in-the-loop、KPI 儀表板、治理與回滾 | 達到門檻後再決定擴大 |

建議第一案只選一個流程，例如：

- 會議紀錄 → 決策／待辦 → Owner → 截止日 → 追蹤。
- 客服訊息分類 → 草擬回覆 → 高風險升級真人。
- 表單／報表彙整 → 異常偵測 → 主管摘要。
- 公開資料研究 → 來源核驗 → 內容初稿 → 人工發佈。

---

## 6. 驗收儀表板

至少同時追蹤「效率、品質、治理、採用」四類指標：

| 類別 | 建議指標 |
|---|---|
| 效率 | 平均處理時間、等待時間、人工工時、單次成本 |
| 品質 | 正確率、完整率、退回率、返工次數 |
| 治理 | 越權事件、無來源主張、人工升級率、可回滾率 |
| 採用 | 活躍使用者、流程覆蓋率、滿意度、持續使用率 |
| 商業 | 節省成本、增量營收、ROI／SROI、回收期 |

> 指標先做導入前基準，再比較導入後結果；沒有基準，就無法證明 Agent 創造了價值。

---

## 7. 召喚團隊時的共同背景模板

將下列內容與 VAC 一起提供給所有參與的數位員工：

```text
【企業與部門】
產業：
部門：
流程 Owner：
實際使用者：

【要改善的流程】
目前流程：
主要痛點：
導入前基準：
期望成果：
明確不做：

【資料與工具】
允許資料：
禁止資料：
可用工具：
讀寫權限：

【風險與核准】
風險等級：
必須人工核准的動作：
停止／升級條件：
回滾方式：

【驗收】
品質門檻：
時間門檻：
成本上限：
證據與紀錄位置：
```

---

## 8. 課堂與企業工作坊用法

1. 學員以真實工作流程完成一張 VAD。
2. 將 VAD 轉成一張 VAC，交換給另一組驗收是否清楚。
3. 從核心團隊選 3–5 位 Agent，不准一開始全選。
4. 用 Shadow Mode 跑 5–10 個案例，記錄通過、退回與例外。
5. 比較人工基準與 Agent 結果，決定修正、停止或擴大。
6. 通過後將 VAC、測試與指標存入企業能力庫，形成下一輪 Reuse。

---

## 9. 最終原則

> **VAD 讓需求、資料與流程被看見；VAC 讓成功標準被保存；專業 Agent 負責執行；
> Verify 確保正確與安全；Reuse 讓企業能力持續複利。**

這套配方的目的不是用 Agent 取代所有員工，而是把重複工作交給可治理的數位員工，
讓真人把時間留給判斷、創意、關係與責任。

**AI Coach 益力康陳董｜2026 AI to Agent**
