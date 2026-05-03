---
id: system-prompt
term: System prompt
zh: 系統提示詞
category: sessions-context-windows-and-turns
layers: [L1, L4]
course_days: [day1, day3]
learning_stages: [level1, level4]
related_terms: [context, harness, agents-md]
source_inspiration:
  - mattpocock/dictionary-of-ai-coding
status: draft
---

# System prompt - 系統提示詞

## 一句話

系統提示詞是用來設定 AI 行為、角色、限制和操作規則的高優先級指令。

## 不要誤會成

它不是一般使用者 prompt。使用者可能看不到完整系統提示詞，但它會深刻影響 AI 的回答方式、工具使用規則和安全邊界。

## 為什麼重要

同一個模型在不同系統提示詞下會像不同產品。coding agent 的系統提示詞可能要求它讀檔、遵守 repo 規範、使用工具、避免破壞使用者改動。

## 在五層模型的位置

- L1：系統提示詞會進入模型 context。
- L4：它定義 Agent 的工作方式與治理規則。
- L5：它影響使用者看到的互動風格。

## 課程中會出現在哪裡

Day 1 可用來說明「AI 回答不是自然發生，而是被設計出來」。Day 3 可延伸到 Skill 和工作流卡：你不是只寫 prompt，而是在設計可重複的行為規則。

## Agent 需要注意什麼

系統提示詞不是萬能保證。它仍然受 context、工具權限、模型限制和外部環境影響。重要流程要搭配 validation rules。

## 範例

同一句「幫我整理這份文件」，在一般聊天介面可能得到摘要；在 coding agent 裡可能先讀檔、檢查格式、產出 patch，因為系統提示詞和工具環境不同。

## 相關術語

- [Context](context.md)
- [Harness](harness.md)
- [AGENTS.md](agents-md.md)
