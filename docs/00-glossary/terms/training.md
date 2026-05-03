---
id: training
term: Training
zh: 訓練
category: model
layers: [L1]
course_days: [day1]
learning_stages: [level1]
related_terms: [model, parameters, inference]
source_inspiration:
  - mattpocock/dictionary-of-ai-coding
status: draft
---

# Training - 訓練

## 一句話

Training 是用大量資料和計算調整模型權重，使模型獲得能力的過程。

## 不要誤會成

它不是在聊天中教 AI 一次格式，也不是 prompt engineering。

## 為什麼重要

理解 training 可以避免把 context、memory、fine-tuning 和真正模型訓練混在一起。

## 在五層模型的位置

主要對應 L1 模型層。理解它可以幫助你判斷問題發生在五層模型的哪個位置。

## 課程中會出現在哪裡

這個術語會出現在 Day 1 重新認識生成式 AI，用來幫助學員把實作經驗連回 AI 工作系統的概念。

## Agent 需要注意什麼

不要向使用者暗示單次對話會改變模型本體；要說清楚哪些是暫時 context，哪些是持久知識。

## 情境例句

> 「我在對話裡教 AI 一個格式，這算 training 嗎？」
>
> 「不算。那是提供 context 或建立 Skill；training 是更新模型能力的訓練流程。」

## 常見錯誤

- 把提示詞教學當成模型訓練。
- 忽略訓練資料品質和評估。
- 以為一次對話會改變模型權重。

## 相關術語

- [Model](model.md)
- [Parameters](parameters.md)
- [Inference](inference.md)
