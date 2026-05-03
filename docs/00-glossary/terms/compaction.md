---
id: compaction
term: Compaction
zh: 壓縮
category: handoffs
layers: [L4]
course_days: [day3]
learning_stages: [level4]
related_terms: [context-window, session, autocompact, memory-system]
source_inspiration:
  - mattpocock/dictionary-of-ai-coding
status: draft
---

# Compaction - 壓縮

## 一句話

Compaction 是把長對話或大量資訊壓縮成較短摘要，以便放回 context window 的過程。

## 不要誤會成

它不是完整原文，也不是保證無損的記憶系統。

## 為什麼重要

它讓長任務可以延續，但也可能造成細節遺失或錯誤簡化。

## 在五層模型的位置

主要對應 L4 Agent 協調層。理解它可以幫助你判斷問題發生在五層模型的哪個位置。

## 課程中會出現在哪裡

這個術語會出現在 Day 3 把自己的工作方法交給 AI 協作，用來幫助學員把實作經驗連回 AI 工作系統的概念。

## Agent 需要注意什麼

壓縮摘要要包含目標、已完成事項、決策理由、待辦、風險和不可更動的使用者變更。

## 情境例句

> 「對話太長時，系統幫我摘要，這跟記憶一樣嗎？」
>
> 「不一樣。compaction 是壓縮工作上下文，不是完整記憶。被壓掉的細節可能回不來。」

## 常見錯誤

- 以為 compaction 沒有資訊損失。
- 沒有把決策寫進持久文件。
- 壓縮摘要太籠統，導致後續 Agent 無法接手。

## 相關術語

- [Context Window](context-window.md)
- [Session](session.md)
- [Autocompact](autocompact.md)
- [Memory System](memory-system.md)
