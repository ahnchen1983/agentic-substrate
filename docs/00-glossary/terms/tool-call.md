---
id: tool-call
term: Tool call
zh: 工具呼叫
category: tools-and-environment
layers: [L2]
course_days: [day1, day2]
learning_stages: [level2]
related_terms: [tool, tool-result, permission-request, sandbox]
source_inspiration:
  - mattpocock/dictionary-of-ai-coding
status: draft
---

# Tool call - 工具呼叫

## 一句話

工具呼叫是 Agent 向外部工具提出的結構化操作請求。

## 不要誤會成

它不是最終答案，也不是模型「自己真的去做了」。工具呼叫通常由 harness 解析、檢查權限、執行工具，再把工具結果送回模型。

## 為什麼重要

Tool call 讓 AI 的行動變得可控、可記錄、可稽核。你可以知道它呼叫了什麼、拿到什麼結果、下一步如何推論。

## 在五層模型的位置

- L2：工具呼叫是工具與協議層的核心動作。
- L4：Agent 決定何時需要工具呼叫，以及如何解讀結果。

## 課程中會出現在哪裡

Day 1 用來說明「大腦有了手腳」。Day 2 用來說明工具組合不是清單，而是一串可驗證的行動流程。

## Agent 需要注意什麼

不要為了看起來勤奮而亂呼叫工具。每次 tool call 都應該有目的、權限判斷、結果解讀和必要驗證。

## 範例

使用者問「repo 裡 Day 2 的生成有沒有接 API？」Agent 不應該憑感覺回答，而應該讀 `course-day2.html`，搜尋 `fetch`、`api`、`openai` 等關鍵字，這就是工具呼叫。

## 相關術語

- [Tool](tool.md)
- [Tool result](tool-result.md)
- [Permission request](permission-request.md)
- [Sandbox](sandbox.md)
