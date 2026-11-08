# Set up the skills and tools on another Windows laptop

This guide sets up the public skills, plugins, Python libraries, and video tools for Codex Desktop, Codex CLI, Claude Desktop Code mode, and Claude Code CLI. Use your private Notion **Work & Life → Skills Inbox** to find saved resources and device notes.

## 1. Install the clients and prerequisites

Install [Codex Desktop and CLI](https://developers.openai.com/codex/), [Claude Desktop](https://claude.ai/downloads), and [Claude Code](https://code.claude.com/docs/en/setup). Sign in to each client you use. In Claude Desktop, choose **Code → This computer**. In a terminal, use `claude auth login` for Claude Code CLI if needed.

Open PowerShell 7. Install any missing prerequisites with Winget and then reopen the terminal.

```powershell
winget install --id Git.Git --exact
winget install --id OpenJS.NodeJS.LTS --exact
winget install --id astral-sh.uv --exact
winget install --id Gyan.FFmpeg --exact
git --version
node --version
uv --version
ffmpeg -version
ffprobe -version
```

## 2. Install the public portable skills

Install each skill group into the user skill folders for both coding clients. The `--skill` values are the skill names declared by the upstream files.

```powershell
function Add-AgentSkills {
    param([string]$Repo, [string[]]$Names)
    npx --yes skills add $Repo --skill @Names --agent codex claude-code --global --yes --copy --full-depth
    if ($LASTEXITCODE -ne 0) { throw "Skill installation failed for $Repo" }
}

Add-AgentSkills 'multica-ai/andrej-karpathy-skills' @('karpathy-guidelines')
Add-AgentSkills 'anthropics/skills' @('doc-coauthoring')
Add-AgentSkills 'wshobson/agents' @('data-storytelling', 'prompt-engineering-patterns')
Add-AgentSkills 'K-Dense-AI/scientific-agent-skills' @('experimental-design', 'statistical-power')
Add-AgentSkills 'google/skills' @('bigquery-basics', 'bigquery-ai-ml', 'bigquery-optimization', 'datalineage-summary', 'datalineage-bigquery-asset-impact-analysis')
Add-AgentSkills 'microsoft/azure-skills' @('azure-diagnostics')
Add-AgentSkills 'microsoft/playwright-cli' @('playwright-cli')
Add-AgentSkills 'fastapi/fastapi' @('fastapi')
Add-AgentSkills 'docling-project/docling' @('docling')
Add-AgentSkills 'streamlit/streamlit' @('developing-with-streamlit')
Add-AgentSkills 'vercel-labs/agent-skills' @('vercel-react-best-practices', 'web-design-guidelines')
Add-AgentSkills 'vercel/ai' @('ai-sdk')
Add-AgentSkills 'supabase/agent-skills' @('supabase-postgres-best-practices')
Add-AgentSkills 'upstash/context7' @('find-docs')
Add-AgentSkills 'remotion-dev/skills' @('remotion-maps', 'remotion-captions', 'remotion-render', 'remotion-markup', 'remotion-studio')
Add-AgentSkills 'coleam00/excalidraw-diagram-skill' @('excalidraw-diagram')
Add-AgentSkills 'noamseg/interview-coach-skill' @('interview-coach')
Add-AgentSkills 'NVIDIA/skills' @('cuopt-multi-objective-exploration', 'cuopt-numerical-optimization-formulation', 'cuopt-routing-api-python', 'omniverse-realtime-viewer')
Add-AgentSkills 'NVIDIA/auto-ontology' @('nvidia-ontology-management', 'nvidia-ontology-query', 'nvidia-ontology-setup')
Add-AgentSkills 'NVIDIA-Omniverse/usd-exchange' @('usd-authoring')
Add-AgentSkills 'NVIDIA-Omniverse/usd-optimize' @('run-validators')
Add-AgentSkills 'NVIDIA-Omniverse/usd-search' @('search')

uv tool install --python 3.12 graphifyy
graphify install --platform codex
graphify install --platform windows
```

For Animation Production Skills, use the [v1.1.0 release and installation instructions](https://github.com/leowjs/animation-production-skills/blob/v1.1.0/README.md#install). Keep all five folders together in each client’s skills directory so their reference links work. Invoke `$video-production` in Codex or `/video-production` in Claude Code.

If the installer cannot discover a skill, open its upstream link in the [catalog](README.md) or Notion and copy the folder containing `SKILL.md` and its supporting files to `$env:USERPROFILE/.agents/skills` for Codex or `$env:USERPROFILE/.claude/skills` for Claude. Streamlit also provides its own [skill installer](https://docs.streamlit.io/develop/api-reference/cli/skills).

Restore private or customized skill folders from your own private backup. The public [Career Ops](https://github.com/career-ops-hq/career-ops) and [AI Job Search](https://github.com/ai-job-search-dev/ai-job-search) repos provide upstream versions. Local integrations, personal evidence, credentials, and machine-specific paths need to be restored privately.

## 3. Install plugins

### Claude Code CLI and Claude Desktop Code mode

```powershell
$knowledgePlugins = @('data', 'enterprise-search', 'finance', 'human-resources',
    'marketing', 'operations', 'product-management', 'productivity', 'sales')
foreach ($name in $knowledgePlugins) {
    claude plugin install $name --marketplace anthropics/knowledge-work-plugins --scope user
}

claude plugin install power-automate --marketplace microsoft/power-platform-skills --scope user
claude plugin install fabric-skills --marketplace microsoft/skills-for-fabric --scope user
claude plugin install powerbi-authoring --marketplace microsoft/skills-for-fabric --scope user
claude plugin install reactive-resume --marketplace reactive-resume/reactive-resume --scope user
claude plugin install promptfoo --marketplace promptfoo/promptfoo --scope user
claude plugin install mcp-server-dev@claude-plugins-official --scope user
claude plugin install superpowers@claude-plugins-official --scope user
claude plugin list
```

In Claude Desktop **Code → Customize → Plugins → Yours**, the user-scoped plugins should appear as installed locally. Chat and Cowork use the Claude account’s plugin list. Use **Customize → Plugins → Discover** for the options your workspace makes available.

### Codex Desktop and CLI

```powershell
$marketplaces = @('microsoft/skills-for-fabric', 'anthropics/knowledge-work-plugins',
    'reactive-resume/reactive-resume', 'promptfoo/promptfoo', 'anthropics/claude-plugins-official')
foreach ($marketplace in $marketplaces) {
    codex plugin marketplace add $marketplace
}

codex plugin add superpowers@openai-curated-remote
codex plugin add data-analytics@openai-curated-remote
codex plugin add fabric-skills@fabric-collection
codex plugin add powerbi-authoring@fabric-collection
codex plugin add reactive-resume@reactive-resume
codex plugin add promptfoo@promptfoo
codex plugin add mcp-server-dev@claude-plugins-official

$knowledgePlugins = @('data', 'enterprise-search', 'finance', 'human-resources',
    'marketing', 'operations', 'product-management', 'productivity', 'sales')
foreach ($name in $knowledgePlugins) {
    codex plugin add "$name@knowledge-work-plugins"
}
```

If Data or Product Management is already enabled from another marketplace, keep one copy. The Data Analytics plugin contains `jupyter-notebooks`. Power Automate is listed in Microsoft’s Claude marketplace. Fabric and Power BI access require your own authorized Microsoft sign-in and any applicable server setup.

## 4. Install Python libraries

A plain `python` command uses the Python found on that process’s `PATH`. An activated project environment, a PyCharm interpreter, or a Fabric notebook can use a different Python. This setup adds a shared Python 3.12 environment to your Windows user PATH for use outside projects.

```powershell
$agentTools = Join-Path $env:LOCALAPPDATA 'AgentTools'
uv python install 3.12

function Install-AgentPythonGroup {
    param([string]$Name, [string[]]$Packages)
    $environment = Join-Path $agentTools $Name
    $executable = Join-Path $environment 'Scripts/python.exe'
    if (!(Test-Path -LiteralPath $executable)) {
        uv venv --seed --python 3.12 $environment
        if ($LASTEXITCODE -ne 0) { throw "Could not create $Name" }
    }
    uv pip install --python $executable @Packages
    if ($LASTEXITCODE -ne 0) { throw "Could not install $Name" }
    uv pip check --python $executable
    if ($LASTEXITCODE -ne 0) { throw "Dependency check failed for $Name" }
}

Install-AgentPythonGroup 'python' @(
    'fastapi', 'uvicorn', 'pydantic', 'streamlit', 'pandas', 'numpy', 'scipy',
    'scikit-learn', 'jupyterlab', 'nbformat', 'nbclient', 'ipykernel', 'duckdb',
    'docling', 'great-expectations', 'pandera', 'statsforecast', 'ortools',
    'mlflow', 'evidently', 'fg-data-profiling', 'flaml[automl]', 'pillow',
    'imageio', 'imageio-ffmpeg', 'matplotlib', 'usd-core'
)

$pythonBin = Join-Path $agentTools 'python/Scripts'
$userPath = [Environment]::GetEnvironmentVariable('Path', 'User')
$rest = @($userPath -split ';' | Where-Object { $_ -and $_.TrimEnd('\') -ne $pythonBin.TrimEnd('\') })
[Environment]::SetEnvironmentVariable('Path', ((@($pythonBin) + $rest) -join ';'), 'User')
$env:Path = "$pythonBin;$env:Path"
python -c 'import sys; print(sys.executable)'
```

Use separate environments for the larger or independently versioned stacks. Call the interpreter by its full path when using one of these.

```powershell
Install-AgentPythonGroup 'automl' @('autogluon.tabular', 'autogluon.timeseries')
Install-AgentPythonGroup 'knowledge' @('graphrag', 'graphiti-core', 'acryl-datahub')
Install-AgentPythonGroup 'simulation' @('camel-oasis')
Install-AgentPythonGroup 'voice' @('torch', 'transformers>=5.5', 'accelerate', 'huggingface-hub', 'soundfile')
Install-AgentPythonGroup 'voice-realtime' @('vibevoice[streamingtts] @ git+https://github.com/microsoft/VibeVoice.git@16fb2cb1217c9934a886e1948ffb06120caa2df5')

& "$agentTools/automl/Scripts/python.exe" -c 'from autogluon.timeseries import TimeSeriesPredictor'
& "$agentTools/knowledge/Scripts/python.exe" -c 'import graphrag, graphiti_core, datahub'
& "$agentTools/simulation/Scripts/python.exe" -c 'import oasis'
& "$agentTools/voice/Scripts/python.exe" -c 'import torch, transformers, soundfile'
& "$agentTools/voice-realtime/Scripts/python.exe" -c 'from vibevoice.modular.modeling_vibevoice_streaming_inference import VibeVoiceStreamingForConditionalGenerationInference'
```

## 5. Install browser, evaluation, and video tooling

```powershell
npm install -g ctx7 @playwright/cli promptfoo hyperframes
ctx7 --version
playwright-cli --version
promptfoo --version
hyperframes --version
hyperframes doctor

$videoTools = Join-Path $env:LOCALAPPDATA 'AgentTools/remotion'
New-Item -ItemType Directory -Path $videoTools -Force | Out-Null
Push-Location -LiteralPath $videoTools
try {
    if (!(Test-Path package.json)) { npm init -y }
    npm install --save-exact remotion @remotion/cli react react-dom three @react-three/fiber @react-three/rapier @react-three/postprocessing postprocessing
    npm ls --depth=0
    npx remotion browser ensure
} finally {
    Pop-Location
}

winget install --id BlenderFoundation.Blender --exact
```

Use Remotion for rendered video. Install matching Remotion packages in the actual project when it already has its own `package.json`. For Blender automation, open Blender once to initialize its user folders and follow the [MCP for Blender setup](https://github.com/ahujasid/mcp-for-blender#readme). Enable the addon, keep its listener on localhost, and set `BLENDER_MCP_SAFE_MODE=1` in the MCP client configuration if you want the addon’s script checks. NVIDIA Omniverse, cuOpt, and hosted knowledge or simulation platforms have their own deployment and service requirements.

For Microsoft VibeVoice, use `voice-realtime` for the [English narration demo](https://github.com/microsoft/VibeVoice/blob/16fb2cb1217c9934a886e1948ffb06120caa2df5/docs/vibevoice-realtime-0.5b.md) and `voice` for the newer Transformers runtime used for [caption transcription](https://github.com/microsoft/VibeVoice/blob/main/docs/vibevoice-asr.md). Model weights download separately and GPU support depends on the laptop. Test a short narration clip first.

## 6. Verify after restarting the apps

Fully quit and reopen both desktop apps and open a new terminal after changing PATH. Check `python -c 'import sys; print(sys.executable)'` inside each coding client if interpreter choice matters. Try `$video-production` in Codex or `/video-production` in Claude Code. Vercel’s `use-ai-sdk` folder declares the invocation name `ai-sdk`. Use each app’s plugin list to verify the setup, and sign in to external services when you first need them.
