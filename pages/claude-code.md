---
layout: center
transition: slide-up
---

<h1 flex="~ col" class="text-center items-center">
<div text-2xl origin-top-left transition duration-500 :class="$clicks <= 1 ? 'scale-150' : 'op50'">
  <span v-click>Meet</span>
</div>
<div mt2 forward:delay-300 v-click class="flex items-center gap-4">
  <img src="/cc.svg" alt="Claude Code" class="h-12 w-12" />
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

#  Getting Started — First Session

Log in once, then describe what you want in plain English.

<div class="grid grid-cols-2 gap-8 mt-4 text-xm">

<div>

````md magic-move


```bash
#  **Step 1 — Log in**
claude # Prompted to log in on first use
/login # Switch accounts at any time
```



```bash
# **Step 2 — Start in your project**
cd /path/to/your/project
claude
```



```md
<!--**Step 3 — Ask anything**-->
what does this project do?
what technologies does this project use?
where is the main entry point?
explain the folder structure
```

````

<div class="text-xs opacity-60 mt-1 mb-4">
  Supports: Claude Pro/Max/Teams/Enterprise · Console API · Bedrock · Vertex AI · Foundry
</div>

<div class="text-xs opacity-60 mt-1">
  Place at root — Claude reads it automatically every session
</div>

</div>

<div>

<div v-click>

**What it can do**

<div class="space-y-2 mt--3">
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

<div style="max-height: 150px; overflow-y: auto;">

```markdown
# My Project

## Stack
- Next.js 15, TypeScript, Tailwind
- Supabase for auth + database

## Conventions
- kebab-case filenames
- Run `bun run typecheck` after changes
```

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
# use carefully
claude --dangerously-skip-permissions
```

</div>

<!--
The permission model is what makes Claude Code safe to run on real codebases.
"Accept all" mode can be toggled per session for trusted automation tasks.
-->

---
layout: default
transition: slide-up
---

# Claude Code — Hooks

Shell commands (or HTTP calls) that fire automatically on lifecycle events.

<div class="grid grid-cols-2 gap-6 mt-4">

<div>

**Event types**

<div class="space-y-2 mt-2 text-sm">
  <div v-click class="flex gap-2 items-start">
    <span class="text-yellow-400 font-mono text-xs mt-0.5">PreToolUse</span>
    <span class="opacity-80">— runs before a tool call; can block it</span>
  </div>
  <div v-click class="flex gap-2 items-start">
    <span class="text-green-400 font-mono text-xs mt-0.5">PostToolUse</span>
    <span class="opacity-80">— runs after a tool call completes</span>
  </div>
  <div v-click class="flex gap-2 items-start">
    <span class="text-blue-400 font-mono text-xs mt-0.5">Stop</span>
    <span class="opacity-80">— fires when Claude finishes; can resume it</span>
  </div>
  <div v-click class="flex gap-2 items-start">
    <span class="text-purple-400 font-mono text-xs mt-0.5">Notification</span>
    <span class="opacity-80">— desktop alert when Claude needs attention</span>
  </div>
</div>

<div v-click class="mt-4 text-xs opacity-60">
  Configure in <code>~/.claude/settings.json</code> · matcher uses regex on tool name
</div>

</div>

<div v-click>

**Real-world recipes**

```json
{
  "hooks": {
    "PostToolUse": [{
      "matcher": "Edit|Write",
      "hooks": [{
        "type": "command",
        "command": "npx prettier --write $TOOL_OUTPUT_FILE"
      }]
    }],
    "Stop": [{
      "hooks": [{
        "type": "command",
        "command": "osascript -e 'display notification \"Claude is done\"'"
      }]
    }]
  }
}
```

</div>

</div>

<!--
Hooks run outside Claude's context — they're plain shell scripts, so they can do
anything: send Slack messages, run formatters, validate output, or log to a file.
The Stop hook can return {"ok": false} to make Claude keep working.
-->

---
layout: default
transition: slide-up
---

# Claude Code — MCP Servers

**Model Context Protocol** — plug any external tool, database, or API into Claude as a first-class tool.

<div class="grid grid-cols-2 gap-6 mt-4">

<div>

<div v-click>

**Add a server in one line**

```bash
# HTTP server (remote)
claude mcp add --transport http github \
  https://api.githubcopilot.com/mcp/

