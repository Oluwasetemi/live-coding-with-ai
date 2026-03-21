---
layout: center
transition: slide-up
---

<h1 flex="~ col" class="text-center">
<div text-2xl origin-top-left transition duration-500 :class="$clicks <= 1 ? 'scale-150' : 'op50'">
  <span v-click>What are</span>
  <span> Agentic</span>
</div>
<div mt2 forward:delay-300 v-click class="text-gradient">Coding Tools?</div>
</h1>

---
layout: default
transition: slide-up
---

# What are Terminal Agentic Tools?

AI assistants that **live in your terminal** — they don't just suggest code, they *act*.

<div class="grid grid-cols-3 gap-6 mt-8">

<div v-click class="border border-white/20 rounded-lg p-4">
  <div class="text-2xl mb-2">🤔</div>
  <div class="font-bold text-lg mb-1">Traditional AI</div>
  <div class="text-sm opacity-70">You copy-paste suggestions from a chat UI into your editor</div>
</div>

<div v-click class="border border-white/20 rounded-lg p-4">
  <div class="text-2xl mb-2">⚡</div>
  <div class="font-bold text-lg mb-1">Agentic Tools</div>
  <div class="text-sm opacity-70">The AI reads your files, writes code, runs tests — autonomously</div>
</div>

<div v-click class="border border-white/20 rounded-lg p-4">
  <div class="text-2xl mb-2">🔁</div>
  <div class="font-bold text-lg mb-1">The Loop</div>
  <div class="text-sm opacity-70">Plan → Act → Observe → Repeat until the task is done</div>
</div>

</div>

<div v-click class="mt-8 text-center">

> **You describe the goal. The agent figures out the steps.**

</div>

<!--
The key shift: from autocomplete to autonomous execution.
These tools can read your entire codebase, understand context,
and make coordinated changes across many files.
-->

---
layout: two-cols
transition: slide-up
---

# The Agent Loop

How agentic tools reason and act:

<div class="mt-4 space-y-3">

<div v-click class="flex items-start gap-3">
  <div class="bg-blue-500/20 text-blue-400 rounded px-2 py-1 text-sm font-mono shrink-0">1. Plan</div>
  <div class="text-sm opacity-80">Break the goal into steps, understand the codebase structure</div>
</div>

<div v-click class="flex items-start gap-3">
  <div class="bg-green-500/20 text-green-400 rounded px-2 py-1 text-sm font-mono shrink-0">2. Read</div>
  <div class="text-sm opacity-80">Explore relevant files, search for patterns, understand context</div>
</div>

<div v-click class="flex items-start gap-3">
  <div class="bg-yellow-500/20 text-yellow-400 rounded px-2 py-1 text-sm font-mono shrink-0">3. Act</div>
  <div class="text-sm opacity-80">Edit files, run shell commands, install packages</div>
</div>

<div v-click class="flex items-start gap-3">
  <div class="bg-purple-500/20 text-purple-400 rounded px-2 py-1 text-sm font-mono shrink-0">4. Verify</div>
  <div class="text-sm opacity-80">Run tests, check types, lint — confirm the change works</div>
</div>

<div v-click class="flex items-start gap-3">
  <div class="bg-red-500/20 text-red-400 rounded px-2 py-1 text-sm font-mono shrink-0">5. Repeat</div>
  <div class="text-sm opacity-80">Loop until the task is complete or clarification is needed</div>
</div>

</div>

::right::

<div class="mt-12 pl-6">

```mermaid {scale: 0.7}
flowchart TD
    A[User Goal] --> B[Plan]
    B --> C[Read Files]
    C --> D[Edit / Run]
    D --> E{Tests Pass?}
    E -- Yes --> F[Done ✅]
    E -- No --> B
```

</div>

<!--
The agentic loop is the key mental model.
Unlike autocomplete, the agent owns the full cycle from reading to verification.
-->
