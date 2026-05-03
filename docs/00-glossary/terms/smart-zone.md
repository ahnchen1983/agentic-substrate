---
id: smart-zone
term: Smart zone
zh: 智慧區
category: failure-modes
layers: [L1, L4]
course_days: [day1, day3]
learning_stages: [level1, level4]
related_terms: [attention-budget, attention-degradation, context-window]
source_inspiration:
  - mattpocock/dictionary-of-ai-coding
status: draft
---

# Smart zone - 智慧區

## 一句話

Smart zone 是 context 中最容易被模型注意並影響輸出的關鍵位置。

## 不要誤會成

它不是正式標準名詞，而是用來提醒資訊擺放會影響模型注意力的工作概念。

## 為什麼重要

把任務目標、限制和驗收標準放在 smart zone，可以提升長任務穩定度。

## 在五層模型的位置

主要對應 L1 模型層、L4 Agent 協調層。理解它可以幫助你判斷問題發生在五層模型的哪個位置。

## 課程中會出現在哪裡

這個術語會出現在 Day 1 重新認識生成式 AI、Day 3 把自己的工作方法交給 AI 協作，用來幫助學員把實作經驗連回 AI 工作系統的概念。

## Agent 需要注意什麼

整理 prompt 或文件時，要把最重要的決策靠近當前任務，並用標題清楚標示。

## 情境例句

> 「長文件中哪一段最該放任務目標？」
>
> 「放在 smart zone：模型最容易注意並用來決策的位置，通常靠近最後指令或清楚標示的重點區。」

## 常見錯誤

- 把重點埋在長文中間。
- 在任務尾端加入互相矛盾的新要求。
- 沒有用標題或摘要強化重點。

## 相關術語

- [Attention Budget](attention-budget.md)
- [Attention Degradation](attention-degradation.md)
- [Context Window](context-window.md)
