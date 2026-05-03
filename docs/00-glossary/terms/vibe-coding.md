---
id: vibe-coding
term: Vibe coding
zh: 氛圍編程
category: patterns-of-work
layers: [L5]
course_days: [day2]
learning_stages: [level2, level3]
related_terms: [human-in-the-loop, tool-call, automated-review]
source_inspiration:
  - mattpocock/dictionary-of-ai-coding
status: draft
---

# Vibe coding - 氛圍編程

## 一句話

Vibe coding 是用自然語言和 AI 快速探索、生成或修改程式的工作方式。

## 不要誤會成

它不是不用理解程式，也不是可以不 review、不測試。

## 為什麼重要

它很適合原型和探索，但若要進入產品，就必須補上規格、測試和維護結構。

## 在五層模型的位置

主要對應 L5 Interface 使用介面層。理解它可以幫助你判斷問題發生在五層模型的哪個位置。

## 課程中會出現在哪裡

這個術語會出現在 Day 2 AI 工具的選擇與搭配，用來幫助學員把實作經驗連回 AI 工作系統的概念。

## Agent 需要注意什麼

接受 AI 改動前要讀 diff、跑檢查，並逐步把成功做法轉成 spec 或 Skill。

## 情境例句

> 「我跟 AI 說大概想要什麼，讓它一路寫，這就是 vibe coding 嗎？」
>
> 「是，但要小心。適合探索和原型，不適合沒有測試、沒有 review 的正式交付。」

## 常見錯誤

- 把 vibe coding 當成不用懂程式。
- 沒有讀 diff 就直接接受。
- 原型一路長成產品卻沒有補規格和測試。

## 相關術語

- [Human In The Loop](human-in-the-loop.md)
- [Tool Call](tool-call.md)
- [Automated Review](automated-review.md)
