---
id: stateless
term: Stateless
zh: 無狀態
category: sessions-context-windows-and-turns
layers: [L1, L4]
course_days: [day1, day3]
learning_stages: [level1, level4]
related_terms: [stateful, session, memory-system]
source_inspiration:
  - mattpocock/dictionary-of-ai-coding
status: draft
---

# Stateless - 無狀態

## 一句話

Stateless 指每次請求基本上獨立，系統不自動保留先前完整狀態。

## 不要誤會成

它不是不能做長任務，而是需要把必要狀態明確帶入。

## 為什麼重要

API、工具呼叫和某些 agent step 常是 stateless，這會影響 workflow 設計。

## 在五層模型的位置

主要對應 L1 模型層、L4 Agent 協調層。理解它可以幫助你判斷問題發生在五層模型的哪個位置。

## 課程中會出現在哪裡

這個術語會出現在 Day 1 重新認識生成式 AI、Day 3 把自己的工作方法交給 AI 協作，用來幫助學員把實作經驗連回 AI 工作系統的概念。

## Agent 需要注意什麼

每次呼叫要提供必要 context，並把中間狀態寫到可持久的位置。

## 情境例句

> 「API 每次都要把背景資料重新送一次，為什麼？」
>
> 「因為它通常是 stateless。服務端不一定保留你上一輪的完整上下文。」

## 常見錯誤

- 期待 stateless API 自動記得先前對話。
- 沒有在 request 中帶入必要狀態。
- 把無狀態設計誤認為功能不足。

## 相關術語

- [Stateful](stateful.md)
- [Session](session.md)
- [Memory System](memory-system.md)
