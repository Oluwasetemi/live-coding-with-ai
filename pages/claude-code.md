---
layout: center
transition: slide-up
---

<h1 flex="~ col" class="text-center">
<div text-2xl origin-top-left transition duration-500 :class="$clicks <= 1 ? 'scale-150' : 'op50'">
  <span v-click>Meet</span>
</div>
<div mt2 forward:delay-300 v-click>
  <span class="text-gradient font-hand text-5xl">Claude Code</span>
</div>
<div mt2 v-click class="text-xl opacity-60">Anthropic's official terminal coding agent</div>
</h1>

---
layout: default
transition: slide-up
---

# Install Claude Code

Pick your platform — one command and you're running.

<div class="grid grid-cols-[1fr_auto] gap-6 mt-4 items-start">

<div>

````md magic-move
```bash
# ── macOS / Linux / WSL (Recommended) ──────────────────
# Native install — auto-updates in the background
curl -fsSL https://claude.ai/install.sh | bash

# Then start Claude Code
claude
```
```powershell
# ── Windows PowerShell ──────────────────────────────────
# Native install — auto-updates in the background
irm https://claude.ai/install.ps1 | iex

# Then start Claude Code
claude
```
```batch
:: ── Windows CMD ─────────────────────────────────────────
:: Requires Git for Windows: https://git-scm.com/downloads/win
curl -fsSL https://claude.ai/install.cmd -o install.cmd && install.cmd && del install.cmd

:: Then start Claude Code
claude
```
```bash
# ── Homebrew (macOS / Linux) ────────────────────────────
# Does NOT auto-update — run upgrade periodically
brew install --cask claude-code

# Upgrade when needed
brew upgrade claude-code

# Then start Claude Code
claude
```
```powershell
# ── WinGet (Windows) ────────────────────────────────────
# Does NOT auto-update — run upgrade periodically
winget install Anthropic.ClaudeCode

# Upgrade when needed
winget upgrade Anthropic.ClaudeCode

# Then start Claude Code
claude
```
````

</div>

<div class="space-y-3 text-sm min-w-48">
  <div v-click="1" :class="$clicks === 1 ? 'opacity-100 font-bold text-green-400' : 'opacity-40'" class="transition flex gap-2 items-center">
    <carbon:checkmark-filled /> macOS / Linux / WSL
  </div>
  <div v-click="2" :class="$clicks === 2 ? 'opacity-100 font-bold text-blue-400' : 'opacity-40'" class="transition flex gap-2 items-center">
    <carbon:checkmark-filled /> Windows PowerShell
  </div>
  <div v-click="3" :class="$clicks === 3 ? 'opacity-100 font-bold text-yellow-400' : 'opacity-40'" class="transition flex gap-2 items-center">
    <carbon:checkmark-filled /> Windows CMD
  </div>
  <div v-click="4" :class="$clicks === 4 ? 'opacity-100 font-bold text-orange-400' : 'opacity-40'" class="transition flex gap-2 items-center">
    <carbon-logo-github /> Homebrew
  </div>
  <div v-click="5" :class="$clicks === 5 ? 'opacity-100 font-bold text-purple-400' : 'opacity-40'" class="transition flex gap-2 items-center">
    <carbon:checkmark-filled /> WinGet
  </div>
</div>

</div>

<div v-click="6" class="mt-4 text-xs opacity-50 flex gap-6">
  <span>💡 Native installs (curl/irm) auto-update silently</span>
  <span>🍺 Homebrew / WinGet require manual <code>upgrade</code></span>
  <span>🌐 Also: Web · Desktop App · VS Code · JetBrains · Slack · GitHub Actions</span>
</div>

<!--
The native curl/irm scripts are the recommended path — they handle PATH setup,
auto-updates, and platform quirks automatically. npm install -g is legacy.
-->

---
layout: default
transition: slide-up
class: text-sm
---

Getting Started — First Session

Log in once, then describe what you want in plain English.

<div class="grid grid-cols-2 gap-8 mt-4 text-xm">

<div>

**Step 1 — Log in**

```bash
claude
# Prompted to log in on first use

/login
# Switch accounts at any time
```

<div class="text-xs opacity-60 mt-1 mb-4">
  Supports: Claude Pro/Max/Teams/Enterprise · Console API · Bedrock · Vertex AI · Foundry
</div>

**Step 2 — Start in your project**

```bash
cd /path/to/your/project
claude
```

**Step 3 — Ask anything**

```text
what does this project do?
what technologies does this project use?
where is the main entry point?
explain the folder structure
```

</div>

<div>

<div v-click>

**What it can do**

