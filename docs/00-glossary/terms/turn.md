---
id: turn
term: Turn
zh: 對話輪次
category: sessions-context-windows-and-turns
layers: [L1, L5]
course_days: [day1]
learning_stages: [level1]
related_terms: [session, context, model-provider-request]
source_inspiration:
  - mattpocock/dictionary-of-ai-coding
status: draft
---

# Turn - 對話輪次

## 一句話

Turn 是對話或 Agent 執行中的一個互動回合，可能包含訊息、工具呼叫和工具結果。

## 不要誤會成

它不是只有使用者一句話，也不一定只有模型一段回答。

## 為什麼重要

多工具 Agent 的一個 turn 可能包含觀察、行動和修正，理解 turn 有助於除錯工作流。

## 在五層模型的位置

主要對應 L1 模型層、L5 Interface 使用介面層。理解它可以幫助你判斷問題發生在五層模型的哪個位置。

## 課程中會出現在哪裡

這個術語會出現在 Day 1 重新認識生成式 AI，用來幫助學員把實作經驗連回 AI 工作系統的概念。

## Agent 需要注意什麼

回報時要區分使用者要求、Agent 推論、工具呼叫和工具回傳，避免混在一起。

## 情境例句

> 「這一輪回答為什麼會受到我剛剛補充的限制影響？」
>
> 「因為一個 turn 包含使用者輸入、模型回應，也可能包含工具呼叫與結果。」

## 常見錯誤

- 只把使用者一句話當成 turn。
- 忽略工具結果會改變同一輪推理。
- 長 turn 裡混入太多目標。

## 相關術語

- [Session](session.md)
- [Context](context.md)
- [Model Provider Request](model-provider-request.md)
