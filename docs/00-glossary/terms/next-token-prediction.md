---
id: next-token-prediction
term: Next-token prediction
zh: 下一個詞元預測
category: model
layers: [L1]
course_days: [day1]
learning_stages: [level1]
related_terms: [model, token, non-determinism, hallucination]
source_inspiration:
  - mattpocock/dictionary-of-ai-coding
status: draft
---

# Next-token prediction - 下一個詞元預測

## 一句話

Next-token prediction 是大型語言模型根據前文預測下一個 token 的基本生成機制。

## 不要誤會成

它不是說 AI 只能做文字接龍，也不等於產品層沒有規劃和工具使用。

## 為什麼重要

它提醒我們 AI 的流暢語氣不等於真實性，輸出需要驗證機制。

## 在五層模型的位置

主要對應 L1 模型層。理解它可以幫助你判斷問題發生在五層模型的哪個位置。

## 課程中會出現在哪裡

這個術語會出現在 Day 1 重新認識生成式 AI，用來幫助學員把實作經驗連回 AI 工作系統的概念。

## Agent 需要注意什麼

不要用這個概念過度簡化 Agent；要同時看模型機制與外層 harness。

## 情境例句

> 「AI 是不是先想好整篇文章？」
>
> 「底層是 next-token prediction：一步步預測下一段文字。產品層可以包上規劃和工具，但模型輸出仍是逐步生成。」

## 常見錯誤

- 用這個概念否定所有推理能力。
- 以為逐 token 生成就不能做複雜任務。
- 忽略 harness 會在生成外層加入工具與控制流程。

## 相關術語

- [Model](model.md)
- [Token](token.md)
- [Non Determinism](non-determinism.md)
- [Hallucination](hallucination.md)
