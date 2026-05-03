---
id: contextual-knowledge
term: Contextual knowledge
zh: 脈絡知識
category: failure-modes
layers: [L1, L4]
course_days: [day1, day3]
learning_stages: [level1, level4]
related_terms: [context, parametric-knowledge, memory-system]
source_inspiration:
  - mattpocock/dictionary-of-ai-coding
status: draft
---

# Contextual knowledge - 脈絡知識

## 一句話

Contextual knowledge 是模型在當前任務中透過 context 臨時取得的知識。

## 不要誤會成

它不是模型原本就知道的 parametric knowledge，也不保證下次 session 還在。

## 為什麼重要

它讓 Agent 能理解特定 repo、課程、客戶或專案，但需要被正確載入與維護。

## 在五層模型的位置

主要對應 L1 模型層、L4 Agent 協調層。理解它可以幫助你判斷問題發生在五層模型的哪個位置。

## 課程中會出現在哪裡

這個術語會出現在 Day 1 重新認識生成式 AI、Day 3 把自己的工作方法交給 AI 協作，用來幫助學員把實作經驗連回 AI 工作系統的概念。

## Agent 需要注意什麼

遇到專案特定內容時，要優先讀取 repo 文件或使用者提供資料，不要只靠內建知識猜。

## 情境例句

> 「這個 repo 的課程方向，模型原本不會知道吧？」
>
> 「對，它是透過你貼的內容、檔案和我們讀到的資料取得 contextual knowledge。」

## 常見錯誤

- 把 contextual knowledge 誤認成模型內建知識。
- 沒有提供足夠背景就期待精準輸出。
- 忘記新 session 需要重新載入或讀取這些資料。

## 相關術語

- [Context](context.md)
- [Parametric Knowledge](parametric-knowledge.md)
- [Memory System](memory-system.md)
