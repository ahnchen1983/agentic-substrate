---
id: agent
term: Agent
zh: 代理人
category: sessions-context-windows-and-turns
layers: [L4]
course_days: [day1, day3]
learning_stages: [level4]
related_terms: [model, harness, tool, skill, memory-system]
source_inspiration:
  - mattpocock/dictionary-of-ai-coding
status: draft
---

# Agent - 代理人

## 一句話

Agent 是能在多個步驟中追求任務、使用工具、觀察結果並調整下一步的 AI 系統。

## 不要誤會成

Agent 不是聊天機器人的新名字。聊天機器人主要回應文字；Agent 會進入任務迴圈，規劃、行動、觀察、修正，必要時還會保存狀態或交接工作。

## 為什麼重要

當 AI 開始讀檔、改檔、呼叫 API、管理記憶、拆任務、請求權限時，問題就不只是「回答得好不好」，而是「能不能安全、可控、可驗證地做事」。

## 在五層模型的位置

- L4：Agent 是調度層。
- 它會調用 L1 模型、L2 工具、L3 Skills，並透過 L5 介面和人互動。

## 課程中會出現在哪裡

Day 1 用來區分聊天工具與工作系統。Day 3 用來說明：當你的工作流卡變穩定，它就可能成為 Agent 可以調度的 Skill。

## Agent 需要注意什麼

Agent 應該知道自己目前在哪一層操作、是否需要工具、是否已有 Skill、是否需要人類覆核，以及是否該保存工作狀態。

## 情境例句

> 「這個工具說自己是 Agent，但它只是回我一段文案，算嗎？」
>
> 「不一定。Agent 至少要能跨步驟處理任務：規劃、使用工具、觀察結果、修正下一步。只有聊天輸出，通常比較像 L1 + L5。」

## 常見錯誤

- 把聊天機器人重新命名成 Agent。
- 沒有工具、記憶、驗證，卻期待它完成長流程工作。
- 忽略 Agent 需要 permission、sandbox 和 human review 才能安全運作。

## 相關術語

- [Model](model.md)
- [Harness](harness.md)
- [Tool](tool.md)
- [Skill](skill.md)
- [Memory system](memory-system.md)
