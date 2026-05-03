---
id: cache-tokens
term: Cache tokens
zh: 快取詞元
category: model
layers: [L1]
course_days: [day2]
learning_stages: [level2]
related_terms: [token, prefix-cache, input-tokens]
source_inspiration:
  - mattpocock/dictionary-of-ai-coding
status: draft
---

# Cache tokens - 快取詞元

## 一句話

Cache tokens 是模型服務對重複輸入片段計費或處理時使用快取後產生的 token 類型。

## 不要誤會成

它不是免費 token，也不是長期記憶。

## 為什麼重要

它影響成本與延遲，尤其是固定系統提示、長規格或重複參考資料的工作流。

## 在五層模型的位置

主要對應 L1 模型層。理解它可以幫助你判斷問題發生在五層模型的哪個位置。

## 課程中會出現在哪裡

這個術語會出現在 Day 2 AI 工具的選擇與搭配，用來幫助學員把實作經驗連回 AI 工作系統的概念。

## Agent 需要注意什麼

不要為了快取保留過期 context；快取命中不代表輸出正確。

## 情境例句

> 「為什麼同一份長文件第二次處理比較便宜？」
>
> 「有些平台會把重複前綴計為 cache tokens，讓相同 context 的重複使用成本下降。」

## 常見錯誤

- 以為所有 provider 都用同一種快取規則。
- 為了快取保留過多無用 context。
- 忽略快取只影響成本，不保證品質。

## 相關術語

- [Token](token.md)
- [Prefix Cache](prefix-cache.md)
- [Input Tokens](input-tokens.md)
