---
id: permission-mode
term: Permission mode
zh: 權限模式
category: tools-and-environment
layers: [L2, L4]
course_days: [day2]
learning_stages: [level2, level4]
related_terms: [permission-request, sandbox, agent-mode]
source_inspiration:
  - mattpocock/dictionary-of-ai-coding
status: draft
---

# Permission mode - 權限模式

## 一句話

Permission mode 是控制 Agent 哪些操作可直接執行、哪些需要使用者批准的權限模式。

## 不要誤會成

它不是單純的安全提示，也不是模型能力設定。

## 為什麼重要

它決定 AI 工作能否安全地從建議走向執行。

## 在五層模型的位置

主要對應 L2 工具與環境層、L4 Agent 協調層。理解它可以幫助你判斷問題發生在五層模型的哪個位置。

## 課程中會出現在哪裡

這個術語會出現在 Day 2 AI 工具的選擇與搭配，用來幫助學員把實作經驗連回 AI 工作系統的概念。

## Agent 需要注意什麼

根據任務風險選擇權限；涉及寫檔、刪除、網路、push 或金錢時要提高審慎度。

## 情境例句

> 「為什麼這次 Agent 改檔前會先問我？」
>
> 「因為 permission mode 控制它什麼動作可直接做、什麼動作要先取得授權。」

## 常見錯誤

- 把 permission mode 當成煩人的彈窗。
- 為了方便開太高權限。
- 沒有依任務風險調整模式。

## 相關術語

- [Permission Request](permission-request.md)
- [Sandbox](sandbox.md)
- [Agent Mode](agent-mode.md)
