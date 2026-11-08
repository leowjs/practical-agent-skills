# Practical Agent Skills

A field guide to agent skills and companion tools for coding, testing AI apps, working with knowledge graphs, and producing visual explainers. Each entry says when it is useful and what kind of project it is.

## Where to start

- **I want my coding agent to make smaller, verifiable changes.** Try Karpathy Guidelines for everyday work. Use Superpowers when a feature benefits from design and planning before implementation. [Karpathy Guidelines](https://github.com/multica-ai/andrej-karpathy-skills) · [Superpowers](https://github.com/obra/superpowers)
- **I’m writing a system prompt for a web app agent.** Start with Prompt Engineering Patterns. Give it the agent’s purpose, tools, permissions, and expected output. Use Promptfoo to check whether later edits change behaviour. [Prompt Engineering Patterns](https://github.com/wshobson/agents/blob/main/plugins/llm-application-dev/skills/prompt-engineering-patterns/SKILL.md) · [Promptfoo](https://github.com/promptfoo/promptfoo)
- **I need to understand an unfamiliar codebase.** Use Graphify to trace a real path, then check the important relationships against the source. [Graphify](https://github.com/Graphify-Labs/graphify)
- **I need to explain a product or process visually.** Use Animation Production Skills to choose a format and style, then develop a storyboard or an animation. [Animation Production Skills](https://github.com/leowjs/animation-production-skills)
- **I need to visualize warehouse operations.** Start with a report that flags busy staging zones and affected shipments. Add OpenUSD when the warehouse layout helps users locate an exception. [Warehouse and supply chain visualization](#warehouse-and-supply-chain-visualization)

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

## Warehouse and supply chain visualization

| Project | Type | When it earns its place | Stars | Source |
| --- | --- | --- | ---: | --- |
| **OpenUSD** | Library | Core 3D scene description for the warehouse layout. Use it to represent racks, aisles, staging zones, and loading bays, and assign stable asset identifiers that can be matched to operational data. | 7,623 | [Official source](https://github.com/PixarAnimationStudios/OpenUSD) |
| **NVIDIA USD Authoring** | Agent skill | Official NVIDIA instructions for creating, converting, and validating OpenUSD scenes with the OpenUSD Exchange SDK. The star count is for the SDK repository. | 91 | [Official source](https://github.com/NVIDIA-Omniverse/usd-exchange/blob/main/.agents/skills/usd-authoring/SKILL.md) |
| **Microsoft Fabric Digital Twin Builder** | Fabric platform feature | Model warehouse locations, assets, and processes and connect those relationships to operational data in Fabric. Microsoft labels the feature as preview. | — | [Official source](https://learn.microsoft.com/en-us/fabric/real-time-intelligence/digital-twin-builder/overview) |
| **Azure Maps Path Layer for Power BI** | Power BI visual feature | Display geographic paths between plants, distribution centres, and customers in Power BI. Use route IDs and ordered points to draw paths, with shipment measures for analysis. | — | [Official source](https://learn.microsoft.com/en-us/azure/azure-maps/power-bi-visual-add-path-layer) |
| **Deneb** | Power BI custom visual | Power BI custom visual for building report charts with Vega or Vega-Lite. Use it for warehouse zone utilization, staging exceptions, or other views that need a custom layout. | 316 | [Official source](https://github.com/deneb-viz/deneb) |
| **Vega-Lite** | Library | Declarative chart language and compiler supported by Deneb. Use it to express chart encodings, layers, and interactions as reusable specifications. | 5,546 | [Official source](https://github.com/vega/vega-lite) |
| **NVIDIA Agent Skills** | Skill collection | Official NVIDIA skill collection for workflows across NVIDIA tools. The cuopt-routing-api-python skill helps formulate and run a route-planning problem with the cuOpt Python API. | 3,891 | [Official source](https://github.com/NVIDIA/skills) |
| **NVIDIA cuOpt** | Library | GPU-accelerated optimization engine for vehicle routing and numerical optimization. Consider it for planning with delivery windows and capacity constraints once the business rules are defined. | 1,103 | [Official source](https://github.com/NVIDIA/cuopt) |
| **NVIDIA USD Optimize — run-validators** | Agent skill | Check an OpenUSD scene for validation issues and review the report before sharing the scene. Use it after authoring or converting a warehouse layout. | 38 | [Official skill](https://github.com/NVIDIA-Omniverse/usd-optimize/blob/main/.agents/skills/run-validators/SKILL.md) |
| **NVIDIA USD Search — search** | Agent skill | Search an indexed OpenUSD asset catalog by text, image, or both. Use it to find reusable racks, pallets, and other warehouse assets. | 27 | [Official skill](https://github.com/NVIDIA-Omniverse/usd-search/blob/main/skills/search/SKILL.md) |
| **NVIDIA cuOpt — Numerical Optimization Formulation** | Agent skill | Translate a planning question into decision variables, an objective, and constraints. Use it to define a problem such as bay assignment before selecting a solver. | 3,891 | [Official skill](https://github.com/NVIDIA/skills/blob/main/skills/cuopt-numerical-optimization-formulation/SKILL.md) |

Use OpenUSD for the 3D scene and Fabric for operational records. Match them with stable zone or asset IDs. In Power BI, show zone utilization and exceptions with Deneb, and use Azure Maps for paths between sites. Treat cuOpt as an optional step when the question shifts from seeing shipment activity to planning new routes.

## Multi-agent simulation

| Project | Type | When it earns its place | Stars | Source |
| --- | --- | --- | ---: | --- |
| **MiroFish** | Simulation application | Explore how simulated stakeholders might respond to a change. Use the results as hypotheses to check with real users. | 84,634 | [GitHub](https://github.com/666ghj/MiroFish) |
| **CAMEL OASIS** | Simulation framework | Write custom experiments for interactions among agents. Choose it when you want control over the simulation in code. | 5,403 | [GitHub](https://github.com/camel-ai/oasis) |

GitHub star counts were checked on **8 November 2026**. They are a snapshot of popularity. Skill rows show the star count of the repository that contains the skill. The descriptions explain the trade-offs that matter for choosing a project.

## How to evaluate a skill

1. Read its description and instructions. Check that they fit a task you repeat. For two skills with overlapping descriptions, choose one for the job or invoke your preferred one by name. [Claude Code skills](https://code.claude.com/docs/en/skills) · [Codex skills](https://learn.chatgpt.com/docs/build-skills)
2. Review any scripts, tools, and dependencies before enabling the skill. A scanner can help identify what to inspect. [SkillSpector](https://github.com/NVIDIA/SkillSpector)
3. Try it on a small task with a clear success criterion. Keep it if the result, verification evidence, or time spent improves.

Use each linked project’s documentation for installation, prerequisites, and licensing.
