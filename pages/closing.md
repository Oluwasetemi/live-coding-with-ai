---
layout: default
transition: slide-up
---

# Key Takeaways

<div class="grid grid-cols-2 gap-6 mt-6">

<div class="space-y-4">

<div v-click class="flex gap-3 items-start">
  <div class="text-2xl">🧠</div>
  <div>
    <div class="font-bold">Agentic ≠ Autocomplete</div>
    <div class="text-sm opacity-70">These tools act in a loop — they read, edit, run, and verify until the task is done.</div>
  </div>
</div>

<div v-click class="flex gap-3 items-start">
  <div class="text-2xl">📄</div>
  <div>
    <div class="font-bold">Config files are leverage</div>
    <div class="text-sm opacity-70"><code>CLAUDE.md</code> / <code>AGENTS.md</code> are the highest-ROI thing you can write. Document your conventions once.</div>
  </div>
</div>

<div v-click class="flex gap-3 items-start">
  <div class="text-2xl">🎯</div>
  <div>
    <div class="font-bold">Specificity beats vagueness</div>
    <div class="text-sm opacity-70">Anchor prompts to files, define success criteria, and tell the agent how to verify its work.</div>
  </div>
</div>

<div v-click class="flex gap-3 items-start">
  <div class="text-2xl">🔀</div>
  <div>
    <div class="font-bold">The right tool shifts with context</div>
    <div class="text-sm opacity-70">No single winner. Claude Code for complex reasoning, Gemini for big context, OpenCode for model freedom.</div>
  </div>
</div>

</div>

<div v-click class="flex flex-col justify-center pl-6">

<div class="text-center mb-6">

**Start here this week**

</div>

```bash
# 1. Install Claude Code
curl -fsSL https://claude.ai/install.sh | bash

# 2. Create a CLAUDE.md in your project
echo "# My Project\n## Stack: ..." > CLAUDE.md

# 3. Try a real task
claude "explain what this codebase does
then suggest 3 quick wins for code quality"
```

<div class="text-xs opacity-50 mt-4 text-center">
  The best way to learn is to try it on a real problem.
</div>

</div>

</div>

---
layout: center
transition: fade
hideInToc: true
---

<div class="text-center">

<div class="text-6xl font-hand text-gradient mb-6">Thank You</div>

<div class="text-xl opacity-70 mb-8">Live Coding with AI — Building Real Solutions</div>

<div class="flex gap-8 justify-center text-sm opacity-60">
  <div>
    <div class="font-bold mb-1">Claude Code</div>
    <div>claude.ai/code</div>
  </div>
  <div>
    <div class="font-bold mb-1">Codex CLI</div>
    <div>github.com/openai/codex</div>
  </div>
  <div>
    <div class="font-bold mb-1">OpenCode</div>
    <div>opencode.ai</div>
  </div>
  <div>
    <div class="font-bold mb-1">Aider</div>
    <div>aider.chat</div>
  </div>
</div>

<div class="mt-8">
  <a href="https://live-coding-with-ai-landing.vercel.app/" target="_blank"
    class="inline-block px-4 py-2 rounded-lg border border-white/20 text-sm hover:bg-white/10 transition">
    🚀 Live Tool built in this workshop →
  </a>
</div>

<div class="mt-4 text-sm opacity-40">
  Slides built with <a href="https://sli.dev" class="underline">Slidev</a>
</div>

</div>

<!--
Questions welcome!
-->
