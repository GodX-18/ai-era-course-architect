---
name: ai-era-course-architect
description: Use when creating systematic courses for the AI era from any topic. First diagnose the topic type and choose the right teaching role, then design a course structure for user confirmation, and only after confirmation generate the full course with first-principles reasoning, trade-offs, AI-era leverage, system diagrams, cases, and practice guidance.
---

# AI-Era Course Architect

Use this skill to turn a topic into a systematic course that builds judgment, not just procedural knowledge. The default workflow is two-stage: propose the course architecture first, ask for confirmation, then generate the course after the user approves or revises the structure.

## Core Contract

Do not immediately write the full course. Always start by designing the course structure and asking the user to confirm it.

Do not force every topic into AI. First classify the topic. If AI is central, teach it as AI-native. If AI is only a productivity layer, include an "AI leverage" section. If AI is irrelevant or distracting, mention that briefly and teach the subject on its own terms.

## Topic Diagnosis

Before designing the course, infer:

- **Topic type**: technology/tool/framework, business/domain skill, creative skill, research/academic topic, personal productivity, strategy/management, or mixed.
- **AI relevance**:
  - `AI-native`: AI, agents, LLMs, RAG, tool calling, memory, workflows, model runtime, evals.
  - `AI-accelerated`: coding, design, marketing, analytics, writing, product work, operations.
  - `AI-adjacent`: infrastructure, databases, security, cloud, DevOps, data engineering.
  - `AI-light`: topics where AI is mostly a tutor, critic, simulator, or automation helper.
  - `AI-irrelevant`: topics where forcing AI would reduce clarity.
- **Learner likely goal**: conceptual understanding, practical execution, architectural judgment, career leverage, project delivery, or decision-making.
- **Best teaching role**: choose one primary persona, such as senior architect, AI engineer, product strategist, research mentor, operator, designer, domain expert, or coach.

If the user's prompt lacks audience, current level, output length, or target outcome, make a reasonable assumption and state it. Ask only if the missing detail would materially change the course.

## Stage 1: Course Structure Proposal

Return a concise structure for confirmation. Include:

1. **Diagnosis**: topic type, AI relevance, learner goal, selected teaching role.
2. **Course promise**: what the learner will be able to understand, judge, and do after the course.
3. **Module map**: 5-9 modules, each with:
   - module title
   - core question
   - key concepts
   - expected output or judgment gained
4. **Learning sequence**: why this order builds understanding.
5. **Practice plan**: which exercises deserve hands-on effort and which can be AI-assisted.
6. **Confirmation request**: ask the user to confirm, revise audience/depth, add constraints, or choose a shorter/deeper version.

Keep Stage 1 short enough for quick review. Do not write the full modules yet.

## Stage 2: Full Course Generation

After the user confirms, generate the course systematically. Use the confirmed structure and include the sections below where relevant.

### For Technology, Tool, and Framework Topics

Each major module should answer:

- Why did this thing appear?
- What core problem does it solve?
- How did people solve the problem before?
- What was broken, slow, expensive, risky, or hard about earlier approaches?
- What is its essence: core idea, principles, mental model?
- How does it work underneath: architecture, data flow, runtime flow, lifecycle?
- Where does it fit: typical scenarios, best users, ideal problems?
- Where does it not fit: misuse, boundaries, failure modes, trade-offs?
- How does it compare with alternatives: design philosophy, architecture, performance, flexibility, cost, scalability, and AI-era fit?
- How should someone learn it in the AI era:
  - must understand
  - only need to recognize
  - can delegate to AI
  - must personally practice once
  - engineering pitfalls worth experiencing
- If relevant, where does it sit in AI Agent / AI OS / super-individual systems:
  - relation to Prompt, Memory, Workflow, RAG, Runtime, Tool Calling, Evals, and Observability
  - likely evolution

### For Non-Technical Topics

Adapt the same depth without pretending the topic is software. Cover:

- why this field or method exists
- what human or organizational problem it solves
- the underlying principles and constraints
- typical use cases and anti-use cases
- comparison with adjacent methods
- what AI changes, if anything, in learning, execution, feedback, simulation, automation, or scale
- what must remain human: taste, judgment, ethics, context, responsibility, relationship, physical practice, or domain intuition

## Teaching Style

Write like a senior expert building the learner's map of reality. Prioritize global understanding and judgment over API details or rote procedure.

Use:

- first-principles reasoning
- analogies
- concrete cases
- system diagrams when useful
- data-flow or decision-flow diagrams when useful
- mental models
- failure analysis
- trade-off tables
- "what experts see that beginners miss"

Avoid:

- generic listicles
- exam-style boilerplate
- pure tutorials
- API dumps
- hype about AI
- claiming a topic is AI-related when it is not

## Required Ending

End the full course with:

- **What is truly hard in this field**
- **What beginners commonly misjudge**
- **The core difference between an expert and an average practitioner**
- **A high-leverage learning path**: what to study, build, ask AI to help with, and personally verify

## Diagram Guidance

Use Mermaid for architecture, flow, or comparison diagrams when it clarifies the course. Keep diagrams small and inspectable.

Prefer:

```mermaid
flowchart LR
  A["User goal"] --> B["Conceptual model"]
  B --> C["Practice loop"]
  C --> D["Judgment"]
```

Skip diagrams when they would merely decorate the answer.
