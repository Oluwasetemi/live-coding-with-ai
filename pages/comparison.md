---
layout: center
transition: slide-up
---

<h1 flex="~ col" class="text-center">
<div v-click class="text-2xl opacity-50">How do they</div>
<div mt2 forward:delay-300 v-click class="text-gradient text-5xl font-hand">Stack Up?</div>
</h1>

---
layout: default
transition: slide-up
---

# Tool Comparison

<div class="mt-4 overflow-auto">

| | **Claude Code** | **Codex CLI** | **OpenCode** | **Aider** | **Gemini CLI** |
|---|---|---|---|---|---|
| **Model** | Claude (Anthropic) | GPT / o-series | Any provider | Any provider | Gemini |
| **UI** | Terminal REPL | Terminal REPL | TUI (split panes) | Terminal REPL | Terminal REPL |
| **Open Source** | ❌ | ❌ | ✅ | ✅ | ❌ |
| **MCP Support** | ✅ | ❌ | ✅ | ❌ | ✅ |
| **Sandbox** | Permissions model | macOS / Docker | ❌ | ❌ | ❌ |
| **Project config** | `CLAUDE.md` | `AGENTS.md` | `opencode.json` | `.aider.conf.yml` | `GEMINI.md` |
| **Git-native** | ✅ | ✅ | ✅ | ✅ (auto-commit) | ✅ |
| **Context window** | 200K tokens | 128K tokens | Varies by model | Varies | **1M tokens** |
| **Free tier** | ✅ (limited) | ✅ (limited) | Bring your key | Bring your key | ✅ |

</div>

<div v-click class="mt-4 text-sm opacity-60 text-center">

💡 All tools benefit from a good project config file — treat it like onboarding docs for the AI

</div>

---
layout: two-cols
transition: slide-up
---

# When to Use Which

<div class="space-y-4 mt-4">

<div v-click class="border-l-4 border-orange-400 pl-4">
  <div class="font-bold">Claude Code</div>
  <div class="text-sm opacity-70">Best all-rounder. Strongest at complex multi-file refactors, PR workflows, and MCP integrations. Best-in-class reasoning.</div>
</div>

<div v-click class="border-l-4 border-blue-400 pl-4">
  <div class="font-bold">Codex CLI</div>
  <div class="text-sm opacity-70">Reach for it when you need sandboxed execution or multimodal input (paste a screenshot of a UI to build).</div>
</div>

<div v-click class="border-l-4 border-purple-400 pl-4">
  <div class="font-bold">OpenCode</div>
  <div class="text-sm opacity-70">When your team needs model flexibility or you want 100% open-source, self-hostable tooling.</div>
</div>

<div v-click class="border-l-4 border-green-400 pl-4">
  <div class="font-bold">Gemini CLI</div>
  <div class="text-sm opacity-70">When context size matters — ingest an entire large codebase in one shot with 1M token window.</div>
</div>

</div>

::right::

<div class="pl-6 mt-4">

<div v-click class="bg-white/5 rounded-lg p-4 mb-4">
  <div class="font-bold mb-2 text-sm">The honest take</div>
  <div class="text-xs opacity-70 space-y-1">
    <div>• They are converging rapidly — features copy across tools weekly</div>
    <div>• The model matters more than the shell around it</div>
    <div>• Your <strong>project config file</strong> is the biggest productivity multiplier</div>
  </div>
</div>

<div v-click class="bg-white/5 rounded-lg p-4">
  <div class="font-bold mb-2 text-sm">Pick by team context</div>
  <div class="text-xs opacity-70 space-y-1">
    <div>🏢 Enterprise with Anthropic contract → Claude Code</div>
    <div>🔓 OSS / self-host required → OpenCode + Aider</div>
    <div>📐 Need multimodal → Codex CLI</div>
    <div>📚 Huge legacy codebase → Gemini CLI</div>
  </div>
</div>

</div>

<!--
The real superpower isn't picking the perfect tool — it's learning
how to write great prompts and project config files.
-->
