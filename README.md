# Practical Agent Skills

A field guide to agent skills and companion tools for coding, testing AI apps, working with knowledge graphs, and producing visual explainers. Each entry says when it is useful and what kind of project it is.

[Set up the skills, plugins, Python libraries, and video tools on Windows](WINDOWS-SETUP.md).

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
| **Vercel React Best Practices and Web Design Guidelines** | Agent skills | Review React and Next.js apps for slow loading, unnecessary re-renders, keyboard accessibility, and form usability. | 33,701 | [React Best Practices](https://github.com/vercel-labs/agent-skills/tree/main/skills/react-best-practices) · [Web Design Guidelines](https://github.com/vercel-labs/agent-skills/tree/main/skills/web-design-guidelines) |
| **Vercel use-ai-sdk** | Agent skill | Build TypeScript AI features with streamed responses, tool calls, structured outputs, and React chat interfaces. | 27,806 | [Skill](https://github.com/vercel/ai/blob/main/skills/use-ai-sdk/SKILL.md) |
| **FastAPI official skill** | Agent skill | Build Python API endpoints with validated models, stream AI responses, and keep generated frontend clients aligned with OpenAPI. | 104,560 | [Skill](https://github.com/fastapi/fastapi/blob/master/fastapi/.agents/skills/fastapi/SKILL.md) · [Setup](https://fastapi.tiangolo.com/ai-development/) |
| **Context7 find-docs** | Agent skill + CLI | Look up current library APIs and examples while coding, then check them against the project's dependency version. | 64,340 | [Skill setup](https://github.com/upstash/context7/blob/master/docs/clients/cli.mdx) |
| **Anthropic Build MCP Server** | Agent skill | Design MCP tool schemas, choose a deployment model, and scaffold a server in Python or Node. Designed for Claude Code. | 46,403 | [Skill](https://github.com/anthropics/claude-plugins-official/blob/main/plugins/mcp-server-dev/skills/build-mcp-server/SKILL.md) |
| **Microsoft Azure Diagnostics** | Agent skill | Investigate errors and latency in Azure-hosted apps using authorized logs, metrics, and service-specific diagnostic steps. | 1,627 | [Skill](https://github.com/microsoft/azure-skills/blob/main/skills/azure-diagnostics/SKILL.md) |
| **Supabase Postgres Best Practices** | Agent skill | Review PostgreSQL schemas, queries, indexes, connection pooling, and row-level security for app backends. | 3,029 | [Skill](https://github.com/supabase/agent-skills/tree/main/skills/supabase-postgres-best-practices) |
| **Excalidraw Diagram** | Agent skill | Turn an architecture or process into an editable diagram, then render a preview to catch overlaps and spacing issues. | 5,216 | [GitHub](https://github.com/coleam00/excalidraw-diagram-skill) |
| **Anthropic Doc Coauthoring** | Agent skill | Draft technical handovers and design documents in stages, then test whether a fresh reader can answer key questions from the draft. | 189,039 | [Skill](https://github.com/anthropics/skills/blob/main/skills/doc-coauthoring/SKILL.md) |
| **Animation Production Skills** | Skill suite | Choose an animation style and build a visual explainer, short video, or interactive browser story. Maintained by the author of this guide. | 0 | [GitHub](https://github.com/leowjs/animation-production-skills) |
| **Remotion Agent Skills** | Skill collection | Produce rendered videos with reusable React scenes, route animations, and captions. | 6,567 | [GitHub](https://github.com/remotion-dev/skills) |
| **Microsoft VibeVoice** | Speech models | Generate single-speaker English narration or draft timestamped captions from recorded speech. | 56,733 | [GitHub](https://github.com/microsoft/VibeVoice) |

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
| **Google BigQuery Optimization** | Agent skill | Review costly queries and compare partitioning, clustering, or materialized views for a BigQuery workload. | 23,582 | [Skill](https://github.com/google/skills/blob/main/skills/cloud/bigquery-optimization/SKILL.md) |
| **Docling** | Agent skill + document library | Extract text and tables from PDFs, scans, and Office files. Check the structure against the source before indexing documents for retrieval. | 70,277 | [Skill](https://github.com/docling-project/docling/blob/main/docling/.agents/skills/docling/SKILL.md) |
| **OpenAI Jupyter Notebooks** | Agent skill | Build reproducible Python or SQL notebooks and verify conclusions against executed outputs. Part of the Codex Data Analytics plugin. | 7,812 | [Skill](https://github.com/openai/plugins/blob/main/plugins/data-analytics/skills/jupyter-notebooks/SKILL.md) |
| **Developing with Streamlit** | Agent skill | Build interactive Python data apps with controls, charts, and filters. The skill ships with Streamlit. | 46,270 | [Skill](https://github.com/streamlit/streamlit/blob/develop/lib/streamlit/.agents/skills/developing-with-streamlit/SKILL.md) · [Setup](https://docs.streamlit.io/develop/api-reference/cli/skills) |

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
| **NVIDIA Omniverse — Realtime Viewer** | Agent skill | Build an interactive OpenUSD viewer with camera controls and object selection. Use it to let people click a warehouse zone and see operational measures joined from a separate data source. | 3,891 | [Official skill](https://github.com/NVIDIA/skills/blob/main/skills/omniverse-realtime-viewer/SKILL.md) |
| **NVIDIA cuOpt — Multi-Objective Exploration** | Agent skill | Compare feasible plans across competing objectives through repeated optimization solves. Use it to explore how fewer late departures trade off against overtime after the planning problem is defined. | 3,891 | [Official skill](https://github.com/NVIDIA/skills/blob/main/skills/cuopt-multi-objective-exploration/SKILL.md) |

Use OpenUSD for the 3D scene and Fabric for operational records. Match them with stable zone or asset IDs. In Power BI, show zone utilization and exceptions with Deneb, and use Azure Maps for paths between sites. Treat cuOpt as an optional step when the question shifts from seeing shipment activity to planning new routes.

## Finance and accounting

| Project | Type | When it earns its place | Stars | Source |
| --- | --- | --- | ---: | --- |
| **Anthropic Knowledge Work Plugins — Finance & Accounting** | Claude Code and Cowork plugin | Reconcile inventory valuation with the general ledger, explain variances, or coordinate month-end close. The plugin includes the reconciliation skill. | 35,159 | [Finance plugin](https://github.com/anthropics/knowledge-work-plugins/blob/main/finance/README.md) · [Reconciliation skill](https://github.com/anthropics/knowledge-work-plugins/blob/main/finance/skills/reconciliation/SKILL.md) |

For Claude Code, install the finance plugin from the Knowledge Work Plugins marketplace.

```bash
claude plugin marketplace add anthropics/knowledge-work-plugins
claude plugin install finance@knowledge-work-plugins
```

## Data science and AutoML

| Project | Type | When it earns its place | Stars | Source |
| --- | --- | --- | ---: | --- |
| **Anthropic Data — explore-data** | Agent skill | Guide a first pass on a dataset, including column types, missing values, duplicates, distributions, and suspicious values. Included in Anthropic’s Data plugin for Claude Code. | 35,160 | [Official source](https://github.com/anthropics/knowledge-work-plugins/blob/main/data/skills/explore-data/SKILL.md) · [Data plugin and Claude Code installation](https://github.com/anthropics/knowledge-work-plugins/blob/main/data/README.md) |
| **FG Data Profiling** | Library | Generate a repeatable data profiling report for a new extract. The old YData Profiling GitHub link redirects to this repository. | 13,755 | [Official source](https://github.com/Data-Centric-AI-Community/fg-data-profiling) |
| **Microsoft FLAML** | Library | Search model and parameter options within a time budget. Use it to establish a Fabric notebook baseline and track trials with MLflow. | 4,417 | [Official source](https://github.com/microsoft/FLAML) · [Microsoft Fabric AutoML guide](https://learn.microsoft.com/en-us/fabric/data-science/automated-machine-learning-fabric) |
| **AutoGluon** | Library | Train a second AutoML benchmark for tabular prediction or time-series forecasting. Compare results on the same validation split and metric as the baseline. | 10,819 | [Official source](https://github.com/autogluon/autogluon) |
| **K-Dense Statistical Power and Experimental Design** | Agent skills | Estimate the sample size needed to detect a meaningful effect, then design how to assign units to test and control groups. Use them before collecting data for a pilot. | 56,441 | [Statistical Power](https://github.com/K-Dense-AI/scientific-agent-skills/blob/main/skills/statistical-power/SKILL.md) · [Experimental Design](https://github.com/K-Dense-AI/scientific-agent-skills/blob/main/skills/experimental-design/SKILL.md) |

Profile the dataset first. Then define the prediction target, the baseline, and the validation split before using AutoML. For a forecast or a prediction made at a specific point in a workflow, test on a later period and use only inputs available when the prediction would be made.

## Career and interview skills

| Project | Type | When it earns its place | Stars | Source |
| --- | --- | --- | ---: | --- |
| **Career Ops** | Job search framework | Discover openings, assess role fit, and track applications and follow-ups. Includes workflows for interview preparation and reviewing written offers. | 81,004 | [GitHub](https://github.com/career-ops-hq/career-ops) |
| **AI Job Search** | Job search framework | Evaluate a job description, tailor a CV and cover letter, and prepare for interviews. Use it to build an application packet for a specific role. | 70,354 | [GitHub](https://github.com/ai-job-search-dev/ai-job-search) |
| **Reactive Resume — Career Plugin** | Plugin | Draft or tailor a CV, practise a mock interview, and prepare for offer negotiation. Includes a data résumé skill that distinguishes offline evaluation from production results. | 45,468 | [GitHub](https://github.com/reactive-resume/reactive-resume/tree/main/plugins/reactive-resume) |
| **Interview Coach Skill** | Agent skill | Run role-specific drills and mock interviews with rubric feedback. Build a reusable story bank, debrief real interviews, and rehearse negotiation conversations. | 2,500 | [GitHub](https://github.com/noamseg/interview-coach-skill) |

## Multi-agent simulation

| Project | Type | When it earns its place | Stars | Source |
| --- | --- | --- | ---: | --- |
| **MiroFish** | Simulation application | Explore how simulated stakeholders might respond to a change. Use the results as hypotheses to check with real users. | 84,634 | [GitHub](https://github.com/666ghj/MiroFish) |
| **CAMEL OASIS** | Simulation framework | Write custom experiments for interactions among agents. Choose it when you want control over the simulation in code. | 5,403 | [GitHub](https://github.com/camel-ai/oasis) |

GitHub star counts were checked on **8 November 2026**. They are a snapshot of popularity. Skill and plugin rows show the star count of the repository that contains them. The descriptions explain the trade-offs that matter for choosing a project.

## How to evaluate a skill

1. Read its description and instructions. Check that they fit a task you repeat. For two skills with overlapping descriptions, choose one for the job or invoke your preferred one by name. [Claude Code skills](https://code.claude.com/docs/en/skills) · [Codex skills](https://learn.chatgpt.com/docs/build-skills)
2. Review any scripts, tools, and dependencies before enabling the skill. A scanner can help identify what to inspect. [SkillSpector](https://github.com/NVIDIA/SkillSpector)
3. Try it on a small task with a clear success criterion. Keep it if the result, verification evidence, or time spent improves.

Use each linked project’s documentation for installation, prerequisites, and licensing.
