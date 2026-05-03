---
id: parametric-knowledge
term: Parametric knowledge
zh: 參數知識
category: failure-modes
layers: [L1]
course_days: [day1]
learning_stages: [level1]
related_terms: [parameters, knowledge-cutoff, contextual-knowledge]
source_inspiration:
  - mattpocock/dictionary-of-ai-coding
status: draft
---

# Parametric knowledge - 參數知識

## 一句話

Parametric knowledge 是模型在訓練中吸收到並儲存在權重裡的知識。

## 不要誤會成

它不是即時查詢結果，也不是可追溯來源的資料庫。

## 為什麼重要

它能讓模型快速回答一般知識，但遇到最新或高風險內容時需要外部驗證。

## 在五層模型的位置

主要對應 L1 模型層。理解它可以幫助你判斷問題發生在五層模型的哪個位置。

## 課程中會出現在哪裡

這個術語會出現在 Day 1 重新認識生成式 AI，用來幫助學員把實作經驗連回 AI 工作系統的概念。

## Agent 需要注意什麼

要區分「模型記得」與「工具查到」；需要來源時不能只靠 parametric knowledge。

## 情境例句

> 「AI 怎麼知道一些歷史知識？」
>
> 「那可能是 parametric knowledge：訓練時被壓進模型權重裡的知識，不是現在去查到的。」

## 常見錯誤

- 把 parametric knowledge 當成最新資料。
- 無法區分模型記得的內容和工具查到的內容。
- 對需要來源的任務沒有引用外部證據。

## 相關術語

- [Parameters](parameters.md)
- [Knowledge Cutoff](knowledge-cutoff.md)
- [Contextual Knowledge](contextual-knowledge.md)
