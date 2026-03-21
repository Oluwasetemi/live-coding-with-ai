---
layout: center
transition: slide-up
---

<h1 flex="~ col" class="text-center">
<div v-click class="text-2xl opacity-50">Patterns for</div>
<div mt2 forward:delay-300 v-click class="text-gradient text-5xl font-hand">Live Coding</div>
</h1>

---
layout: default
transition: slide-up
---

# Prompting Patterns That Work

Writing good prompts is the highest-leverage skill.

<div class="grid grid-cols-2 gap-6 mt-6">

<div>

<div v-click class="mb-4">

**❌ Vague**
```
make this code better
```

**✅ Specific + Constrained**
```
refactor auth.ts to use async/await.
Keep the existing function signatures.
Run npm run typecheck when done.
```

</div>

<div v-click>

**❌ Too broad**
```
build me an e-commerce site
```

**✅ Scoped + Verifiable**
```
add a /cart route to the Express API
that accepts { productId, qty } and
writes to the SQLite carts table.
Add a test in tests/cart.test.ts.
```

</div>

</div>

<div class="space-y-4">

<div v-click class="bg-white/5 rounded p-3 text-sm">
  <div class="font-bold mb-1">Pattern: Anchor to files</div>
  <div class="opacity-70">Reference specific files and line numbers — agents explore better when they have a starting point rather than scanning everything.</div>
</div>

<div v-click class="bg-white/5 rounded p-3 text-sm">
  <div class="font-bold mb-1">Pattern: Specify the verification step</div>
  <div class="opacity-70">Tell the agent how to confirm success: <em>"run npm test and make sure all tests pass"</em>. This closes the feedback loop.</div>
</div>

<div v-click class="bg-white/5 rounded p-3 text-sm">
  <div class="font-bold mb-1">Pattern: Use CLAUDE.md as a multiplier</div>
  <div class="opacity-70">Every convention you document there is a prompt you never have to write again. Think of it as onboarding docs for the AI.</div>
</div>

</div>

</div>

---
layout: default
transition: slide-up
---

# Real-World Workflows

<div class="grid grid-cols-3 gap-4 mt-6">

<div v-click class="border border-white/15 rounded-lg p-4">
  <div class="text-2xl mb-2">🔧</div>
  <div class="font-bold mb-2">Bug Fix Loop</div>
  <div class="text-xs opacity-70 space-y-1">
    <div>1. Paste error log / failing test</div>
    <div>2. Agent traces root cause</div>
    <div>3. Proposes + applies fix</div>
    <div>4. Re-runs test to verify</div>
    <div>5. Creates commit message</div>
  </div>
</div>

<div v-click class="border border-white/15 rounded-lg p-4">
  <div class="text-2xl mb-2">🏗️</div>
  <div class="font-bold mb-2">Feature Scaffold</div>
  <div class="text-xs opacity-70 space-y-1">
    <div>1. Describe the feature + constraints</div>
    <div>2. Agent proposes a plan first</div>
    <div>3. You approve / adjust the plan</div>
    <div>4. Agent implements incrementally</div>
    <div>5. Review diffs in your editor</div>
  </div>
</div>

<div v-click class="border border-white/15 rounded-lg p-4">
  <div class="text-2xl mb-2">🔄</div>
  <div class="font-bold mb-2">Codebase Migration</div>
  <div class="text-xs opacity-70 space-y-1">
    <div>1. Define the target state in CLAUDE.md</div>
    <div>2. Agent inventories affected files</div>
    <div>3. Migrates in batches</div>
    <div>4. Runs typecheck after each batch</div>
    <div>5. Creates a PR with a full summary</div>
  </div>
</div>

</div>

<div v-click class="mt-6 bg-yellow-500/10 border border-yellow-500/30 rounded-lg p-4 text-sm">

**Pro tip — keep humans in the loop strategically:**
Let the agent do the boring parts (boilerplate, migrations, test setup). Review architecture and business logic decisions yourself. The agent is fast; you provide judgment.

</div>

<!--
The migration workflow is where agentic tools really shine —
tedious work that a human would rush through gets done systematically.
-->
