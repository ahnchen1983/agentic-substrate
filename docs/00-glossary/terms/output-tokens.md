---
id: output-tokens
term: Output tokens
zh: 輸出詞元
category: model
layers: [L1]
course_days: [day2]
learning_stages: [level2]
related_terms: [token, inference, model-provider-request]
source_inspiration:
  - mattpocock/dictionary-of-ai-coding
status: draft
---

# Output tokens - 輸出詞元

## 一句話

Output tokens 是模型生成出來的回應內容所切成的 token。

## 不要誤會成

它不是輸出字數的精確等價物。

## 為什麼重要

輸出越長通常成本越高、延遲越久，也越需要檢查。

## 在五層模型的位置

主要對應 L1 模型層。理解它可以幫助你判斷問題發生在五層模型的哪個位置。

## 課程中會出現在哪裡

這個術語會出現在 Day 2 AI 工具的選擇與搭配，用來幫助學員把實作經驗連回 AI 工作系統的概念。

## Agent 需要注意什麼

要限制輸出格式、長度和欄位，避免要求模型一次產生無邊界的大量內容。

## 情境例句

> 「為什麼叫 AI 寫長文會比較貴也比較慢？」
>
> 「因為生成的內容會計為 output tokens。越長的輸出通常成本和延遲越高。」

## 常見錯誤

- 只要求越長越好。
- 沒有限制格式和長度。
- 忽略長輸出更需要檢查。

## 相關術語

- [Token](token.md)
- [Inference](inference.md)
- [Model Provider Request](model-provider-request.md)
