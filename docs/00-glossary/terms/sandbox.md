---
id: sandbox
term: Sandbox
zh: 沙盒
category: tools-and-environment
layers: [L2, L4]
course_days: [day2]
learning_stages: [level2, level4]
related_terms: [environment, permission-mode, tool-call]
source_inspiration:
  - mattpocock/dictionary-of-ai-coding
status: draft
---

# Sandbox - 沙盒

## 一句話

Sandbox 是限制 Agent 執行範圍的安全環境，例如檔案、網路或命令權限。

## 不要誤會成

它不是錯誤狀態，也不是模型本身的限制。

## 為什麼重要

它讓 AI 能執行工具，同時降低誤刪、外洩或破壞系統的風險。

## 在五層模型的位置

主要對應 L2 工具與環境層、L4 Agent 協調層。理解它可以幫助你判斷問題發生在五層模型的哪個位置。

## 課程中會出現在哪裡

這個術語會出現在 Day 2 AI 工具的選擇與搭配，用來幫助學員把實作經驗連回 AI 工作系統的概念。

## Agent 需要注意什麼

遇到權限失敗時要判斷是否真的需要升權，並向使用者說明風險與目的。

## 情境例句

> 「Agent 說不能連網或不能寫某個資料夾，是壞掉嗎？」
>
> 「不一定。sandbox 是安全邊界，限制它能讀寫、執行或連線的範圍。」

## 常見錯誤

- 把 sandbox 當成模型能力不足。
- 不理解權限錯誤的安全意義。
- 為了省事關掉所有限制。

## 相關術語

- [Environment](environment.md)
- [Permission Mode](permission-mode.md)
- [Tool Call](tool-call.md)
