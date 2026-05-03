---
id: attention-budget
term: Attention budget
zh: 注意力預算
category: failure-modes
layers: [L1, L4]
course_days: [day1, day3]
learning_stages: [level1, level4]
related_terms: [context-window, attention-degradation, smart-zone]
source_inspiration:
  - mattpocock/dictionary-of-ai-coding
status: draft
---

# Attention budget - 注意力預算

## 一句話

Attention budget 是模型在有限 context 中能有效關注資訊的注意力資源。

## 不要誤會成

它不是 token 數的同義詞；context 放得下，不代表模型都會用得好。

## 為什麼重要

長文件、長對話和大量工具結果會競爭注意力，影響模型是否抓到真正重要的限制。

## 在五層模型的位置

主要對應 L1 模型層、L4 Agent 協調層。理解它可以幫助你判斷問題發生在五層模型的哪個位置。

## 課程中會出現在哪裡

這個術語會出現在 Day 1 重新認識生成式 AI、Day 3 把自己的工作方法交給 AI 協作，用來幫助學員把實作經驗連回 AI 工作系統的概念。

## Agent 需要注意什麼

要把目標、限制、已決策事項和驗收標準放在清楚位置，必要時摘要和重排 context。

## 情境例句

> 「我把所有資料都貼給 AI，為什麼答案反而變差？」
>
> 「因為注意力是有限資源。context window 很大不代表每個細節都會被同等重視。」

## 常見錯誤

- 認為資料越多一定越好。
- 沒有把最重要的限制和目標放在前面。
- 長任務中沒有定期摘要與重申決策。

## 相關術語

- [Context Window](context-window.md)
- [Attention Degradation](attention-degradation.md)
- [Smart Zone](smart-zone.md)
