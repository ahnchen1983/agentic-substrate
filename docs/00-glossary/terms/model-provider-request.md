---
id: model-provider-request
term: Model provider request
zh: 模型供應商請求
category: model
layers: [L1, L2]
course_days: [day2]
learning_stages: [level2]
related_terms: [model-provider, inference, input-tokens, output-tokens, tool-result]
source_inspiration:
  - mattpocock/dictionary-of-ai-coding
status: draft
---

# Model provider request - 模型供應商請求

## 一句話

Model provider request 是送到模型供應方的一次請求，通常包含訊息、參數、工具定義和上下文。

## 不要誤會成

它不是使用者肉眼看到的單一句 prompt。

## 為什麼重要

理解 request 可以幫助除錯、控成本、做稽核，也能釐清哪些資料真的被送出去。

## 在五層模型的位置

主要對應 L1 模型層、L2 工具與環境層。理解它可以幫助你判斷問題發生在五層模型的哪個位置。

## 課程中會出現在哪裡

這個術語會出現在 Day 2 AI 工具的選擇與搭配，用來幫助學員把實作經驗連回 AI 工作系統的概念。

## Agent 需要注意什麼

處理 request log 時要注意敏感資料；重現問題時要記錄模型、參數、工具和輸入摘要。

## 情境例句

> 「一次 API 請求裡到底送了什麼？」
>
> 「model provider request 可能包含 prompt、system message、工具 schema、上下文、參數和安全設定。」

## 常見錯誤

- 只看使用者輸入，忽略系統與工具資訊。
- 把 request log 暴露給不該看的人。
- 沒有記錄參數，導致結果難以重現。

## 相關術語

- [Model Provider](model-provider.md)
- [Inference](inference.md)
- [Input Tokens](input-tokens.md)
- [Output Tokens](output-tokens.md)
- [Tool Result](tool-result.md)
