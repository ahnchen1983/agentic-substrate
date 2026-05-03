---
id: agents-md
term: AGENTS.md
zh: AGENTS.md
category: memory-and-steering
layers: [L4]
course_days: [day3]
learning_stages: [level4]
related_terms: [memory-system, system-prompt, progressive-disclosure]
source_inspiration:
  - mattpocock/dictionary-of-ai-coding
status: draft
---

# AGENTS.md - AGENTS.md

## 一句話

AGENTS.md 是放在 repo 裡，讓 Agent 讀取專案規則、工作慣例和安全邊界的指引文件。

## 不要誤會成

它不是 README 的替代品，也不是把所有背景資料塞進一個檔案。

## 為什麼重要

它讓 Agent 不依賴對話歷史，也能在新 session 中重建基本工作方式。

## 在五層模型的位置

主要對應 L4 Agent 協調層。理解它可以幫助你判斷問題發生在五層模型的哪個位置。

## 課程中會出現在哪裡

這個術語會出現在 Day 3 把自己的工作方法交給 AI 協作，用來幫助學員把實作經驗連回 AI 工作系統的概念。

## Agent 需要注意什麼

讀到 AGENTS.md 後要遵守其中的 coding、testing、commit、permission 和文件規則；若規則與使用者最新指令衝突，要說明並確認。

## 情境例句

> 「為什麼新開一個 Agent 後，它還知道 repo 的寫作規則？」
>
> 「因為規則寫在 `AGENTS.md`。這類檔案讓 Agent 不靠對話歷史，也能讀到專案慣例。」

## 常見錯誤

- 把只適合單次任務的細節寫進 `AGENTS.md`。
- 規則太長、太抽象，Agent 反而抓不到重點。
- 修改規則後沒有測試實際輸出是否跟著改變。

## 相關術語

- [Memory System](memory-system.md)
- [System Prompt](system-prompt.md)
- [Progressive Disclosure](progressive-disclosure.md)
