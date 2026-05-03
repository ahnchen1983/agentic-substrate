---
id: model
term: Model
zh: 模型
category: model
layers: [L1]
course_days: [day1]
learning_stages: [level1]
related_terms: [parameters, training, inference, harness]
source_inspiration:
  - mattpocock/dictionary-of-ai-coding
status: draft
---

# Model - 模型

## 一句話

模型是接收輸入、進行推論、產生輸出的已訓練系統。

## 不要誤會成

模型不是完整的 AI 產品。ChatGPT、Claude Code、Cursor、Codex 這些體驗都不只是模型，還包含介面、工具、權限、記憶、系統提示詞與執行環境。

## 為什麼重要

很多人會把「模型能力」和「產品能力」混在一起。實際上，同一個模型放在不同 harness 裡，能做的事可能完全不同。模型負責推理，但它本身不會讀你的檔案、不會自己按按鈕，也不會自動記住你的專案狀態。

## 在五層模型的位置

- L1：模型是 LLM 運算層的核心。
- L2-L5：工具、Skill、Agent、介面會決定模型能接觸什麼、能做什麼、怎麼被使用。

## 課程中會出現在哪裡

Day 1 會用來說明「AI 不是 App，而是新的運算層」。學員需要先知道：模型只是大腦，工作系統還需要手腳、流程、調度和介面。

## Agent 需要注意什麼

不要把任務失敗直接歸因於模型不夠強。先檢查 context、tool access、permission、Skill definition、validation loop 和 interface constraints。

## 情境例句

> 「這個任務要不要換成更強的模型？」
>
> 「可以測，但先不要只怪模型。這次失敗看起來比較像工具權限、上下文和檢查流程沒設好。模型是大腦，外面的 harness 也會決定它能不能做事。」

## 常見錯誤

- 把產品能力全部歸因於模型能力。
- 以為換更強模型就能解決缺工具、缺資料、缺流程的問題。
- 忽略同一個模型在不同介面和權限下會有完全不同的表現。

## 相關術語

- [Parameters](parameters.md)
- [Training](training.md)
- [Inference](inference.md)
- [Harness](harness.md)
