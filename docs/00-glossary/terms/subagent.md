---
id: subagent
term: Subagent
zh: 子代理
category: memory-and-steering
layers: [L4]
course_days: [day3]
learning_stages: [level4]
related_terms: [agent, handoff, agent-mode]
source_inspiration:
  - mattpocock/dictionary-of-ai-coding
status: draft
---

# Subagent - 子代理

## 一句話

Subagent 是被主 Agent 派出來處理明確子任務的次級 Agent。

## 不要誤會成

它不是魔法分身，也不是把困難任務丟出去就會更好。

## 為什麼重要

Subagent 適合平行探索、獨立檢查或分工實作，能提升複雜任務效率。

## 在五層模型的位置

主要對應 L4 Agent 協調層。理解它可以幫助你判斷問題發生在五層模型的哪個位置。

## 課程中會出現在哪裡

這個術語會出現在 Day 3 把自己的工作方法交給 AI 協作，用來幫助學員把實作經驗連回 AI 工作系統的概念。

## Agent 需要注意什麼

派工要界定範圍、輸出格式和不可碰的檔案；回收結果時要整合與驗證。

## 情境例句

> 「可以叫另一個 Agent 同時查資料嗎？」
>
> 「可以，這就是 subagent 的典型用途：把可並行、範圍清楚的子任務交出去。」

## 常見錯誤

- 把阻塞主線的核心任務丟給 subagent。
- 多個 subagent 做重複工作。
- 沒有定義輸出格式和責任範圍。

## 相關術語

- [Agent](agent.md)
- [Handoff](handoff.md)
- [Agent Mode](agent-mode.md)
