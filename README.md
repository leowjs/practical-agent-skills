# Practical Agent Skills

A field guide to agent skills and companion tools for coding, testing AI apps, working with knowledge graphs, and producing visual explainers. Each entry says when it is useful and what kind of project it is.

## Where to start

- **I want my coding agent to make smaller, verifiable changes.** Try Karpathy Guidelines for everyday work. Use Superpowers when a feature benefits from design and planning before implementation. [Karpathy Guidelines](https://github.com/multica-ai/andrej-karpathy-skills) · [Superpowers](https://github.com/obra/superpowers)
- **I’m writing a system prompt for a web app agent.** Start with Prompt Engineering Patterns. Give it the agent’s purpose, tools, permissions, and expected output. Use Promptfoo to check whether later edits change behaviour. [Prompt Engineering Patterns](https://github.com/wshobson/agents/blob/main/plugins/llm-application-dev/skills/prompt-engineering-patterns/SKILL.md) · [Promptfoo](https://github.com/promptfoo/promptfoo)
- **I need to understand an unfamiliar codebase.** Use Graphify to trace a real path, then check the important relationships against the source. [Graphify](https://github.com/Graphify-Labs/graphify)
- **I need to explain a product or process visually.** Use Animation Production Skills to choose a format and style, then develop a storyboard or an animation. [Animation Production Skills](https://github.com/leowjs/animation-production-skills)

## Coding and creative workflows

| Project | Type | When it earns its place | Stars | Source |
| --- | --- | --- | ---: | --- |
| **Karpathy Guidelines** | Skill / project rules | State assumptions, make focused edits, and verify the result. Start here for a lightweight coding baseline. | 230,559 | [GitHub](https://github.com/multica-ai/andrej-karpathy-skills) |
| **Superpowers** | Skill suite | Guide a larger feature from brainstorming and design through implementation and verification. | 314,011 | [GitHub](https://github.com/obra/superpowers) |
| **wshobson Agents** | Skill collection | Pick a specialist workflow. Start with Prompt Engineering Patterns to draft or revise a system message for a web app agent. | 42,281 | [GitHub](https://github.com/wshobson/agents) |
| **Animation Production Skills** | Skill suite | Choose an animation style and build a visual explainer, short video, or interactive browser story. Maintained by the author of this guide. | 0 | [GitHub](https://github.com/leowjs/animation-production-skills) |

## Evaluation and skill security

| Project | Type | When it earns its place | Stars | Source |
| --- | --- | --- | ---: | --- |
| **Promptfoo** | Evaluation toolkit | Compare prompt or model versions with repeatable checks. Try a normal request, missing context, a tool failure, and an access-boundary case. | 26,936 | [GitHub](https://github.com/promptfoo/promptfoo) |
| **NVIDIA SkillSpector** | Security scanner | Inspect a third-party skill bundle before enabling it. Review the findings and check what the scan actually covered. | 24,784 | [GitHub](https://github.com/NVIDIA/SkillSpector) |

## Knowledge, memory, and analytics

| Project | Type | When it earns its place | Stars | Source |
| --- | --- | --- | ---: | --- |
| **Graphify** | Skill + indexing tool | Map a codebase and its docs. Start here when you need to trace a feature to its dependencies, data, or tests. | 143,899 | [GitHub](https://github.com/Graphify-Labs/graphify) |
| **Graphiti** | Agent memory framework | Keep track of facts and relationships that change over time. Try asking for a current value and then its earlier value. | 32,625 | [GitHub](https://github.com/getzep/graphiti) |
| **Microsoft GraphRAG** | Document retrieval framework | Index a document collection for questions that need evidence or themes from several documents. | 36,589 | [GitHub](https://github.com/microsoft/graphrag) |
| **NVIDIA Auto Ontology** | Semantic layer + skills | Define business measures and relationships, then verify the SQL and results an agent generates against known answers. | 9,695 | [GitHub](https://github.com/NVIDIA/auto-ontology) |

## Multi-agent simulation

| Project | Type | When it earns its place | Stars | Source |
| --- | --- | --- | ---: | --- |
| **MiroFish** | Simulation application | Explore how simulated stakeholders might respond to a change. Use the results as hypotheses to check with real users. | 84,634 | [GitHub](https://github.com/666ghj/MiroFish) |
| **CAMEL OASIS** | Simulation framework | Write custom experiments for interactions among agents. Choose it when you want control over the simulation in code. | 5,403 | [GitHub](https://github.com/camel-ai/oasis) |

GitHub star counts were checked on **8 November 2026**. They are a snapshot of popularity. The descriptions explain the trade-offs that matter for choosing a project.

## How to evaluate a skill

1. Read its description and instructions. Check that they fit a task you repeat. For two skills with overlapping descriptions, choose one for the job or invoke your preferred one by name. [Claude Code skills](https://code.claude.com/docs/en/skills) · [Codex skills](https://learn.chatgpt.com/docs/build-skills)
2. Review any scripts, tools, and dependencies before enabling the skill. A scanner can help identify what to inspect. [SkillSpector](https://github.com/NVIDIA/SkillSpector)
3. Try it on a small task with a clear success criterion. Keep it if the result, verification evidence, or time spent improves.

Use each linked project’s documentation for installation, prerequisites, and licensing.
