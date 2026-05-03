---
id: context-window
term: Context window
zh: 脈絡視窗
category: sessions-context-windows-and-turns
layers: [L1, L4]
course_days: [day1, day3]
learning_stages: [level1, level4]
related_terms: [context, token, attention-budget, compaction]
source_inspiration:
  - mattpocock/dictionary-of-ai-coding
status: draft
---

# Context window - 脈絡視窗

## 一句話

脈絡視窗是模型在一次推論中能看見的資訊範圍。

## 不要誤會成

它不是長期記憶，也不是 AI 永遠知道的東西。超出脈絡視窗的內容，模型在當下就不能可靠使用。

## 為什麼重要

Agent 的能力很大一部分取決於它當下看得到什麼。如果需求、檔案、工具結果、過去決策或限制沒有進入 context，模型就可能漏看、誤判或重新發明已經做過的事。

## 在五層模型的位置

- L1：脈絡視窗是模型推論的輸入邊界。
- L4：Agent 需要透過檔案、記憶、摘要、檢索與 compaction 管理這個邊界。

## 課程中會出現在哪裡

Day 1 用來說明 AI 不是全知。Day 3 用來說明為什麼工作流卡要清楚列出輸入、步驟、檢查標準和前後流程。

## Agent 需要注意什麼

先判斷哪些資訊必須進 context，哪些應該留在檔案中按需讀取。長任務要建立 checkpoint，不要依賴對話歷史自然保留。

## 範例

如果你叫 AI「照我們上次的格式寫」，但那個格式已經不在 context 裡，它可能會憑印象猜。把格式寫進 `AGENTS.md` 或模板檔會更穩。

## 相關術語

- [Context](context.md)
- [Token](token.md)
- [Attention budget](attention-budget.md)
- [Compaction](compaction.md)
