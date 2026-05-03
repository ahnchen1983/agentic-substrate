---
id: permission-request
term: Permission request
zh: 權限請求
category: tools-and-environment
layers: [L2, L5]
course_days: [day2]
learning_stages: [level2]
related_terms: [permission-mode, tool-call, sandbox]
source_inspiration:
  - mattpocock/dictionary-of-ai-coding
status: draft
---

# Permission request - 權限請求

## 一句話

Permission request 是 Agent 在執行受限操作前向使用者提出的授權請求。

## 不要誤會成

它不是形式化通知，而是風險控制節點。

## 為什麼重要

它讓高風險操作可被人類審核，也讓責任邊界更清楚。

## 在五層模型的位置

主要對應 L2 工具與環境層、L5 Interface 使用介面層。理解它可以幫助你判斷問題發生在五層模型的哪個位置。

## 課程中會出現在哪裡

這個術語會出現在 Day 2 AI 工具的選擇與搭配，用來幫助學員把實作經驗連回 AI 工作系統的概念。

## Agent 需要注意什麼

提出請求時要說明目的、影響範圍和替代方案；批准前要確認是否符合任務。

## 情境例句

> 「Agent 問我要不要允許 push，該怎麼判斷？」
>
> 「這是 permission request。你要看它要做什麼、影響範圍、是否可回復，以及是否符合目前目標。」

## 常見錯誤

- 沒看清楚就批准。
- 讓 Agent 用模糊理由取得高權限。
- 沒有保留敏感操作的審核節點。

## 相關術語

- [Permission Mode](permission-mode.md)
- [Tool Call](tool-call.md)
- [Sandbox](sandbox.md)
