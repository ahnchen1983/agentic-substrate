---
id: attention-relationship
term: Attention relationship
zh: 注意力關係
category: failure-modes
layers: [L1]
course_days: [day1]
learning_stages: [level1]
related_terms: [attention-budget, attention-degradation, context-window]
source_inspiration:
  - mattpocock/dictionary-of-ai-coding
status: draft
---

# Attention relationship - 注意力關係

## 一句話

Attention relationship 指 context 裡不同資訊之間的距離、順序、標題和關聯如何影響模型判斷。

## 不要誤會成

它不是資料有沒有被放進去而已，而是資料怎麼被排列和強調。

## 為什麼重要

同樣內容放在不同位置，模型可能給出不同權重；這會影響長規格、課程文稿和 agent protocol。

## 在五層模型的位置

主要對應 L1 模型層。理解它可以幫助你判斷問題發生在五層模型的哪個位置。

## 課程中會出現在哪裡

這個術語會出現在 Day 1 重新認識生成式 AI，用來幫助學員把實作經驗連回 AI 工作系統的概念。

## Agent 需要注意什麼

設計 context 時要讓目標、資料、例外和驗收標準彼此靠近，避免矛盾指令散落各處。

## 情境例句

> 「同一段規則，放在文件開頭和埋在附錄，效果一樣嗎？」
>
> 「通常不一樣。資訊在 context 裡的位置、密度和相互關係，都會影響模型注意到什麼。」

## 常見錯誤

- 把 context 當成平面的資料庫。
- 重要規則沒有靠近任務目標。
- 混放互相矛盾的指示。

## 相關術語

- [Attention Budget](attention-budget.md)
- [Attention Degradation](attention-degradation.md)
- [Context Window](context-window.md)
