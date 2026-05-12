# Agentic Substrate Learning System SDD

Status: Draft v0.1
Date: 2026-05-12
Owner: Agentic Substrate

## 1. Purpose

This document defines how this repository evolves from a three-day course artifact into a long-term learning system for the LLM-native era.

這份 SDD 定義本 repo 如何從 Day 1/2/3 的臨時教材，發展成一套長期維護的 LLM 時代學習架構。

The core claim:

> Agentic Substrate is not a tool tutorial collection. It is a learning architecture for understanding how LLMs, tools, Skills, Agents, and interfaces form the next software substrate.

> Agentic Substrate 不是工具教學集合，而是一套學習架構：幫助人理解 LLM、工具、Skill、Agent、介面如何組成下一代軟體底層。

## 2. Problem Statement

Current AI education often teaches tools one by one:

- How to use ChatGPT.
- How to use Claude.
- How to use AI Studio.
- How to write better prompts.

This helps people start, but it does not explain the system behind the tools. Learners often know many features but cannot answer:

- Which layer am I working in?
- When should I use chat, tool use, workflow, Skill, or Agent?
- How do different AI tools complement each other?
- How do I preserve a good process so it can be reused?
- How do I validate AI output instead of trusting fluent text?

Agentic Substrate should solve this by giving people a stable conceptual map and multiple practical learning paths.

## 3. Design Thesis

The repository has two identities:

1. **Human learning system**
   A structured curriculum and knowledge base for people learning how to work in the LLM-native era.

2. **Agent-readable operating substrate**
   A set of documents, Skills, protocols, and repo conventions that help AI agents understand and execute work.

These two identities must share one architecture: the five-layer model.

## 4. Core Model

All educational content should map back to the five-layer structure:

| Layer | Human Explanation | Learning Question |
|---|---|---|
| LLM | The reasoning and generation layer | What can the model understand, infer, and generate? |
| Tools | The action layer | What external capabilities can the model call? |
| Skill / Workflow | The reusable process layer | How do we encode a repeatable way of working? |
| Agent | The orchestration layer | How does AI choose tools, run steps, check results, and continue work? |
| Interface / Substrate | The interaction and environment layer | Where does the human meet the system, and where does state live? |

中文教學版本：

| 層級 | 白話說法 | 學習問題 |
|---|---|---|
| LLM | 大腦 | 模型能理解、推理、生成什麼？ |
| Tools | 手腳 | 模型能呼叫哪些外部能力？ |
| Skill / Workflow | 肌肉記憶 | 如何把一套做事方法保存成可重用流程？ |
| Agent | 協調者 / 經理人 | AI 如何選工具、跑步驟、檢查結果、延續任務？ |
| Interface / Substrate | 入口與環境 | 人在哪裡跟系統互動？狀態與記憶放在哪裡？ |

## 5. Target Audiences

| Audience | Primary Need | Entry Point |
|---|---|---|
| General learners | Understand what AI is becoming | Day 1/2/3 course |
| Knowledge workers | Turn repeated work into workflows | Skill cards and workflow examples |
| Internal training teams | Teach AI adoption without tool chaos | Course summary and workshop materials |
| Engineers / builders | Design LLM-native systems | Architecture docs and agent education layer |
| AI agents | Read repo state and execute work safely | `AGENTS.md`, `llms.txt`, `agent-education/` |

## 6. Information Architecture

Proposed long-term structure:

```text
docs/
  00-glossary/
  01-foundations/
  02-architecture/
  03-tools/
  04-curriculum/
  05-workflows/
  06-agents/
  07-case-studies/
```

Current repo already contains most of this. The immediate expansion is:

```text
docs/03-tools/
  README.md
  chatgpt.md
  claude.md
  hermes.md
  ai-studio.md

course-summary.html
tools.html
tool-chatgpt.html
tool-claude.html
tool-hermes.html
tool-aistudio.html
```

## 7. Course Layer

The Day 1/2/3 pages should be treated as the first public course product.

### Day 1: Cognitive Shift

Theme:

> AI is not just another app. It is a new work-system entry point.

Mapped layers:

- LLM
- Interface
- Basic tool awareness

Core outcomes:

- Learners understand why AI differs from search engines and traditional apps.
- Learners understand probabilistic output and the need for validation.
- Learners see the first version of the five-layer model.

### Day 2: Tool Selection and Output

Theme:

> Tools are not brands to memorize. They are capabilities to compose.

Mapped layers:

