---
id: automated-review
term: Automated review
zh: 自動審查
category: patterns-of-work
layers: [L3, L4]
course_days: [day2, day3]
learning_stages: [level3, level4]
related_terms: [automated-check, human-review, hallucination]
source_inspiration:
  - mattpocock/dictionary-of-ai-coding
status: draft
---

# Automated review - 自動審查

## 一句話

Automated review 是由 AI 或工具輔助檢視程式碼、文件或流程風險的審查方式。

## 不要誤會成

它不是最終批准，也不是取代負責人的簽核。

## 為什麼重要

它可以快速找到遺漏、矛盾和風險，特別適合 PR、規格和 agent protocol 的初步審查。

## 在五層模型的位置

主要對應 L3 Skill 與可重複工作流層、L4 Agent 協調層。理解它可以幫助你判斷問題發生在五層模型的哪個位置。

## 課程中會出現在哪裡

這個術語會出現在 Day 2 AI 工具的選擇與搭配、Day 3 把自己的工作方法交給 AI 協作，用來幫助學員把實作經驗連回 AI 工作系統的概念。

## Agent 需要注意什麼

要把 findings 分成確定問題、可能風險和建議；高風險項目仍要 human review。

## 情境例句

> 「我想讓 AI 幫我看 PR，可以直接相信嗎？」
>
> 「automated review 可以抓風險和遺漏，但它是第二雙眼睛，不是最後責任人。」

## 常見錯誤

- 把 automated review 當成正式批准。
- 沒有區分建議、風險和確定 bug。
- 對高風險改動缺少人類覆核。

## 相關術語

- [Automated Check](automated-check.md)
- [Human Review](human-review.md)
- [Hallucination](hallucination.md)
