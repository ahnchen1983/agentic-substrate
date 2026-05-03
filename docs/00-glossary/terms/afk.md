---
id: afk
term: AFK
zh: 離開鍵盤
category: patterns-of-work
layers: [L4]
course_days: [day3]
learning_stages: [level4]
related_terms: [agent, permission-mode, automated-review]
source_inspiration:
  - mattpocock/dictionary-of-ai-coding
status: draft
---

# AFK - 離開鍵盤

## 一句話

AFK 是讓 Agent 在人暫時離開時繼續執行一段受控任務的工作模式。

## 不要誤會成

AFK 不是完全放手不管，也不是讓 Agent 擁有無限制權限。

## 為什麼重要

它代表 AI 工作從即時聊天走向背景執行，但也更需要邊界、檢查點與回報機制。

## 在五層模型的位置

主要對應 L4 Agent 協調層。理解它可以幫助你判斷問題發生在五層模型的哪個位置。

## 課程中會出現在哪裡

這個術語會出現在 Day 3 把自己的工作方法交給 AI 協作，用來幫助學員把實作經驗連回 AI 工作系統的概念。

## Agent 需要注意什麼

只在低風險、可驗證、可中止的任務上採用 AFK；涉及外部發布、金錢、刪除或敏感資料時要要求人類確認。

## 情境例句

> 「我能不能讓 Agent 跑著，自己去吃飯？」
>
> 「可以，但只適合低風險、檢查點明確的任務。像跑測試、整理格式可以 AFK；涉及刪檔、發信、花錢或公開發布，就要有人回來確認。」

## 常見錯誤

- 把 AFK 當成完全不用管。
- 沒有設停止條件和驗收標準。
- 讓 Agent 在高風險權限下長時間自動執行。

## 相關術語

- [Agent](agent.md)
- [Permission Mode](permission-mode.md)
- [Automated Review](automated-review.md)