- Tools
- Interface
- Human review

Core outcomes:

- Learners choose tools by task type, risk, freshness, and workflow complexity.
- Learners produce a concrete one-page website content package.
- Learners learn that public output requires stronger review.

### Day 3: Workflow, Skill, and Agent

Theme:

> Your expertise becomes reusable when it is written as a workflow.

Mapped layers:

- Skill / Workflow
- Agent
- Human-in-the-loop

Core outcomes:

- Learners write an AI workflow card.
- Learners test whether someone else can run their workflow.
- Learners understand the path from prompt to Skill to Agent.

## 8. Course Summary Page

Add `course-summary.html` as the canonical human-facing recap after Day 1/2/3.

It should not be a poster only. It should act as a learning bridge:

1. What changed in how we understand AI.
2. The five-layer model in one screen.
3. What each day taught.
4. The 10 beginner principles from the pasted guide, rewritten for this course.
5. Common pitfalls.
6. Next learning paths.

Proposed sections:

- Hero: `三日課程總整理：從 Chat 到 Agentic Workflow`
- Section 1: `三天學到的不是工具，而是一套系統觀`
- Section 2: `五層模型速查`
- Section 3: `Day 1 / Day 2 / Day 3 回顧`
- Section 4: `入門 10 原則`
- Section 5: `常見踩坑`
- Section 6: `下一步：工具章節、Workflow 章節、Agent 章節`

## 9. Tool Chapter

Tool pages should not be generic product reviews. Each page should explain the tool's role inside the Agentic Substrate stack.

工具介紹頁不能只是功能清單，而要回答：這個工具在五層模型裡扮演什麼角色？

### Canonical Tool Page Template

Each tool page should use the same structure:

1. What it is
2. Its position in the five-layer model
3. Best use cases
4. Weak spots / risk areas
5. Recommended workflows
6. How it pairs with other tools
7. Validation checklist
8. Beginner mode
9. Advanced mode
10. Official references and update date

### Initial Tool Pages

| Page | Role in System | Notes |
|---|---|---|
| ChatGPT | General interface + tool-using assistant | Strong for broad tasks, multimodal work, browsing/tool workflows depending on plan and setup |
| Claude | Long-form reasoning, writing, code/project collaboration | Strong for document reasoning, artifacts, coding workflows, careful synthesis |
| Hermes | Human-to-human workflow mediator / Agent archetype | A teaching concept for the Agent layer: an AI colleague that reads context, prepares handoffs between human experts, routes work across domains, asks for human review, and preserves reusable results. Not initially defined as a specific product. |
| AI Studio | Model building and experimentation environment | Should be explained as a model/workflow prototyping interface, not just a chat app |

All tool claims that may change must be sourced from official docs at implementation time.

### Hermes as Human-to-Human Workflow Mediator

Hermes is the named teaching archetype for the Agent layer. Its long-term role is not only to run tasks, but to mediate professional handoffs between humans.

Hermes assumes that humans remain domain owners:

- Each person still has a primary scope of responsibility.
- Each person still owns professional judgment in their field.
- AI should not flatten expertise into generic summaries.
- Valuable work requires context, responsibility, acceptance criteria, and professional handoff.

It should help learners answer:

- What changes when AI moves from answering to executing?
- What does it mean for an AI to carry context across steps?
- How does an Agent choose tools or Skills?
- When must the Agent stop and ask a human?
- What should be saved back into the repo, document, or workflow memory?
- How should one person's work be translated into a clear handoff for the next responsible person?
- What context, decision history, constraints, and review criteria must survive the handoff?

Hermes should be introduced after learners understand ChatGPT / Claude-style interaction. Its role is not to compete with those tools, but to explain the next layer: orchestration across people, tools, and responsibility boundaries.

In the learning system, Hermes represents a future-facing pattern:

> AI Agents become valuable when they can preserve professional context and turn one human's output into another human's actionable input.

> AI Agent 真正有價值的地方，是能保存專業脈絡，並把一個人的產出轉化成下一個專業負責人可以接手的輸入。

## 10. Practical Guide Layer

The pasted `GPT / Codex 實戰指南` should be decomposed into learning modules, not inserted as-is.

### Keep

- GPT is not a search engine.
- Work in layers.
- Define system logic before asking for output.
- Use documents as external memory.
- Separate sessions by task.
- Treat context as an asset.
- Use real data, logs, schemas, and API responses.
- Validate every output.
- Use precise terminology.
- Treat AI as a pair engineer, not a wish machine.

