---
id: session
term: Session
zh: 工作階段
category: sessions-context-windows-and-turns
layers: [L4, L5]
course_days: [day3]
learning_stages: [level4]
related_terms: [turn, stateless, memory-system, compaction]
source_inspiration:
  - mattpocock/dictionary-of-ai-coding
status: draft
---

# Session - 工作階段

## 一句話

Session 是一次連續互動或工作期間所形成的暫時上下文。

## 不要誤會成

它不是永久記憶，也不是 repo 狀態的替代品。

## 為什麼重要

很多 Agent 問題來自 session 結束後脈絡消失，因此需要文件化和 handoff。

## 在五層模型的位置

主要對應 L4 Agent 協調層、L5 Interface 使用介面層。理解它可以幫助你判斷問題發生在五層模型的哪個位置。

## 課程中會出現在哪裡

這個術語會出現在 Day 3 把自己的工作方法交給 AI 協作，用來幫助學員把實作經驗連回 AI 工作系統的概念。

## Agent 需要注意什麼

重要結果要寫回檔案、issue、decision log 或其他持久位置，不要只留在對話裡。

## 情境例句

> 「為什麼這個對話結束後，下一次又要重新讀檔？」
>
> 「因為 session 是一次工作上下文。除非狀態寫進檔案或記憶系統，下一次不一定可見。」

## 常見錯誤

- 把 session 當成永久工作區。
- 重要決策只留在聊天中。
- 不知道何時需要 handoff。

## 相關術語

- [Turn](turn.md)
- [Stateless](stateless.md)
- [Memory System](memory-system.md)
- [Compaction](compaction.md)