# stdio server (local process)
claude mcp add filesystem \
  npx @modelcontextprotocol/server-filesystem /tmp
```

</div>

<div v-click class="mt-4">

**Or configure in settings.json**

<div style="max-height: 150px; overflow-y: auto;">

```json
{
  "mcpServers": {
    "sentry": {
      "type": "http",
      "url": "https://mcp.sentry.dev/mcp"
    },
    "my-db": {
      "type": "stdio",
      "command": "node",
      "args": ["./mcp-server.js"],
      "env": { "DATABASE_URL": "$DATABASE_URL" }
    }
  }
}
```

</div>

</div>

</div>

<div>

<div v-click class="mb-4">

**Popular MCP servers**

<div class="space-y-2 text-sm mt-2">
  <div class="flex gap-2 items-center"><span class="text-green-400">→</span> <code>github</code> — PRs, issues, reviews</div>
  <div class="flex gap-2 items-center"><span class="text-green-400">→</span> <code>filesystem</code> — read/write outside cwd</div>
  <div class="flex gap-2 items-center"><span class="text-green-400">→</span> <code>postgres</code> — query your database</div>
  <div class="flex gap-2 items-center"><span class="text-green-400">→</span> <code>sentry</code> — fetch error traces</div>
  <div class="flex gap-2 items-center"><span class="text-green-400">→</span> <code>context7</code> — live library docs</div>
  <div class="flex gap-2 items-center"><span class="text-green-400">→</span> <code>cloudflare</code> — D1, KV, Workers</div>
</div>

</div>

<div v-click class="border border-blue-500/30 rounded-lg p-3 bg-blue-500/5 text-xs">
  <div class="font-bold text-blue-400 mb-1">How it works</div>
  Claude discovers all server tools on startup and calls them the same way it calls built-in tools like <code>Read</code> or <code>Bash</code>. You just ask: <em>"Check Sentry for the latest error"</em>.
</div>

</div>

</div>

<!--
MCP is an open standard — any language can implement a server.
/mcp inside a session lets you enable/disable servers without restarting.
-->

---
layout: default
transition: slide-up
---

# Claude Code — Skills & Commands

Reusable slash-command prompts you (or your team) define once and invoke with `/`.

<div class="grid grid-cols-2 gap-6 mt-4">

<div>

<div v-click>

**Anatomy of a skill**

```
.claude/
├── skills/
│   └── review-pr/
│       └── SKILL.md       ← the skill definition
└── commands/
    └── deploy.md          ← simpler one-file command
```

</div>

<div v-click class="mt-4">

**SKILL.md format**

<div style="max-height: 150px; overflow-y: auto;">

```md
---
description: Review a pull request for correctness,
  security, and style
---

Review the diff in $ARGUMENTS.
Check for: security issues, naming conventions,
missing tests, and edge cases.
Output a structured review with severity labels.
```

</div>

</div>

</div>

<div>

<div v-click class="mb-4">

**Using skills in a session**

```bash
# Browse all available skills
/

# Invoke by name
/review-pr https://github.com/org/repo/pull/42
/deploy staging
/commit
/pr_comments
```

</div>

<div v-click class="border border-purple-500/30 rounded-lg p-3 bg-purple-500/5 text-xs">
  <div class="font-bold text-purple-400 mb-1">Plugins — bundle everything</div>
  <div class="opacity-80 space-y-1">
    <div>A <strong>plugin</strong> packages skills + hooks + MCP servers into a shareable <code>plugin.json</code> manifest — install once, works for the whole team.</div>
    <div class="mt-2 font-mono text-xs">claude plugin install gh:org/my-plugin</div>
  </div>
</div>

<div v-click class="mt-3 text-xs opacity-60">
  Skills ship with this very session — the <code>/slidev-teaching</code>, <code>/commit</code>, <code>/review-pr</code> shortcuts you see here are all skills.
</div>

</div>

</div>

<!--
Skills are how you encode team knowledge — runbooks, review checklists, deploy
procedures — into Claude's vocabulary. Anyone on the team types /deploy and gets
the same expert behaviour every time.
-->
