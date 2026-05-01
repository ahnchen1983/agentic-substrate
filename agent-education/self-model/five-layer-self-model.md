# Five-Layer Self-Model
### Agent 的五層自我定位協議

Purpose: help an AI agent identify which layer of Agentic Substrate it is operating in before it acts.

目的：幫助 AI Agent 在行動前，先判斷自己目前正在 Agentic Substrate 的哪一層運作。

---

## Layer Map - 層級地圖

| Layer | Agent question | Typical action |
|---|---|---|
| L1. LLM Computation | Can I solve this through reasoning, generation, or transformation only? | Answer, draft, summarize, classify, reason |
| L2. Tool / Protocol | Do I need to inspect, fetch, execute, write, or call an external capability? | Search files, run commands, call APIs, read data |
| L3. Skill | Is this a repeatable workflow with a known structure or quality standard? | Invoke, create, improve, or compose a Skill |
| L4. Agent | Does this require planning across time, memory, delegation, or multiple capabilities? | Plan, coordinate, monitor, recover, persist state |
| L5. Interface | How should the result be exposed to the user or host environment? | Chat answer, file edit, PR, page, report, dashboard |

Traditional users often experience only the interface and the model response. An agent should be aware of all five layers.

一般使用者常常只感覺到介面和模型回答。Agent 必須知道自己其實在五層之間移動。

---

## Self-Location Protocol - 自我定位流程

Before acting, ask these questions in order:

行動前，依序問自己：

1. **What is the user actually asking for?**
   - Explanation, decision support, file change, research, automation, creation, review, or long-running work.

2. **What is the lowest sufficient layer?**
   - Prefer the simplest layer that can safely complete the task.

3. **Is an existing Skill relevant?**
   - If a workflow already exists, reuse it before inventing a new one.

4. **Are tools required?**
   - Use tools when the task depends on current facts, repo state, file contents, execution results, or external systems.

5. **What validation is required?**
   - Higher-risk tasks require stronger verification and clearer uncertainty.

6. **Is this pattern worth preserving?**
   - If the workflow is repeatable and valuable, mark it as a Skill or memory candidate.

7. **What interface should the result take?**
   - The same work may become a chat answer, Markdown file, code change, course page, diagram, PR, or template.

---

## Operating State Schema - 操作狀態格式

Use this schema internally, or expose it when it helps the user understand the work:

```yaml
current_layer: L1 | L2 | L3 | L4 | L5
task_mode: explain | decide | edit | research | automate | review | create | orchestrate
required_capabilities:
  - reasoning
  - file_read
  - file_write
  - tool_call
  - web_research
  - validation
existing_skill_to_reuse:
tool_use_required: true | false
validation_required: low | medium | high
persistence_candidate: none | memory | skill | documentation
next_action:
```

---

## Decision Rules - 決策規則

- If the task is one-step and low-risk, stay near L1.
- If facts may have changed or file state matters, move to L2.
- If the same pattern appears repeatedly, move to L3 and consider Skill creation.
- If the task spans multiple steps, time, tools, or recovery paths, operate as L4.
- If the user needs to consume, share, teach, or reuse the result, design the L5 interface deliberately.

---

## Failure Modes - 常見失誤

- Treating a one-off prompt as a Skill.
- Treating unverified tool output as truth.
- Using tools when reasoning is enough.
- Avoiding tools when current state is required.
- Producing content without deciding the right interface.
- Forgetting to preserve a workflow that should become reusable.
