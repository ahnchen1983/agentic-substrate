---
id: filesystem
term: Filesystem
zh: 檔案系統
category: tools-and-environment
layers: [L2]
course_days: [day2, day3]
learning_stages: [level2, level4]
related_terms: [environment, tool, agents-md]
source_inspiration:
  - mattpocock/dictionary-of-ai-coding
status: draft
---

# Filesystem - 檔案系統

## 一句話

Filesystem 是檔案與資料夾構成的工作空間，Agent 透過工具在其中讀寫專案內容。

## 不要誤會成

它不是模型記憶，也不代表 Agent 可以讀取整台電腦。

## 為什麼重要

對 coding agent 來說，repo 裡的檔案通常比對話歷史更可靠，是可持續記憶的主要載體。

## 在五層模型的位置

主要對應 L2 工具與環境層。理解它可以幫助你判斷問題發生在五層模型的哪個位置。

## 課程中會出現在哪裡

這個術語會出現在 Day 2 AI 工具的選擇與搭配、Day 3 把自己的工作方法交給 AI 協作，用來幫助學員把實作經驗連回 AI 工作系統的概念。

## Agent 需要注意什麼

讀寫檔案前要確認路徑、權限和是否有使用者未提交變更；不要覆蓋不相關改動。

## 情境例句

> 「Agent 說它讀不到檔案，是它不會讀嗎？」
>
> 「不一定。可能檔案不在 workspace、權限不足，或 sandbox 不允許讀取。」

## 常見錯誤

- 以為 Agent 能讀整台電腦。
- 沒有確認工作目錄。
- 把檔案系統權限和模型能力混在一起。

## 相關術語

- [Environment](environment.md)
- [Tool](tool.md)
- [Agents Md](agents-md.md)
