---
id: token
term: Token
zh: 詞元
category: model
layers: [L1]
course_days: [day1, day2]
learning_stages: [level1, level2]
related_terms: [input-tokens, output-tokens, context-window]
source_inspiration:
  - mattpocock/dictionary-of-ai-coding
status: draft
---

# Token - 詞元

## 一句話

詞元是模型讀取與產生文字時使用的基本單位。

## 不要誤會成

詞元不等於一個中文字、一個英文單字或一個字元。不同模型和 tokenizer 會用不同方式切分文字。

## 為什麼重要

成本、速度、上下文視窗大小和輸出長度通常都用 token 計算。當你把很多文件塞進 prompt，或讓 agent 反覆呼叫工具時，token 會快速累積。

## 在五層模型的位置

- L1：token 是模型推論的基本計量。
- L4：Agent 需要管理 context、摘要和檔案讀取策略，避免 token 浪費。

## 課程中會出現在哪裡

Day 1 可以用來解釋模型如何「逐步生成」。Day 2 可以用來解釋為什麼長流程、多工具和反覆生成會有成本。

## Agent 需要注意什麼

不要把整個 repo、整份逐字稿或所有工具結果一次塞進 context。先找出任務需要的片段，再讀取精準內容。

## 範例

一份很長的會議逐字稿直接丟進 AI，可能消耗大量 input tokens。更好的做法是先切段摘要，再把關鍵摘要和待辦表交給下一步。

## 相關術語

- [Input tokens](input-tokens.md)
- [Output tokens](output-tokens.md)
- [Context window](context-window.md)
