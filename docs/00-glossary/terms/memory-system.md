---
id: memory-system
term: Memory system
zh: 記憶系統
category: memory-and-steering
layers: [L4]
course_days: [day3]
learning_stages: [level4]
related_terms: [stateful, agents-md, compaction, contextual-knowledge]
source_inspiration:
  - mattpocock/dictionary-of-ai-coding
status: draft
---

# Memory system - 記憶系統

## 一句話

記憶系統是讓 Agent 在單次推論或單一工作階段之外保存、查找、更新資訊的機制。

## 不要誤會成

它不是模型自己永遠記得。大多數情況下，記憶是由檔案、資料庫、向量檢索、設定檔、摘要或專案狀態文件承載。

## 為什麼重要

沒有記憶系統，Agent 每次都要重新理解專案、重新問偏好、重新發現流程。長期工作需要明確保存 durable facts、決策理由、進度與可複用模式。

## 在五層模型的位置

- L4：記憶系統是 Agent 調度層的重要能力。
- L2：記憶通常透過檔案、資料庫或工具讀寫。
- L3：成熟的記憶可沉澱為 Skill 或 workflow。

## 課程中會出現在哪裡

Day 3 會用工作流卡說明：你的工作方法如果只存在腦中，AI 每次都要重新猜；寫成卡片、模板或 Skill，才會成為可延續的記憶。

## Agent 需要注意什麼

不要什麼都記。只保存跨 session 仍然有用的事實、規則、偏好、決策和流程。短期狀態應該留在工作記錄，不該污染長期記憶。

## 情境例句

> 「為什麼每次開新 session，AI 都要我重新解釋 repo 的方向？」
>
> 「因為它沒有可讀的記憶系統。把穩定規則寫進 `AGENTS.md`、決策寫進 decision log、工作狀態寫進專案檔，下次 Agent 才能接續。」

## 常見錯誤

- 以為模型會自然記得上次所有事。
- 把暫時狀態寫進長期記憶，讓記憶越來越髒。
- 記了結論但沒記決策理由，導致下次無法判斷是否仍適用。

## 相關術語

- [Stateful](stateful.md)
- [AGENTS.md](agents-md.md)
- [Compaction](compaction.md)
- [Contextual knowledge](contextual-knowledge.md)
