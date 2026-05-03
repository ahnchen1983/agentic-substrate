---
id: prefix-cache
term: Prefix cache
zh: 前綴快取
category: model
layers: [L1, L4]
course_days: [day2]
learning_stages: [level2, level4]
related_terms: [input-tokens, cache-tokens, context-window]
source_inspiration:
  - mattpocock/dictionary-of-ai-coding
status: draft
---

# Prefix cache - 前綴快取

## 一句話

Prefix cache 是對重複出現在輸入前段的內容進行快取，以降低成本或延遲的機制。

## 不要誤會成

它不是記憶系統，也不是保證所有重複內容都會被快取。

## 為什麼重要

固定 system prompt、長規格和工具 schema 常受 prefix cache 影響。

## 在五層模型的位置

主要對應 L1 模型層、L4 Agent 協調層。理解它可以幫助你判斷問題發生在五層模型的哪個位置。

## 課程中會出現在哪裡

這個術語會出現在 Day 2 AI 工具的選擇與搭配，用來幫助學員把實作經驗連回 AI 工作系統的概念。

## Agent 需要注意什麼

要保持穩定前綴時也要避免塞入過期資訊；快取策略不能取代內容設計。

## 情境例句

> 「為什麼相同系統提示和長背景可以被重用？」
>
> 「prefix cache 會快取前面相同的一段輸入，適合固定規則加不同任務的場景。」

## 常見錯誤

- 以為改一點點內容也一定命中快取。
- 為了快取犧牲清楚度。
- 把快取當成記憶系統。

## 相關術語

- [Input Tokens](input-tokens.md)
- [Cache Tokens](cache-tokens.md)
- [Context Window](context-window.md)