### Reframe

Some items are engineering-specific and should move to advanced paths:

- SDD / ADR / Schema
- Repo-first workflow
- Worktree parallel development
- MCP
- Commit / PR automation

These should not overwhelm the Day 1/2/3 beginner recap. They belong in:

- `docs/02-architecture/`
- `docs/05-workflows/`
- `agent-education/`

## 11. Website Navigation

Recommended public navigation:

```text
Home
  Start Here
  Five-Layer Model
  Three-Day Course
  Course Summary
  Tools
  Workflows
  Skills
  Agent Education
```

`course.html` should link to:

- Day 1
- Day 2
- Day 3
- Course Summary
- Tool Guide

`course-summary.html` should link forward to:

- `tools.html`
- `docs/01-foundations/five-layer-model.md`
- `docs/04-curriculum/learning-path.md`
- Skill examples

### Homepage Routing Strategy

The homepage / interactive architecture portal should break the project open with four clear entry paths:

| Audience Intent | Label | Destination |
|---|---|---|
| First-time AI learners | 第一次學 AI | `course-summary.html` |
| Architecture learners | 理解核心架構 | `#five-layers` / Five-Layer Model |
| Tool selectors | 選擇 AI 工具 | Product map now; future `tools.html` |
| Agents / developers | 給 Agent / 開發者 | `agent-education/README.md` and GitHub |

Hero CTA priority:

1. `Start with the 3-Day Summary`
2. `Understand the Five-Layer Model`
3. `Explore AI Tools & Hermes`

The homepage is the canonical architecture portal. `course-summary.html` is the first human-learning route, not a replacement for the homepage.

## 12. Content Source Policy

Because AI tools change quickly:

- Product capability claims must include an update date.
- Official docs are preferred over media summaries.
- Media articles can be used as inspiration or examples, not as canonical truth.
- Course content should describe durable usage patterns, not only temporary UI features.

Example:

```text
Updated: 2026-05-12
Source type: official docs / product page / observed course workflow
Stability: stable concept / changing product feature
```

## 13. Acceptance Criteria

This learning system is working when:

- A new learner can understand the five-layer model within 5 minutes.
- A non-engineer can explain the difference between chat, tool, workflow, Skill, and Agent.
- Day 1/2/3 have a clear summary path.
- Tool pages explain when and why to use each tool, not only what buttons exist.
- Every tool page maps back to the five-layer model.
- Hermes helps learners understand Agent as a mediator of responsibility, context, and professional handoff between humans.
- The repo supports both human learning and agent-readable execution.
- New course materials can be added without breaking the architecture.

## 14. Implementation Phases

### Phase 1: Define the Learning System

- Create this SDD.
- Review and revise terminology.
- Decide final navigation names.

### Phase 2: Build Course Summary

- Create `course-summary.html`.
- Convert the pasted guide into beginner principles, pitfalls, and next steps.
- Link it from `course.html` and `README.md`.

### Phase 3: Build Tool Chapter

- Create `docs/03-tools/README.md`.
- Create `tools.html`.
- Create tool pages for ChatGPT, Claude, Hermes, and AI Studio.
- Use official references for current product claims.

### Phase 4: Connect to Existing Architecture

- Update `docs/START-HERE.md`.
- Update `docs/04-curriculum/learning-path.md`.
- Update `llms.txt` so agents understand the new learning system.

### Phase 5: Public Polish

- Add visual route maps.
- Add examples and workshop exercises.
- Add reading paths by audience.

## 15. Open Questions

1. Hermes definition:
   - Resolved for v0.1: Hermes is an Agent-layer teaching concept and human-to-human workflow mediator, not initially a specific product.
   - Future decision: whether Hermes later becomes an internal agent implementation, a course character, or both.

2. Should tool pages be HTML-first for public reading, Markdown-first for repo maintainability, or both?

3. Should `course-summary.html` be the fourth page in the Day 1/2/3 course flow, or a separate recap page?

4. How bilingual should the new course pages be?
   - Current detailed course pages are Chinese-first.
   - Core repo docs are bilingual.

5. Should the pasted practical guide remain as a poster-style page, or be decomposed entirely into structured learning modules?

## 16. Immediate Next Step

Review this SDD with the user and resolve:

1. Final name of the learning system.
2. Final structure for `docs/03-tools/`.
3. Whether Hermes should later become an internal agent implementation, a course character, or both.
4. Whether to build `course-summary.html` first or `tools.html` first.
