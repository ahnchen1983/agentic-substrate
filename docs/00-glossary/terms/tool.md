---
id: tool
term: Tool
zh: 工具
category: tools-and-environment
layers: [L2]
course_days: [day1, day2]
learning_stages: [level2]
related_terms: [tool-call, tool-result, harness]
source_inspiration:
  - mattpocock/dictionary-of-ai-coding
status: draft
---

# Tool - 工具

## 一句話

Tool 是 Agent 可以呼叫來讀資料、操作環境、查詢外部系統或產生副作用的能力。

## 不要誤會成

Tool 不是模型本身，也不是最終答案。

## 為什麼重要

工具讓 AI 從「會說」變成「能做」，是五層模型中連接世界的手腳。

## 在五層模型的位置

主要對應 L2 工具與環境層。理解它可以幫助你判斷問題發生在五層模型的哪個位置。

## 課程中會出現在哪裡

這個術語會出現在 Day 1 重新認識生成式 AI、Day 2 AI 工具的選擇與搭配，用來幫助學員把實作經驗連回 AI 工作系統的概念。

## Agent 需要注意什麼

呼叫工具前要確認目的和權限；呼叫後要閱讀 tool result，而不是假設成功。

## 情境例句

> 「AI 要怎麼知道 GitHub Actions 錯在哪？」
>
> 「它需要 tool，例如讀 log、查檔案、跑測試或呼叫 GitHub API。」

## 常見錯誤

- 把 tool 和 Agent 混在一起。
- 沒有確認工具權限和輸出。
- 期待模型憑空知道外部狀態。

## 相關術語

- [Tool Call](tool-call.md)
- [Tool Result](tool-result.md)
- [Harness](harness.md)
