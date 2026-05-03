---
id: non-determinism
term: Non-determinism
zh: 非決定性
category: model
layers: [L1]
course_days: [day1]
learning_stages: [level1]
related_terms: [next-token-prediction, hallucination, automated-review]
source_inspiration:
  - mattpocock/dictionary-of-ai-coding
status: draft
---

# Non-determinism - 非決定性

## 一句話

Non-determinism 是 AI 在相同或相近輸入下可能產生不同輸出的特性。

## 不要誤會成

它不是單純 bug，也不是完全不可控。

## 為什麼重要

它是概率式 AI 和傳統確定性 App 的關鍵差異，會影響測試、教學和工作流穩定性。

## 在五層模型的位置

主要對應 L1 模型層。理解它可以幫助你判斷問題發生在五層模型的哪個位置。

## 課程中會出現在哪裡

這個術語會出現在 Day 1 重新認識生成式 AI，用來幫助學員把實作經驗連回 AI 工作系統的概念。

## Agent 需要注意什麼

需要穩定輸出時，要用模板、範例、低溫度設定、檢查表和版本紀錄降低變動。

## 情境例句

> 「同一個問題問兩次，為什麼答案不一樣？」
>
> 「AI 輸出有 non-determinism。這是概率式系統的特性，所以重要任務要設檢查與版本控制。」

## 常見錯誤

- 期待 AI 像傳統 App 一樣每次完全相同。
- 沒有保存關鍵輸出版本。
- 對需要一致性的流程缺少模板和測試。

## 相關術語

- [Next Token Prediction](next-token-prediction.md)
- [Hallucination](hallucination.md)
- [Automated Review](automated-review.md)
