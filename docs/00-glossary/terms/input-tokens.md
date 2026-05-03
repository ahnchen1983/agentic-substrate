---
id: input-tokens
term: Input tokens
zh: 輸入詞元
category: model
layers: [L1]
course_days: [day2]
learning_stages: [level2]
related_terms: [token, context-window, prefix-cache]
source_inspiration:
  - mattpocock/dictionary-of-ai-coding
status: draft
---

# Input tokens - 輸入詞元

## 一句話

Input tokens 是送進模型的輸入內容所切成的 token，包括提示、上下文、檔案片段和工具結果。

## 不要誤會成

它不是只算使用者最後打的那一句話。

## 為什麼重要

成本、速度和注意力都會受 input tokens 影響，長文件任務尤其明顯。

## 在五層模型的位置

主要對應 L1 模型層。理解它可以幫助你判斷問題發生在五層模型的哪個位置。

## 課程中會出現在哪裡

這個術語會出現在 Day 2 AI 工具的選擇與搭配，用來幫助學員把實作經驗連回 AI 工作系統的概念。

## Agent 需要注意什麼

要先篩選、摘要或分段輸入，避免把不必要內容塞進每一輪。

## 情境例句

> 「我只要求 AI 回答 100 字，為什麼還是花很多 token？」
>
> 「因為 input tokens 也算。你前面貼的文件、規則和工具結果都會進成本。」

## 常見錯誤

- 只估輸出，不估輸入。
- 長文件沒有先摘要或切塊。
- 重複貼相同背景資料。

## 相關術語

- [Token](token.md)
- [Context Window](context-window.md)
- [Prefix Cache](prefix-cache.md)
