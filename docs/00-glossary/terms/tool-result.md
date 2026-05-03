---
id: tool-result
term: Tool result
zh: 工具結果
category: tools-and-environment
layers: [L2, L4]
course_days: [day2, day3]
learning_stages: [level2, level4]
related_terms: [tool-call, hallucination, automated-review]
source_inspiration:
  - mattpocock/dictionary-of-ai-coding
status: draft
---

# Tool result - 工具結果

## 一句話

工具結果是工具呼叫執行後回傳給 Agent 的資料、狀態或錯誤訊息。

## 不要誤會成

工具結果不等於真相。工具可能回傳過期資料、片段資料、錯誤訊息，Agent 也可能解讀錯。

## 為什麼重要

很多 AI 錯誤不是模型亂編，而是工具結果不完整、查錯地方、或 Agent 把結果推論過頭。重要任務必須把 observation 和 inference 分開。

## 在五層模型的位置

- L2：工具結果來自工具與協議層。
- L4：Agent 負責驗證、整合、決定是否要繼續行動。

## 課程中會出現在哪裡

Day 2 的工具組合會強調「輸入 -> 工具串接 -> 輸出 -> 人工覆核點」。Day 3 則會把工具結果納入工作流卡的檢查標準。

## Agent 需要注意什麼

工具結果要先檢查風險等級。對程式碼、財務、法律、醫療、個資或公開內容，不能只看工具成功就當作任務成功。

## 範例

`git diff --check` 通過只代表沒有空白格式錯誤，不代表內容正確、連結完整或課程設計合理。Agent 還要做語意檢查。

## 相關術語

- [Tool call](tool-call.md)
- [Hallucination](hallucination.md)
- [Automated review](automated-review.md)
