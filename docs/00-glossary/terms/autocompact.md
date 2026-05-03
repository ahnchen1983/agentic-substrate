---
id: autocompact
term: Autocompact
zh: 自動壓縮
category: handoffs
layers: [L4]
course_days: [day3]
learning_stages: [level4]
related_terms: [compaction, context-window, memory-system]
source_inspiration:
  - mattpocock/dictionary-of-ai-coding
status: draft
---

# Autocompact - 自動壓縮

## 一句話

Autocompact 是系統在對話過長時自動壓縮上下文，讓 session 可以繼續運作的機制。

## 不要誤會成

它不是完整備份，也不是無損記憶。

## 為什麼重要

它能延長工作時間，但可能丟失細節、語氣、例外條件和未寫入檔案的決策。

## 在五層模型的位置

主要對應 L4 Agent 協調層。理解它可以幫助你判斷問題發生在五層模型的哪個位置。

## 課程中會出現在哪裡

這個術語會出現在 Day 3 把自己的工作方法交給 AI 協作，用來幫助學員把實作經驗連回 AI 工作系統的概念。

## Agent 需要注意什麼

重要決策要寫回 repo 或 handoff artifact；壓縮後要重新檢查關鍵假設是否還存在。

## 情境例句

> 「為什麼長對話中途之後，AI 像是換了一個腦袋？」
>
> 「可能發生 autocompact。系統把前面內容壓縮成摘要，細節不一定完整保留。」

## 常見錯誤

- 以為 autocompact 會無損保存所有細節。
- 重要決策只留在對話裡，沒有寫回檔案。
- 沒有在壓縮後重新確認關鍵假設。

## 相關術語

- [Compaction](compaction.md)
- [Context Window](context-window.md)
- [Memory System](memory-system.md)
