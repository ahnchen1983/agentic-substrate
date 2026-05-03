---
id: context
term: Context
zh: 脈絡
category: sessions-context-windows-and-turns
layers: [L1, L4]
course_days: [day1, day3]
learning_stages: [level1, level4]
related_terms: [context-window, contextual-knowledge, system-prompt]
source_inspiration:
  - mattpocock/dictionary-of-ai-coding
status: draft
---

# Context - 脈絡

## 一句話

Context 是模型在這次回應中可見的所有資訊，包括使用者訊息、系統規則、檔案內容和工具結果。

## 不要誤會成

它不是人腦記憶，也不是模型訓練資料的全部。

## 為什麼重要

AI 的輸出高度依賴 context；同一個問題放在不同背景裡，可能得到完全不同的答案。

## 在五層模型的位置

主要對應 L1 模型層、L4 Agent 協調層。理解它可以幫助你判斷問題發生在五層模型的哪個位置。

## 課程中會出現在哪裡

這個術語會出現在 Day 1 重新認識生成式 AI、Day 3 把自己的工作方法交給 AI 協作，用來幫助學員把實作經驗連回 AI 工作系統的概念。

## Agent 需要注意什麼

回答前要分辨哪些是正式指令、哪些是背景資料、哪些是工具觀察，避免把過期資訊當成最新狀態。

## 情境例句

> 「AI 為什麼知道我們在講 Day 3？」
>
> 「因為這一輪對話、檔案內容、工具結果和系統規則一起構成 context。」

## 常見錯誤

- 把 context 只理解成前一句話。
- 忘記工具結果也會進入判斷。
- 沒有清楚區分背景資料和正式指令。

## 相關術語

- [Context Window](context-window.md)
- [Contextual Knowledge](contextual-knowledge.md)
- [System Prompt](system-prompt.md)
