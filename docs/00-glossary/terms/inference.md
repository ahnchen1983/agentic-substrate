---
id: inference
term: Inference
zh: 推論
category: model
layers: [L1]
course_days: [day1]
learning_stages: [level1]
related_terms: [model, training, token, model-provider-request]
source_inspiration:
  - mattpocock/dictionary-of-ai-coding
status: draft
---

# Inference - 推論

## 一句話

Inference 是模型在收到輸入後產生輸出的推論過程。

## 不要誤會成

它不是 training，也不是模型在此刻上網查資料。

## 為什麼重要

理解 inference 有助於分清楚「模型根據 context 推出答案」和「模型真的取得外部證據」。

## 在五層模型的位置

主要對應 L1 模型層。理解它可以幫助你判斷問題發生在五層模型的哪個位置。

## 課程中會出現在哪裡

這個術語會出現在 Day 1 重新認識生成式 AI，用來幫助學員把實作經驗連回 AI 工作系統的概念。

## Agent 需要注意什麼

不要宣稱模型已知道最新事實；需要外部資料時要透過工具取得並標示來源。

## 情境例句

> 「我輸入 prompt 後模型正在做什麼？」
>
> 「它在 inference：根據目前 context 推算下一個輸出，而不是重新訓練自己。」

## 常見錯誤

- 把 inference 當成搜尋網路。
- 以為每次對話都會更新模型權重。
- 忽略輸入 context 對結果的影響。

## 相關術語

- [Model](model.md)
- [Training](training.md)
- [Token](token.md)
- [Model Provider Request](model-provider-request.md)
