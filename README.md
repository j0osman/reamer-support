<div align="center">
<img src="https://reamerlabs.com/reamer-mark.png" width="72" height="72" alt="" />

# Reamer Support

**Found something wrong with Reamer? This is where you tell me.**

[Website](https://reamerlabs.com) · [Docs](https://reamerlabs.com/docs) · [Execution Spec](https://reamerlabs.com/spec) · [Benchmarks](https://reamerlabs.com/benchmark)

</div>

---

This isn't the source repo — Reamer's source isn't public. This repo exists for one reason: to give bugs, wrong results, and confusing docs a place to land where the fix and the follow-up are visible, not just handled quietly over email.

## What Reamer is

Two closed-source products for institutional mid-frequency trading, each shipped as a stable C ABI and a precompiled binary — no source, no build-from-source, ever:

- **Reamer Research** — a deterministic backtesting engine. A C ABI and shared library, not a program you run: you write a program that builds a strategy vtable and calls `reamer_research_run_backtest()`. Any language that can call a C ABI can drive it; worked examples ship in C++ and Python. Determinism is the property to evaluate — a run with a fixed `rng_seed` is byte-identical across repeats, verified against a published execution specification and a large conformance suite.
- **Reamer Server** — the execution path between a strategy and a venue. A C ABI plus an out-of-process strategy-socket protocol for extension; customers implement a gate and broker connector against the shipped header.

Evaluation kits and licensing are institutional, contact-based — no self-serve or free tier. Full details at [reamerlabs.com](https://reamerlabs.com).

## Report something

- **Open an issue here** — a wrong fill, a result that doesn't match the spec, a docs page that's misleading, a crash, anything. Include what you ran and what you expected vs. what happened; the more specific, the faster it gets fixed.
- **Email:** support@reamerlabs.com
- **DM on X:** @j0osman

## What happens after you report something

I read every one of these myself — no ticket queue, no support team standing between you and the person who wrote the execution engine. If it's real, I fix it, and I say so here (or wherever you reported it) once it's shipped: what was wrong, what changed, and that it's safe to retest. If it's not a bug, I'll say that too, and why.

Bugs happen. What matters is whether they get found and fixed, or found and buried. This repo is the record of the first one.

## Before you report

- Check the [docs](https://reamerlabs.com/docs) and [execution spec](https://reamerlabs.com/spec) first — a lot of "is this a bug" questions are answered by the spec's explicit tie-breaking and fill-price rules.
- Include which product (Research or Server), the version, your OS, and the language of the reference example you're using, if relevant.
