---
layout: center
transition: slide-up
---

<h1 flex="~ col" class="text-center">
<div text-2xl origin-top-left transition duration-500 :class="$clicks <= 1 ? 'scale-150' : 'op50'">
  <span v-click>The</span>
  <span> Ecosystem</span>
</div>
<div mt2 forward:delay-300 v-click class="text-gradient">Other Terminal Agents</div>
</h1>

---
layout: default
transition: slide-up
---

# OpenAI Codex CLI

OpenAI's terminal agent — multimodal and sandboxed.

<div class="grid grid-cols-2 gap-8 mt-4">

<div>

```bash
npm install -g @openai/codex
codex "migrate this Express app to Fastify"
```

**Key features**

<div class="space-y-2 mt-3">
  <div v-click class="flex gap-2 text-sm">
    <span class="text-blue-400">→</span>
    <span>Multimodal: pass screenshots or diagrams</span>
  </div>
  <div v-click class="flex gap-2 text-sm">
    <span class="text-blue-400">→</span>
    <span>Sandboxed execution (macOS Seatbelt / Docker)</span>
  </div>
  <div v-click class="flex gap-2 text-sm">
    <span class="text-blue-400">→</span>
    <span>Supports <code>o4-mini</code>, <code>o3</code> models</span>
  </div>
  <div v-click class="flex gap-2 text-sm">
    <span class="text-blue-400">→</span>
    <span>Full-auto mode with network-disabled sandbox</span>
  </div>
</div>

</div>

<div v-click>

**Approval modes**

```bash
# Suggest only — you review every change
codex --approval-mode suggest "..."

# Auto-edit — edits files, asks before running
codex --approval-mode auto-edit "..."

# Full-auto — completely autonomous
codex --approval-mode full-auto "..."
```

<div class="text-xs opacity-60 mt-2">
  Config: <code>~/.codex/config.yaml</code> or <code>AGENTS.md</code> in project root
</div>

</div>

</div>

---
layout: default
transition: slide-up
---

# OpenCode

An open-source TUI (terminal UI) agentic coding tool.

<div class="grid grid-cols-2 gap-8 mt-4">

<div>

```bash
# Install via Go or Homebrew
brew install opencode-ai/tap/opencode
opencode
```

**What makes it different**

<div class="space-y-2 mt-3">
  <div v-click class="flex gap-2 text-sm">
    <span class="text-purple-400">→</span>
    <span>Rich TUI with split panes (chat + file diff)</span>
  </div>
  <div v-click class="flex gap-2 text-sm">
    <span class="text-purple-400">→</span>
    <span>Provider-agnostic: Claude, GPT-4, Gemini, local LLMs</span>
  </div>
  <div v-click class="flex gap-2 text-sm">
    <span class="text-purple-400">→</span>
    <span>LSP integration for context-aware edits</span>
  </div>
  <div v-click class="flex gap-2 text-sm">
    <span class="text-purple-400">→</span>
    <span>100% open source (MIT) — run fully offline</span>
  </div>
</div>

</div>

<div v-click>

**opencode.json config**

```json
{
  "model": "anthropic/claude-sonnet-4-6",
  "autoapprove": false,
  "keybindings": {
    "submit": "enter",
    "new_session": "ctrl+n"
  },
  "mcp": {
    "servers": {}
  }
}
```

<div class="text-xs opacity-60 mt-2">
  Great for: teams who want model flexibility without vendor lock-in
</div>

</div>

</div>

---
layout: default
transition: slide-up
---

# Other Tools Worth Knowing

<div class="grid grid-cols-2 gap-6 mt-6">

<div v-click class="border border-white/15 rounded-lg p-4">
  <div class="flex items-center gap-2 mb-2">
    <span class="text-lg">🤖</span>
    <span class="font-bold">Aider</span>
    <span class="text-xs bg-white/10 px-1 rounded">Open Source</span>
  </div>
  <div class="text-xs opacity-70 mb-2">Python-based, git-native agent. Tracks changes with git automatically.</div>
  <code class="text-xs">pip install aider-chat && aider</code>
</div>

<div v-click class="border border-white/15 rounded-lg p-4">
  <div class="flex items-center gap-2 mb-2">
    <span class="text-lg">🌊</span>
    <span class="font-bold">Amp (Sourcegraph)</span>
    <span class="text-xs bg-white/10 px-1 rounded">Terminal</span>
  </div>
  <div class="text-xs opacity-70 mb-2">Deep codebase search + agent from Sourcegraph team. Strong at large repos.</div>
  <code class="text-xs">npm install -g @sourcegraph/amp</code>
</div>

<div v-click class="border border-white/15 rounded-lg p-4">
  <div class="flex items-center gap-2 mb-2">
    <span class="text-lg">🦀</span>
    <span class="font-bold">Gemini CLI</span>
    <span class="text-xs bg-white/10 px-1 rounded">Google</span>
  </div>
  <div class="text-xs opacity-70 mb-2">Google's terminal agent. 1M token context window. Free tier available.</div>
  <code class="text-xs">npm install -g @google/gemini-cli && gemini</code>
</div>

<div v-click class="border border-white/15 rounded-lg p-4">
  <div class="flex items-center gap-2 mb-2">
    <span class="text-lg">🧠</span>
    <span class="font-bold">Goose (Block)</span>
    <span class="text-xs bg-white/10 px-1 rounded">Open Source</span>
  </div>
  <div class="text-xs opacity-70 mb-2">Extensible agent from Block (Square). Plugin system for custom tools.</div>
  <code class="text-xs">brew install block/tap/goose</code>
</div>

</div>

<!--
The space is moving fast — new tools ship weekly.
The key differentiators are: model flexibility, sandbox safety, UI style, and customization.
-->
