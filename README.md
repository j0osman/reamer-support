<div align="center">
<img src="https://reamerlabs.com/reamer-mark.png" width="72" height="72" alt="" />

# Reamer Labs Support

**Found something wrong with Reamer Research or Reamer Server? This is where you tell me.**

[Website](https://reamerlabs.com) · [Reamer Research](https://reamerlabs.com/products/reamer-research) · [Reamer Server](https://reamerlabs.com/products/reamer-server) · [Pricing](https://reamerlabs.com/pricing) · [FAQ](https://reamerlabs.com/faq)

</div>

---

This isn't a source repo. Both products are closed-source. This repo exists for one reason: to give bugs, wrong results, and confusing docs a place to land where the fix and the follow-up are visible, not just handled quietly over email.

## What Reamer Labs makes

Two products for systematic quants who write their own code and trade mid-frequency strategies on bars, held from minutes to days, whether independent or at a firm. Each ships as a stable C interface and a precompiled library that runs on your own machine.

- **Reamer Research** is a deterministic backtesting engine. You call it from Python, C++, or any language that can call C. The same data, settings and seed give byte-identical results on every run, with fills, slippage and spread defined by a written execution specification that ships in the kit.
- **Reamer Server** is an order management engine that takes a strategy live. It holds order state and sequencing, runs your own pre-trade check on every order, and sends accepted orders to your broker through a connector you write.

Both are self-serve: buy a 30-day trial or an annual licence at [reamerlabs.com/pricing](https://reamerlabs.com/pricing) and the key and kit arrive by email. Not sure if they fit? Start with the [FAQ](https://reamerlabs.com/faq).

## Report something

- **Open an issue here.** A wrong fill, a result that doesn't match the spec, a misleading doc, a crash, anything. Include what you ran and what you expected vs. what happened; the more specific, the faster it gets fixed.
- **Email:** support@reamerlabs.com, weekdays 09:00–18:00 IST (UTC+5:30).
- **DM on X:** @j0osman

## What happens after you report something

I read every one of these myself. No ticket queue, no support team standing between you and the person who wrote both products. If it's real, I fix it, and I say so here (or wherever you reported it) once it's shipped: what was wrong, what changed, and that it's safe to retest. If it's not a bug, I'll say that too, and why.

Bugs happen. What matters is whether they get found and fixed, or found and buried. This repo is the record of the first one.

## Before you report

- Check the docs in your kit first, especially `EXECUTION_SPEC.md` for Reamer Research. A lot of "is this a bug" questions are answered by its explicit tie-breaking and fill-price rules.
- Include which product, the version, your OS, and the language you're calling it from.
- Never paste your licence key into a public issue. Email it instead.
