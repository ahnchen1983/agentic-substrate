---
id: agent-mode
term: Agent mode
zh: 代理模式
category: tools-and-environment
layers: [L4, L5]
course_days: [day2, day3]
learning_stages: [level4]
related_terms: [agent, permission-mode, sandbox]
source_inspiration:
  - mattpocock/dictionary-of-ai-coding
status: draft
---

# Agent mode - 代理模式

## 一句話

Agent mode 是讓 AI 從回答問題轉為規劃、使用工具並執行任務的模式。

## 不要誤會成

Agent mode 不是比較會聊天的模式，而是工作權限和行為假設都改變的模式。

## 為什麼重要

使用者一旦進入 agent mode，就要開始思考檔案、工具、權限、驗證和回滾。

## 在五層模型的位置

主要對應 L4 Agent 協調層、L5 Interface 使用介面層。理解它可以幫助你判斷問題發生在五層模型的哪個位置。

## 課程中會出現在哪裡

這個術語會出現在 Day 2 AI 工具的選擇與搭配、Day 3 把自己的工作方法交給 AI 協作，用來幫助學員把實作經驗連回 AI 工作系統的概念。

## Agent 需要注意什麼

開始前要確認任務範圍、可改檔案、是否需要 approval，以及完成後要回報哪些 tool results。

## 情境例句

> 「我只是想問一個問題，為什麼工具一直要改檔？」
>
> 「可能你開的是 agent mode。它會把需求理解成可執行任務，而不只是回答問題。」

## 常見錯誤

- 不知道目前是在 chat mode 還是 agent mode。
- 沒有先限制可改檔範圍。
- 把 agent mode 用在尚未釐清的需求上。

## 相關術語

- [Agent](agent.md)
- [Permission Mode](permission-mode.md)
- [Sandbox](sandbox.md)
