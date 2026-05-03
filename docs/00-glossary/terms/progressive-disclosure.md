---
id: progressive-disclosure
term: Progressive disclosure
zh: 漸進揭露
category: memory-and-steering
layers: [cross-layer]
course_days: [day1, day3]
learning_stages: [level3, level4]
related_terms: [skill, agents-md, context-window]
source_inspiration:
  - mattpocock/dictionary-of-ai-coding
status: draft
---

# Progressive disclosure - 漸進揭露

## 一句話

Progressive disclosure 是先給 Agent 必要概要，需要時再讀詳細資料的資訊揭露方式。

## 不要誤會成

它不是藏資訊，也不是讓 Agent 自己亂猜。

## 為什麼重要

它能節省 context window，讓大型文件、skills 和 agent protocol 更容易被使用。

## 在五層模型的位置

主要對應 cross-layer。理解它可以幫助你判斷問題發生在五層模型的哪個位置。

## 課程中會出現在哪裡

這個術語會出現在 Day 1 重新認識生成式 AI、Day 3 把自己的工作方法交給 AI 協作，用來幫助學員把實作經驗連回 AI 工作系統的概念。

## Agent 需要注意什麼

概要要說清楚何時讀哪個檔案；詳細參考要有穩定路徑和明確邊界。

## 情境例句

> 「Skill 文件為什麼不要一開始塞滿所有細節？」
>
> 「progressive disclosure 會先給 Agent 短指引，需要時再讀詳細參考，節省 context。」

## 常見錯誤

- 把所有文件一次塞進 context。
- 短指引太空泛，Agent 不知道何時讀細節。
- 詳細資料沒有清楚路徑。

## 相關術語

- [Skill](skill.md)
- [Agents Md](agents-md.md)
- [Context Window](context-window.md)
