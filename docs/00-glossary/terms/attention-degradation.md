---
id: attention-degradation
term: Attention degradation
zh: 注意力衰退
category: failure-modes
layers: [L1, L4]
course_days: [day1, day3]
learning_stages: [level1, level4]
related_terms: [context-window, attention-budget, compaction]
source_inspiration:
  - mattpocock/dictionary-of-ai-coding
status: draft
---

# Attention degradation - 注意力衰退

## 一句話

Attention degradation 是長任務中模型逐漸失焦、遺漏早期限制或受雜訊干擾的現象。

## 不要誤會成

它不是單純的 hallucination，也不一定代表模型變弱。

## 為什麼重要

它解釋了為什麼長工作流需要 checkpoint、摘要、狀態檔和清楚的 handoff artifact。

## 在五層模型的位置

主要對應 L1 模型層、L4 Agent 協調層。理解它可以幫助你判斷問題發生在五層模型的哪個位置。

## 課程中會出現在哪裡

這個術語會出現在 Day 1 重新認識生成式 AI、Day 3 把自己的工作方法交給 AI 協作，用來幫助學員把實作經驗連回 AI 工作系統的概念。

## Agent 需要注意什麼

發現輸出偏離時，要重新整理目前狀態、移除過期資訊，並重申不可破壞的決策。

## 情境例句

> 「前面講得很清楚，後面怎麼開始偏題？」
>
> 「這可能是 attention degradation。資訊太長、目標太多或中途插入太多工具結果時，模型會逐漸失焦。」

## 常見錯誤

- 把失焦全部怪成模型變笨。
- 沒有在長任務中建立階段性摘要。
- 讓過期資訊留在 context 裡干擾新判斷。

## 相關術語

- [Context Window](context-window.md)
- [Attention Budget](attention-budget.md)
- [Compaction](compaction.md)
