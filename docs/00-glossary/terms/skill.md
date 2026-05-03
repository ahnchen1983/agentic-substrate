---
id: skill
term: Skill
zh: 技能
category: memory-and-steering
layers: [L3]
course_days: [day1, day3]
learning_stages: [level3]
related_terms: [spec, progressive-disclosure, subagent, automated-review]
source_inspiration:
  - mattpocock/dictionary-of-ai-coding
status: draft
---

# Skill - 技能

## 一句話

Skill 是把領域經驗、工作流程、輸入輸出格式與檢查標準封裝成可重複使用的 AI 工作單元。

## 不要誤會成

Skill 不是一句 prompt。Prompt 通常解決一次對話；Skill 保存一套可反覆執行、可交接、可驗證的工作方法。

## 為什麼重要

AI 真正進入工作，不只靠模型更強，而是靠人把專業流程說清楚。Skill 讓領域專家把「我平常怎麼做」轉成 Agent 可以遵循的結構。

## 在五層模型的位置

- L3：Skill 是五層模型中的第三層。
- L4：Agent 可以選擇、組合、執行多個 Skills。
- L5：使用者可能透過聊天、IDE、表單或課程頁建立 Skill。

## 課程中會出現在哪裡

Day 1 先讓學員知道 Skill 是新的軟體單元。Day 3 會讓學員完成自己的 AI 工作流卡，作為 Skill 的前身。

## Agent 需要注意什麼

當同類任務重複出現、流程多步驟、品質標準明確，就應該考慮建立或改進 Skill。不要把每次都重打 prompt 當成長期解法。

## 情境例句

> 「我每次都叫 AI 整理會議紀錄，這算 Skill 嗎？」
>
> 「如果只是每次重打一段 prompt，還不算。當你定義觸發條件、輸入格式、分類步驟、待辦表欄位、驗收標準與後續寄信流程，它才開始變成 Skill。」

## 常見錯誤

- 把長 prompt 當成 Skill。
- 只寫步驟，沒有輸入契約、輸出格式和驗收標準。
- 沒有版本迭代，導致壞流程被穩定重複。

## 相關術語

- [Spec](spec.md)
- [Progressive disclosure](progressive-disclosure.md)
- [Subagent](subagent.md)
- [Automated review](automated-review.md)
