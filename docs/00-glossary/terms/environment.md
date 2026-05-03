---
id: environment
term: Environment
zh: 環境
category: tools-and-environment
layers: [L2]
course_days: [day2]
learning_stages: [level2]
related_terms: [filesystem, sandbox, permission-mode]
source_inspiration:
  - mattpocock/dictionary-of-ai-coding
status: draft
---

# Environment - 環境

## 一句話

Environment 是 Agent 執行任務時所在的環境，包括作業系統、工作目錄、工具、網路與權限。

## 不要誤會成

它不是模型本身，也不等於使用者的全部電腦。

## 為什麼重要

同一個 prompt 在不同 environment 可能能做的事完全不同。

## 在五層模型的位置

主要對應 L2 工具與環境層。理解它可以幫助你判斷問題發生在五層模型的哪個位置。

## 課程中會出現在哪裡

這個術語會出現在 Day 2 AI 工具的選擇與搭配，用來幫助學員把實作經驗連回 AI 工作系統的概念。

## Agent 需要注意什麼

動手前要確認 cwd、可用工具、sandbox、network、依賴版本和輸出位置。

## 情境例句

> 「同一個 Agent 在你電腦和 GitHub Actions 裡結果不同，為什麼？」
>
> 「environment 不同。可用檔案、網路、權限、環境變數和工具版本都可能不同。」

## 常見錯誤

- 以為模型相同就代表執行環境相同。
- 沒有記錄工具版本和限制。
- 在本機可行就直接假設 CI 也會過。

## 相關術語

- [Filesystem](filesystem.md)
- [Sandbox](sandbox.md)
- [Permission Mode](permission-mode.md)
