# Week 1 Sources

> 主題：大腦核心：LLM 選擇與參數設定（LLM & Config）。本筆記記錄本週實際使用過的資料來源與用途。

## 1. Coze 官方教材／文件

### LLM

[Coze LLM](https://www.coze.com/open/docs/guides/llm)

**用途：**
本週課綱提供的 Coze LLM 參考資料，用於理解 Coze 中 LLM 與模型相關設定。

### Model Service

[Coze Model Service](https://www.coze.com/open/docs/guides/model_service)

**用途：**
本週課綱提供的模型服務參考資料。

### Viewing Model

[Coze Viewing Model](https://www.coze.com/open/docs/guides/viewing_model)

**用途：**
本週課綱提供的模型查看相關資料。

### Coze 平台實際操作

本週也直接在 Coze 平台進行實際操作，包括：

- Model Selection
- Model Management
- Model settings
- Usage Records
- Preview & Debug

> 平台實際操作畫面屬於本週實作證據，不應自行補成官方文件中沒有寫明的結論。

---

## 2. Google Gemini 官方資料

### Gemini Models

[Gemini Models](https://ai.google.dev/gemini-api/docs/models)

**用途：**
實際查看 Gemini 目前提供的模型與不同模型定位。

本週主要關注：

- Gemini 2.5 Pro
- Gemini 2.5 Flash
- Gemini 2.5 Flash-Lite

### Gemini API Pricing

[Gemini API Pricing](https://ai.google.dev/gemini-api/docs/pricing)

**用途：**
比較 Gemini 2.5 Pro、Flash、Flash-Lite 的官方 API 定價。

本週查閱時記錄的價格已整理於 [W1-研究筆記](W1-研究筆記.md)。
價格屬於會隨時間更新的資訊，因此後續引用時應標示為「本週查閱官方頁面時的定價」，並在需要時重新確認。

---

## 3. 本週資料來源使用原則

本週盡量以：

1. 官方模型網站
2. 官方文件
3. Coze 平台實際操作結果

作為主要證據。

如果平台實際畫面與外部資料存在差異，不自行推測原因，而是分開記錄：

- 官方資料顯示什麼
- Coze 實際介面顯示什麼
- 哪些地方目前仍無法確認

---

## 4. 目前仍需要注意的資料缺口

### Coze 最便宜模型

本週曾嘗試從 Coze Model Management、模型詳細頁與 Usage Records 尋找模型價格。

**實際觀察：**

- Free filter 顯示 Results 0。
- 帳號仍有每日可使用的 Credit。
- 模型詳細頁可以看到使用紀錄等資訊，但沒有在本週操作中直接找到完整的模型價格比較表。

因此需要區分：
**「免費 Credit」、「Free 模型」、「模型 API 價格」不是同一概念。**

本週曾進一步使用模型供應商官方 API 價格作為比較參考，但這不應直接寫成 Coze 平台本身的 Credit 單價。

---

## 5. 尚未正式查證的項目

以下內容尚未完成官方查證，目前不補來源，也不視為已確認：

- Coze Response max length 的精確單位
- Context rounds 在 Coze 中更細部的計算方式
- Coze 所有模型的完整 Credit 單價排序

這些如果後續作業需要精確描述，再回官方文件查證。

## 6. NIST SP 800-86｜數位鑑識業務流程

**名稱：** Guide to Integrating Forensic Techniques into Incident Response

**機構：** National Institute of Standards and Technology（NIST）

**出版時間：** 2006 年 8 月

**正式來源：** [NIST SP 800-86 官方 PDF](https://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-86.pdf)

### 本次用途與對照範圍

- Section 3、Figure 3-1：確認 Collection → Examination → Analysis → Reporting 四個核心階段。
- Section 3.1.2：對照資料取得、完整性與 chain of custody 的相關說明。
- Sections 3.2–3.4：協助區分 Examination、Analysis 與 Reporting。
- Section 2 與 Section 3.4：作為理解準備、程序、後續管理與流程改善的參考。

### 正式來源與學習整理的界線

- 「案件需求／調查問題 → 權限、程序與技術準備 → Collection → Examination → Analysis → Reporting → 證據保存／後續管理與流程改善」是依資料整理出的較大學習架構，**不是 NIST 官方七階段模型**。
- Reporting 中「AI 模型與偏差揭露」是個人延伸思考，**不是 NIST 的固定規定**。
- USB 18:32 接入、`backup_0915.zip` 18:35 建立等紀錄屬於本次學習的模擬情境，不是 NIST 提供的案例或真實案件證據。
- Agent 推薦優先人工查看項目、縮小實作範圍及模型選擇的連結，均為目前的個人構想或應用假設，不是 NIST 對 AI Agent 的結論，也尚未完成實際驗證。

對應筆記：[W1-學習歷程](W1-學習歷程.md)、[W1-研究筆記](W1-研究筆記.md)。

## 7. Parameter 與 Distillation｜正式來源補充查證

### Google for Developers — Machine Learning Glossary

[Machine Learning Glossary](https://developers.google.com/machine-learning/glossary)

**對照詞條：** parameter、model capacity。

**用途：**查證 Parameter 是模型在訓練過程中學習到的 weights 與 biases；model capacity 通常會隨 model parameters 數量增加。

**引用界線：**上述關係不應改寫成「parameter 越多，特定任務一定越準確」。此來源用於核對我的概念理解，不是模型效能實驗。

### Google for Developers — LLMs: Fine-tuning, distillation, and prompt engineering

[LLMs: Fine-tuning, distillation, and prompt engineering](https://developers.google.com/machine-learning/crash-course/llm/tuning)

**對照段落：** Distillation。

**用途：**查證蒸餾建立較小的 student model，並透過較大 teacher model 的輸出傳遞知識，支持我「用小模型學習較大模型部分能力」的理解。

**引用界線：**蒸餾通常可降低推論所需的計算資源，但不保證結果完全等同 teacher；本次補充沒有新增蒸餾實驗或實測結果。

### Google Research — Distilling the Knowledge in a Neural Network

[Distilling the Knowledge in a Neural Network](https://research.google/pubs/distilling-the-knowledge-in-a-neural-network/)

**用途：**作為 Knowledge Distillation 的經典研究補充來源。繳交版不深入介紹公式或訓練方法，也不宣稱已重現研究。

### 本次補充解決的資料缺口

Parameter 的定義與容量關係、Distillation 的 teacher／student 概念，已補入可對照的正式來源，並同步更新 [W1-研究筆記](W1-研究筆記.md) 與 [W1-繳交版](W1-繳交版.md)。這解決的是概念的來源缺口，不代表完成模型訓練、準確度比較或蒸餾效能驗證；[W1-學習歷程](W1-學習歷程.md) 的原始回答保持不變。
