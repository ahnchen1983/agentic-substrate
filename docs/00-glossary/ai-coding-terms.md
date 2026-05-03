# AI Coding Terms for Agentic Substrate
# Agentic Substrate 的 AI Coding 術語地圖

> Inspired by Matt Pocock's [Dictionary of AI Coding](https://github.com/mattpocock/dictionary-of-ai-coding).
> This document does not reproduce the original dictionary. It reframes selected terms through the Agentic Substrate five-layer model.
>
> 受 Matt Pocock 的 [Dictionary of AI Coding](https://github.com/mattpocock/dictionary-of-ai-coding) 啟發。
> 本文件不重製原始字典，而是把關鍵術語放回 Agentic Substrate 五層模型中重新解釋。

---

## Why This Exists - 為什麼需要這份術語地圖

AI coding is difficult partly because the field is full of terms that sound familiar but carry new architectural meaning.

AI coding 難，有時候不是因為技術本身，而是因為名詞看起來熟悉，背後卻藏著新的架構意義。

For example:

- A **context window** is not just "context." It defines what the model can see in one inference.
- An **agent** is not just a chatbot. It plans, calls tools, interacts with an environment, and may persist state.
- A **tool call** is not just "using a tool." In an agent system, it becomes part of a controlled, auditable execution flow.

先把名詞拆開，後面的架構才會清楚。

---

## How to Read This Glossary - 怎麼讀

Each term uses the same structure:

每個術語都用同一種格式：

- **One-line definition**: the plain-language meaning.
- **Not the same as**: common confusion to avoid.
- **Why it matters**: what breaks if you misunderstand it.
- **Where it sits in Agentic Substrate**: how it maps to LLM, Tool, Skill, Agent, and Interface layers.

---

## Quick Layer Map - 五層速查

| Layer | Name | What belongs here |
|---|---|---|
| L1 | LLM Computation | Model, token, inference, context window, hallucination |
| L2 | Tool / Protocol | Tool, tool call, tool result, permission, sandbox |
| L3 | Skill | Skill, spec, workflow, validation criteria |
| L4 | Agent | Agent, memory system, handoff, subagent, human-in-the-loop |
| L5 | Interface | Chat UI, IDE, CLI, coding assistant, collaboration surface |

---

## The Model - 模型相關

### Model

**One-line definition**: The trained system that receives input and predicts useful output.

**Not the same as**: The whole AI product. ChatGPT, Claude Code, Cursor, and Codex are not only models; they include interfaces, tools, memory, policies, and runtime behavior.

**Why it matters**: Many capability differences come from the harness around the model, not only from the model itself.

**Agentic Substrate layer**: L1 LLM Computation.

---

### Token

**One-line definition**: A unit of text the model reads and generates.

**Not the same as**: A word. One word may be one token, several tokens, or part of a token depending on the tokenizer.

**Why it matters**: Tokens affect cost, context length, latency, and how much information can fit into a single interaction.

**Agentic Substrate layer**: L1 LLM Computation.

---

### Next-Token Prediction

**One-line definition**: The model generates output by repeatedly predicting the next likely token.

**Not the same as**: A database lookup or deterministic program execution.

**Why it matters**: This explains why LLM output is probabilistic, why wording matters, and why validation is required for important work.

**Agentic Substrate layer**: L1 LLM Computation.

---

### Inference

**One-line definition**: The act of running the model on a given input to produce output.

**Not the same as**: Training. Training changes the model; inference uses the trained model.

**Why it matters**: Most application behavior happens around inference: constructing context, calling tools, validating results, and deciding what to do next.

**Agentic Substrate layer**: L1 LLM Computation, coordinated by L4 Agent behavior.

---

### Harness

**One-line definition**: The runtime wrapper that turns a raw model into a usable AI system.

**Not the same as**: The model itself.

**Why it matters**: The same model can feel weak in a plain chat box and powerful inside a coding agent because the harness provides tools, files, permissions, memory, and task flow.

**Agentic Substrate layer**: Cross-layer concept spanning L2 Tool, L4 Agent, and L5 Interface.

---

## Context and Session - 脈絡與工作階段

### Context

**One-line definition**: The information given to the model for a particular inference.

**Not the same as**: Permanent memory.

**Why it matters**: The model can only reason from what is present in the current context plus what it learned during training.

**Agentic Substrate layer**: L1 LLM Computation, managed by L4 Agent.

---

### Context Window

**One-line definition**: The maximum amount of context the model can see in one inference.

**Not the same as**: Long-term memory or project knowledge.

**Why it matters**: If important information falls outside the context window, the model cannot use it reliably. Long contexts also introduce cost and attention-management problems.

**Agentic Substrate layer**: L1 LLM Computation; managed through L4 memory and retrieval strategies.

---

### System Prompt

**One-line definition**: High-priority instructions that shape how the AI should behave.

**Not the same as**: A user prompt. It usually has stronger influence and may be hidden from the user.

**Why it matters**: It defines roles, rules, safety boundaries, tool behavior, and the operating style of the agent.

**Agentic Substrate layer**: L4 Agent behavior expressed through L1 context.

---

### Session

**One-line definition**: A bounded working period between a user and an AI system.

**Not the same as**: Memory. A session may include history, but that history may be compacted, lost, or summarized.

**Why it matters**: Agents need explicit state files, memory systems, or retrieval strategies when work must continue across sessions.

**Agentic Substrate layer**: L4 Agent and L5 Interface.

---

### Turn

**One-line definition**: One exchange in a conversation or agent loop.

**Not the same as**: A whole task. Complex work may require many turns, tool calls, and checkpoints.

**Why it matters**: Good agent design distinguishes between a single response and a multi-turn workflow.

**Agentic Substrate layer**: L5 Interface event, processed through L1 and L4.

---

## Agents and Tools - Agent 與工具

### Agent

**One-line definition**: An AI system that can pursue a task across steps by reasoning, using tools, observing results, and adjusting its next action.

**Not the same as**: A chatbot with a nicer name.

**Why it matters**: Agents require task planning, tool access, permissions, validation, memory, and sometimes handoffs.

**Agentic Substrate layer**: L4 Agent.

---

### Tool

**One-line definition**: A capability the AI can call to act outside pure text generation.

**Not the same as**: A model capability. Writing an answer is LLM generation; reading a file, searching the web, running code, or editing a document is tool use.

**Why it matters**: Tools turn a model from "can talk about work" into "can operate on work."

**Agentic Substrate layer**: L2 Tool / Protocol.

---

### Tool Call

**One-line definition**: A structured request from the agent to use a tool.

**Not the same as**: The final answer. It is an intermediate action in an execution loop.

**Why it matters**: Tool calls create auditable steps: what was requested, what was allowed, what returned, and what the agent inferred from it.

**Agentic Substrate layer**: L2 Tool / Protocol, orchestrated by L4 Agent.

---

### Tool Result

**One-line definition**: The output returned by a tool call.

**Not the same as**: Verified truth.

**Why it matters**: A tool can return outdated data, partial data, errors, or output that the agent misinterprets. Tool results need validation before important use.

**Agentic Substrate layer**: L2 Tool / Protocol; validated through L4 Agent behavior.

---

### Sandbox

**One-line definition**: A controlled environment where the agent can execute actions with limited access and reduced risk.

**Not the same as**: Full permission to the user's machine or accounts.

**Why it matters**: Safe agent systems need boundaries. Sandboxes make execution safer, more inspectable, and easier to recover from.

**Agentic Substrate layer**: L2 Tool / Protocol and L4 Agent safety.

---

### Permission Mode

**One-line definition**: The rules controlling what an agent can do automatically and what requires user approval.

**Not the same as**: Trust. Even trusted agents need explicit permission boundaries.

**Why it matters**: Permission design is the difference between helpful automation and unsafe automation.

**Agentic Substrate layer**: L2 Tool / Protocol, L4 Agent governance, L5 Interface prompts.

---

## Reliability and Limits - 可靠性與限制

### Hallucination

**One-line definition**: A fluent but unsupported or incorrect model output.

**Not the same as**: Lying. The model is generating likely text, not intentionally deceiving.

**Why it matters**: Hallucination risk is why important outputs need source checks, tool validation, and human review.

**Agentic Substrate layer**: L1 LLM Computation; mitigated by L2 tools, L3 validation rules, and L4 review loops.

---

### Knowledge Cutoff

**One-line definition**: The point after which the model's training data may not include newer information.

**Not the same as**: The current date, live web access, or project state.

**Why it matters**: Current facts require browsing, APIs, files, or other tools. The model's internal knowledge may be stale.

**Agentic Substrate layer**: L1 limitation mitigated by L2 tools.

---

### Contextual Knowledge

**One-line definition**: Knowledge supplied in the current context rather than learned during model training.

**Not the same as**: Built-in model knowledge.

**Why it matters**: Many useful agents work by feeding the model the right contextual knowledge at the right time.

**Agentic Substrate layer**: L1 context managed by L4 Agent memory and retrieval.

---

### Attention Degradation

**One-line definition**: The model may use some parts of a long context less reliably than others.

**Not the same as**: Forgetting in the human sense.

**Why it matters**: More context is not always better. Agents need summaries, indexes, retrieval, and carefully structured state.

**Agentic Substrate layer**: L1 limitation managed by L4 Agent context strategy.

---

## Handoffs and Work Packages - 交接與工作包

### Handoff

**One-line definition**: Passing work from one agent, human, session, or system to another.

**Not the same as**: A casual chat summary.

**Why it matters**: Good handoffs preserve intent, state, decisions, constraints, open questions, and next actions.

**Agentic Substrate layer**: L4 Agent orchestration and L5 collaboration interface.

---

### Spec

**One-line definition**: A structured description of what should be built, changed, or executed.

**Not the same as**: A vague request.

**Why it matters**: Agents perform better when goals, constraints, inputs, outputs, and acceptance criteria are explicit.

**Agentic Substrate layer**: L3 Skill input contract and L4 planning.

---

### Ticket

**One-line definition**: A task package with enough information for someone or some agent to act.

**Not the same as**: A title or reminder.

**Why it matters**: Good tickets reduce ambiguity, make work delegable, and create clean handoff boundaries.

**Agentic Substrate layer**: L4 Agent orchestration, often surfaced through L5 tools like issue trackers.

---

### Compaction

**One-line definition**: Compressing conversation or state so an agent can continue within limited context.

**Not the same as**: Perfect memory.

**Why it matters**: Compaction preserves continuity but can lose nuance. Durable facts should be written into explicit memory or project files.

**Agentic Substrate layer**: L4 memory and context management.

---

## Memory and Steering - 記憶與引導

### Memory System

**One-line definition**: A way for an agent to preserve and retrieve information beyond a single inference or session.

**Not the same as**: The model remembering everything by itself.

**Why it matters**: Persistent work requires durable facts, decision logs, project state, and retrieval paths.

**Agentic Substrate layer**: L4 Agent.

---

### AGENTS.md

**One-line definition**: A repository-level instruction file for coding agents.

**Not the same as**: General documentation for humans only.

**Why it matters**: It gives agents local operating guidance: project thesis, conventions, contribution priorities, and what to avoid.

**Agentic Substrate layer**: L4 Agent steering expressed through L2 file context.

---

### Progressive Disclosure

**One-line definition**: Revealing only the information needed at the current step, with paths to deeper detail when needed.

**Not the same as**: Hiding important context.

**Why it matters**: Agents and humans both get worse when overloaded. Good docs and Skills route attention deliberately.

**Agentic Substrate layer**: Cross-layer design principle for L3 Skills, L4 memory, and L5 interfaces.

---

### Skill

**One-line definition**: A reusable workflow unit that encodes domain expertise, process steps, and validation rules.

**Not the same as**: A clever prompt.

**Why it matters**: Skills let domain experts teach agents how work should be done repeatedly.

**Agentic Substrate layer**: L3 Skill.

---

### Subagent

**One-line definition**: A specialized or delegated agent working on a bounded part of a larger task.

**Not the same as**: More intelligence by default.

**Why it matters**: Subagents help when roles are distinct and handoff contracts are clear. They add coordination cost when used too early.

**Agentic Substrate layer**: L4 Agent orchestration.

---

## Patterns of Work - 工作模式

### Human-in-the-Loop

**One-line definition**: A workflow where humans review, approve, correct, or steer AI actions at important points.

**Not the same as**: Manual work replacing AI.

**Why it matters**: Human review is essential for high-risk, ambiguous, relational, or trust-sensitive work.

**Agentic Substrate layer**: L4 governance and L5 interface.

---

### Automated Review

**One-line definition**: Using AI or tools to inspect outputs before they are accepted.

**Not the same as**: Guaranteed correctness.

**Why it matters**: Review loops improve quality, but their criteria and failure handling must be explicit.

**Agentic Substrate layer**: L3 validation and L4 evaluator-optimizer loops.

---

### AFK

**One-line definition**: Letting an agent continue work while the human is away.

**Not the same as**: Unlimited autonomy.

**Why it matters**: AFK work requires safe permissions, checkpoints, clear goals, and recovery plans.

**Agentic Substrate layer**: L4 Agent orchestration with L2 permission controls.

---

### Vibe Coding

**One-line definition**: Building software through high-level intent, rapid AI-generated changes, and frequent human steering.

**Not the same as**: No engineering judgment.

**Why it matters**: Vibe coding can accelerate exploration, but production work still needs architecture, tests, review, and maintainability.

**Agentic Substrate layer**: L5 interaction style powered by L1-L4 capabilities.

---

### Grilling

**One-line definition**: Pressing the AI with follow-up questions to expose assumptions, gaps, and weak reasoning.

**Not the same as**: Being adversarial for its own sake.

**Why it matters**: Good grilling turns a fluent answer into a more reliable answer by forcing clarification and evidence.

**Agentic Substrate layer**: L5 interaction pattern that strengthens L1 reasoning and L4 validation.

---

## Minimal Vocabulary for Beginners - 初學者最小詞彙包

If you only learn ten terms first, learn these:

如果你先只學十個，先學這些：

1. Model
2. Token
3. Context Window
4. System Prompt
5. Agent
6. Tool Call
7. Tool Result
8. Hallucination
9. Memory System
10. Skill

These ten terms explain why AI systems behave so differently across chat apps, coding agents, workflow tools, and persistent collaborators.

這十個詞可以幫你理解：為什麼同樣是 AI，在聊天工具、coding agent、工作流工具、長期協作者裡，表現會完全不同。
