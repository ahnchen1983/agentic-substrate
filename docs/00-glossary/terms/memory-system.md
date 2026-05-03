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

## 範例

`AGENTS.md` 可以記錄 repo 的寫作風格、貢獻優先順序和不能做的事。下一次 Agent 進來時先讀它，就不必重學整個專案。

## 相關術語

- [Stateful](stateful.md)
- [AGENTS.md](agents-md.md)
- [Compaction](compaction.md)
- [Contextual knowledge](contextual-knowledge.md)
