# AI Coding Glossary
# AI Coding 術語知識庫

> A modular glossary for Agentic Substrate.
> This glossary is inspired by Matt Pocock's [Dictionary of AI Coding](https://github.com/mattpocock/dictionary-of-ai-coding), but terms are reframed through the Agentic Substrate five-layer model.
>
> Agentic Substrate 的模組化術語知識庫。
> 本術語庫受 Matt Pocock 的 [Dictionary of AI Coding](https://github.com/mattpocock/dictionary-of-ai-coding) 啟發，但會用 Agentic Substrate 五層模型重新整理。

---

## Start Here - 從這裡開始

- [Development Workflow](DEVELOPMENT-WORKFLOW.md): how this glossary should be expanded and validated.
- [Current Overview Draft](ai-coding-terms.md): the current single-page glossary draft.
- [Registry](glossary.registry.yaml): the canonical term index for humans, agents, and future RAG workflows.
- [By Layer](maps/by-layer.md): terms mapped to the five-layer model.
- [By Course Day](maps/by-course-day.md): terms mapped to Day 1 / Day 2 / Day 3.
- [By Learning Stage](maps/by-learning-stage.md): terms mapped to the L1-L4 learning path.

---

## Why Modular Terms - 為什麼要拆成獨立術語

The glossary is designed as a knowledge system, not a single article.

這份術語庫被設計成知識系統，不是單篇文章。

Each term should eventually have its own page so that:

- course pages can link to exact terms;
- five-layer model pages can reference terms without repeating definitions;
- agent-facing protocols can load only the terms they need;
- future AI agents can use the registry as a small index before reading deeper pages;
- context windows stay manageable as the knowledge base grows.

每個術語未來都會有獨立頁面，讓課程、五層模型、Agent 協議與未來 RAG 流程都能穩定引用。

---

## Current Status - 目前狀態

| Asset | Status | Purpose |
|---|---|---|
| `ai-coding-terms.md` | Draft | Single-page overview, later becomes the summary page |
| `glossary.registry.yaml` | Draft | Canonical index of all selected terms |
| `maps/by-layer.md` | Draft | Layer-to-term map |
| `maps/by-course-day.md` | Draft | Course-to-term map |
| `maps/by-learning-stage.md` | Draft | Learning-stage-to-term map |
| `terms/` | Seeded | One page per term, with scenario and common-mistake sections |

---

## Rule of Thumb - 經驗法則

When adding new learning content, do not explain every term inline.

新增學習內容時，不要把每個術語都塞在正文裡解釋。

Instead:

1. identify the terms the content depends on;
2. link to existing term pages;
3. add missing terms to the registry;
4. update maps only when course, layer, or learning-stage relationships change.

---

## Term Page Learning Pattern - 術語頁學習格式

Each term page should eventually include:

- a short definition;
- what not to confuse it with;
- why it matters;
- where it sits in the five-layer model;
- where it appears in the course;
- what an agent should watch for;
- a dialogue-style scenario;
- common mistakes;
- related terms.

The scenario is important. A term becomes easier to learn when readers can hear how it appears in real work.

情境例句很重要。術語一旦被放進真實工作對話裡，讀者就比較容易知道它到底怎麼用。
