---
id: hallucination
term: Hallucination
zh: 幻覺
category: failure-modes
layers: [L1]
course_days: [day1, day2]
learning_stages: [level1, level2]
related_terms: [knowledge-cutoff, contextual-knowledge, tool-result, human-review]
source_inspiration:
  - mattpocock/dictionary-of-ai-coding
status: draft
---

# Hallucination - 幻覺

## 一句話

幻覺是模型產生看起來流暢、但沒有根據或不正確的內容。

## 不要誤會成

幻覺不是 AI 故意說謊。模型是在生成最可能的文字，不是在保證每句話都已經被驗證。

## 為什麼重要

如果使用者把 AI 的流暢輸出當成事實，就可能做出錯誤決策。越是專業、法律、醫療、財務、資安、公開發佈內容，越需要驗證。

## 在五層模型的位置

- L1：幻覺來自模型生成的本質限制。
- L2：工具可以提供外部證據。
- L3：Skill 可以定義驗收規則。
- L4：Agent 可以建立 review loop。

## 課程中會出現在哪裡

Day 1 開場安全紅線會提到 AI 不是真理機器。Day 2 和 Day 3 會把幻覺處理轉成「人工覆核點」和「檢查標準」。

## Agent 需要注意什麼

不要用自信語氣包裝未驗證內容。需要區分「我看到的來源」、「我推論的結論」、「仍未確認的假設」。

## 範例

AI 可能幫你寫出一份很漂亮的食農教育課程頁，但如果它編造了證照、價格、合作案例或食品營養說法，就會造成信任風險。

## 相關術語

- [Knowledge cutoff](knowledge-cutoff.md)
- [Contextual knowledge](contextual-knowledge.md)
- [Tool result](tool-result.md)
- [Human review](human-review.md)
