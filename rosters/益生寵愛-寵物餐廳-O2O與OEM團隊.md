# 團隊配方：益生寵愛寵物餐廳 — O2O 與 OEM/ODM 雙軌經營

> **這是什麼**：一份「數位員工團隊配方」——把本 repo 既有的角色，依一個真實情境
> 編成一支跨部門團隊。情境取自一份 EMBA 論文《寵物餐廳創新經營策略：以益生寵愛寵物餐廳為例》
> 的分析框架，用來示範「Domain（部門）× Sub-agent（數位員工）」如何對應到一個
> 中小企業的實際經營課題。
>
> **授權**：本檔為原創教學文件，MIT，著作權 dr.aiagent。所引用的角色見各自定義檔。
> 對應的教學導引與 Lab 在姊妹 repo
> [`ai-to-agent-agency-course-zh-TW`](https://github.com/draiagent/ai-to-agent-agency-course-zh-TW)
> 的 `curriculum/垂直應用-益生寵愛寵物餐廳.md`。

---

## 0. 情境與核心命題

**個案**：一家中小型寵物餐廳，資源有限，要在「開店做生意」之外，長出可持續的商業模式。

**論文的核心命題**：
> 中小型寵物餐廳可以從**資源限制**出發，透過**資源整合**與**價值共創**累積顧客信任，
> 再透過**線上線下整合**策略，延伸出 **B2C 電商**與 **B2B OEM/ODM** 並行的**商業模式創新**。

**四個理論主軸**（團隊配方就照這四段編）：

| 主軸 | 理論依據 | 對這支團隊的意義 |
|---|---|---|
| 一、資源整合 | 資源基礎觀點 RBV（Barney, 1991） | 先盤點自己有什麼稀缺資源，決定「不做什麼」 |
| 二、價值共創 | 服務主導邏輯 S-D Logic（Vargo & Lusch, 2004） | 顧客、毛孩、員工、醫師、產學一起創造價值 |
| 三、線上線下整合 | 服務行銷（Berry, 1983）、體驗經濟（Pine & Gilmore, 1998） | 把到店體驗接上社群與線上回購 |
| 四、商業模式創新 | 商業模式（Teece, 2010） | B2C 電商與 B2B 代工兩條營收線並行 |

---

## 1. 主軸一：資源整合 — 先盤點，再決定不做什麼

| 數位員工 | 部門 | 在這一段做什麼 | 對應論文訪談對象 |
|---|---|---|---|
| [business-strategist](../agents/specialized/business-strategist.md) | specialized | VRIN 資源盤點（有價值／稀少／難模仿／不可替代）；把「什麼都想做」收斂成 2–3 個聚焦選擇 | — |
| [financial-analyst](../agents/finance/financial-analyst.md) | finance | 資源投入的單位經濟與現金流上限；每個「要不要做」附情境與敏感度 | — |
| [ux-researcher](../agents/design/ux-researcher.md) | design | 用訪談挖出「顧客真正重視、而我們剛好有」的資源，而非想像 | G1–G3 飼主、B1／B2 店長店員 |
| [ui-designer](../agents/design/ui-designer.md) | design | 把「店內空間體驗」當成一種稀缺資源來設計（動線、毛孩友善、可拍照） | A1 空間設計師 |

**驗收重點**：資源盤點要落到「這 3 項是我們難被模仿的，其餘外包或不做」，不是一張什麼都有的清單。

---

## 2. 主軸二：價值共創 — 把不在決策桌上的人（與毛孩）拉進來

| 數位員工 | 部門 | 在這一段做什麼 | 對應論文訪談對象 |
|---|---|---|---|
| [animal-welfare-advocate](../agents/specialized/animal-welfare-advocate.md) 🆕 | specialized | 代表毛孩這個「非人類利害關係人」：把行為與生理訊號翻成需求，設福利護欄（用餐環境、食材、停留時間），對行銷主張有**福利否決權** | 毛孩（透過 G1–G3 與 C1 觀察） |
| [clinical-evidence-agent](../agents/healthcare/clinical-evidence-agent.md) | healthcare | 品牌合作醫師背書的營養／健康主張要有出處，不越獸醫診斷界線 | C1 品牌合作醫師 |
| [ux-researcher](../agents/design/ux-researcher.md) | design | 共創訪談的方法紀律：問題先於方法，回饋要能追溯 | G1–G3、B1／B2 |
| [support-responder](../agents/support/support-responder.md) | support | 把飼主的抱怨與稱讚變成流程改善項，而不是逐則道歉 | G1–G3 |
| [content-creator](../agents/marketing/content-creator.md) | marketing | 把共創故事（醫師、產學、飼主、店員）寫成有受眾與支柱的內容 | C1、D1／E1、G1–G3 |

**驗收重點**：每一個對外健康／營養主張，都能指到 C1 或 D1／E1 的具體依據；毛孩福利與商業最佳化衝突時，福利優先。

---

## 3. 主軸三：線上線下整合（O2O）— 把到店體驗接上線上回購

| 數位員工 | 部門 | 在這一段做什麼 |
|---|---|---|
| [growth-hacker](../agents/marketing/growth-hacker.md) | marketing | 把「到店 → 加 LINE／社群 → 線上回購」寫成可證偽的漏斗實驗，看 CAC／LTV |
| [ecommerce-operator](../agents/marketing/ecommerce-operator.md) 🆕 | marketing | 線上通路（自架站／momo／蝦皮台灣／LINE）營運、會員分級與回購劇本、把線下客導進第 7／21／30 天回購觸發 |
| [seo-specialist](../agents/marketing/seo-specialist.md) | marketing | 在地搜尋意圖（「寵物友善餐廳 台北」「狗狗鮮食 宅配」）的內容結構與技術 SEO |
| [ai-citation-strategist](../agents/marketing/ai-citation-strategist.md) | marketing | 讓品牌在 AI 助理的推薦答案裡被引用 |
| [ppc-strategist](../agents/paid-media/ppc-strategist.md) | paid-media | 在地客獲取的帳戶結構與出價；到達頁與廣告一致 |
| [analytics-reporter](../agents/support/analytics-reporter.md) | support | O2O 成效儀表板：世代留存、線下→線上轉換率、回購率——要基準、要可行動建議 |

**驗收重點**：有一張把「線下體驗」與「線上回購」接起來的漏斗圖，每一步都有數字，不是「多發社群貼文」。

---

## 4. 主軸四：商業模式創新 — B2C 電商與 B2B OEM/ODM 並行

| 數位員工 | 部門 | 在這一段做什麼 | 對應論文訪談對象 |
|---|---|---|---|
| [business-strategist](../agents/specialized/business-strategist.md) | specialized | 雙軌商業模式設計：兩條營收線的價值主張、關鍵活動、價值攫取；哪些資源共用、哪些要分 | — |
| [pricing-analyst](../agents/specialized/pricing-analyst.md) | specialized | B2C：會員分級與檔期折扣上限（附算式）；B2B：OEM/ODM 量價階梯與**底價**（附 ±20% 敏感度） | F1 OEM/ODM 客戶 |
| [deal-strategist](../agents/sales/deal-strategist.md) | sales | B2B 代工客戶的 MEDDPICC 逐項評分，拆穿一廂情願，缺口配補救 | F1 |
| [ecommerce-operator](../agents/marketing/ecommerce-operator.md) 🆕 | marketing | B2C 電商營運：每個 SKU 完整成本、檔期算真實利潤不追 GMV | — |
| [bookkeeper-controller](../agents/finance/bookkeeper-controller.md) | finance | 兩條營收線的帳務分離、成本歸屬、結帳清單與對帳紀律 | — |
| [backend-architect](../agents/engineering/backend-architect.md) | engineering | 若要自建會員／訂閱／訂單系統：資料模型與整合點的架構取捨 | — |
| [esg-sustainability-officer](../agents/specialized/esg-sustainability-officer.md) | specialized | 若 B2B 客戶要求供應鏈永續揭露：用 GRI／SASB 對照，不漂綠 | F1 |

**驗收重點**：兩條營收線各有自己的單位經濟與底價；共用資源（廚房、配方、品牌）與各自成本被清楚拆開。

---

## 5. 共創網絡（人與非人利害關係人 → 對應數位員工）

| 利害關係人 | 論文代號 | 主要對應數位員工 |
|---|---|---|
| 飼主 | G1、G2、G3 | ux-researcher（訪談）、support-responder（回饋迴路）、content-creator（故事） |
| 毛孩（非人類） | — | **animal-welfare-advocate**（訊號翻譯、福利護欄、福利否決權） |
| 店長／店員 | B1、B2 | ux-researcher、support-responder（第一線流程改善） |
| 品牌合作醫師 | C1 | clinical-evidence-agent（健康主張的證據紀律） |
| 產學研發／品管 | D1、E1 | clinical-evidence-agent、content-creator（配方與品質背書） |
| OEM/ODM 客戶 | F1 | deal-strategist、pricing-analyst、esg-sustainability-officer |
| 空間設計師 | A1 | ui-designer（線下體驗即資源） |

> 這張表就是 S-D Logic「價值由多方共創」在 Agent 團隊上的落地：每個共創方都有一個
> 數位員工負責「把他們的輸入接進流程」，而毛孩這個沉默的一方由 animal-welfare-advocate 代言。

---

## 6. 產業脈絡注入段（給每個數位員工的共同背景）

在召喚上述任何數位員工時，附上這段脈絡，能大幅提高產出的貼題程度：

- **市場結構**：台灣少子化與高齡化下的「毛孩經濟」，寵物擬人化（把寵物當家人）推升鮮食、
  保健、體驗型消費；飼主決策高度受獸醫師與同溫層社群影響。
- **信任門檻**：寵物友善餐飲的顧客對「食安、環境衛生、寵物福利」的容忍度極低，一次負評擴散快；
  「醫師背書」「產學配方」是主要的信任來源。
- **法規與品質**：寵物食品相關規範（寵物食品管理標示、CNS 參考、農業部相關公告）持續演進；
  鮮食涉及冷鏈、保存期限、標示；B2B 代工需符合客戶的品保與（有時）永續揭露要求。
- **成本現實**：鮮食毛利受冷鏈物流、退貨損耗、平台抽成侵蝕；檔期折扣容易把 GMV 做大、利潤做負。
- **資源限制**：中小型業者沒有大品牌的行銷預算與供應鏈議價力，策略必須從「我們難被模仿的少數資源」出發。

---

## 7. 這份配方怎麼用（課堂）

1. 一次課只帶一個主軸，對應 4–6 個數位員工。
2. 每個數位員工先看姊妹 repo 的 `agent-notes/<slug>.md`，再做 `labs/<slug>-lab.md`。
3. 期末整合作業：學員扮演「店主」，用四個主軸的順序，把四段產出串成一份
   「益生寵愛雙軌經營計畫」草案，並在每一步標出「這裡我驗收了什麼、退回了什麼」。

> **注意**：本配方是教學示範，非投資或經營建議。所有數位員工的產出都需要真人主管驗收。