<div class="space-y-2 mt-3">
  <div class="flex gap-2 items-start text-sm">
    <span class="text-green-400">✓</span>
    <span>Read, write, and edit any file in your project</span>
  </div>
  <div class="flex gap-2 items-start text-sm">
    <span class="text-green-400">✓</span>
    <span>Run shell commands, tests, and build scripts</span>
  </div>
  <div class="flex gap-2 items-start text-sm">
    <span class="text-green-400">✓</span>
    <span>Search your codebase with Glob and Grep tools</span>
  </div>
  <div class="flex gap-2 items-start text-sm">
    <span class="text-green-400">✓</span>
    <span>Create git commits, branches, and PRs via <code>gh</code></span>
  </div>
  <div class="flex gap-2 items-start text-sm">
    <span class="text-green-400">✓</span>
    <span>Spawn parallel sub-agents for independent tasks</span>
  </div>
  <div class="flex gap-2 items-start text-sm">
    <span class="text-green-400">✓</span>
    <span>Connect to MCP servers for external integrations</span>
  </div>
</div>

</div>

<div v-click class="mt-4">

**CLAUDE.md — Project Memory**

```markdown
# My Project

## Stack
- Next.js 15, TypeScript, Tailwind
- Supabase for auth + database

## Conventions
- kebab-case filenames
- Run `bun run typecheck` after changes
```

<div class="text-xs opacity-60 mt-1">
  Place at root — Claude reads it automatically every session
</div>

</div>

</div>

</div>

<!--
Credentials are stored after first login — you won't be prompted again.
CLAUDE.md is the highest-leverage thing you can set up for a team.
-->

---
layout: default
transition: slide-up
---

# Claude Code — Key Commands

```bash {1-4|6-10|12-15|17-20|all}
# ── Interactive sessions ────────────────────────────────
claude                          # start session in cwd
claude "fix the failing tests"  # session with initial prompt
claude -c                       # continue most recent conversation

# ── One-shot / scripted ─────────────────────────────────
claude -p "explain this function"
claude -p "list all TODO comments" --output-format json
echo "refactor auth.ts" | claude --print
cat error.log | claude -p "diagnose and fix"

# ── Resume conversations ────────────────────────────────
claude -r                       # pick from recent sessions
claude commit                   # create a git commit

# ── Inside a session ────────────────────────────────────
/help      /clear      /login
/compact   /memory     /doctor
/review    /bug        /pr_comments
```

<div v-click class="mt-4 grid grid-cols-2 gap-4 text-xs opacity-70">
  <div>⌨️ Press <code>?</code> for keyboard shortcuts · Tab for completion · ↑ for history</div>
  <div>🔁 Type <code>/</code> to browse all commands and installed skills</div>
</div>

<!--
The --print flag + piping stdin is great for CI pipelines.
claude commit is a shortcut that uses Claude to write your commit message.
-->

---
layout: default
transition: slide-up
---

# Claude Code — Permission Model

Claude asks before taking risky actions. You control the blast radius.

<div class="grid grid-cols-3 gap-4 mt-6">

<div v-click class="border border-green-500/30 rounded-lg p-4 bg-green-500/5">
  <div class="font-bold text-green-400 mb-2">Auto-allowed</div>
  <div class="text-xs space-y-1 opacity-80">
    <div>• Read files</div>
    <div>• Search (Glob/Grep)</div>
    <div>• Run tests</div>
    <div>• Git status/diff/log</div>
  </div>
</div>

<div v-click class="border border-yellow-500/30 rounded-lg p-4 bg-yellow-500/5">
  <div class="font-bold text-yellow-400 mb-2">Asks first</div>
  <div class="text-xs space-y-1 opacity-80">
    <div>• Write / edit files</div>
    <div>• Install packages</div>
    <div>• Run shell commands</div>
    <div>• Git commit</div>
  </div>
</div>

<div v-click class="border border-red-500/30 rounded-lg p-4 bg-red-500/5">
  <div class="font-bold text-red-400 mb-2">Always confirms</div>
  <div class="text-xs space-y-1 opacity-80">
    <div>• Git push / force push</div>
    <div>• Delete files/branches</div>
    <div>• Destructive operations</div>
    <div>• External API calls</div>
  </div>
</div>

</div>

<div v-click class="mt-6">

```bash
# Allow specific tools without prompting (session flag)
claude --allowedTools "Bash(npm run test),Edit,Read"

# Or lock it down in ~/.claude/settings.json
# "permissions": { "allow": [...], "deny": [...] }
```

</div>

<!--
The permission model is what makes Claude Code safe to run on real codebases.
"Accept all" mode can be toggled per session for trusted automation tasks.
-->
