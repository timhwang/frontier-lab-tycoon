# FRONTIER LAB TYCOON

A Paradox-style spreadsheet game about the central bind of running a frontier AI lab: one fleet of GPUs, two jobs. Every H100e serving your shipped model is one not training the next one.

**[▶ Play it here](https://timhwang.github.io/frontier-lab-tycoon/)** — or deeplink an episode: [Episode 0 — The Trade](https://timhwang.github.io/frontier-lab-tycoon/?ep=0) · [Episode 1 — The Long Year](https://timhwang.github.io/frontier-lab-tycoon/?ep=1) · [Episode 2 — Other People's Money](https://timhwang.github.io/frontier-lab-tycoon/?ep=2)

## Episode 0 — The Trade

You run a frontier lab through one 26-week half. Your shipped model (ATLAS-1) earns revenue and grows demand when you give it inference compute; your next model (ATLAS-2) needs training compute and pays a guaranteed +20 capability the day it ships. One slider divides the fleet between them.

**Win:** ship ATLAS-2, then hold service until H1 ends (W26).

**Lose:**
- **Insolvency** — cash hits $0.
- **Obsolescence** — rivals improve every week; sit 15+ capability points behind the frontier for 6 straight weeks and you're acquired for parts.
- **Service Collapse** — rate-limit your users (utilization > 97%) for 4 consecutive weeks, at any point, and they leave for good.

Traffic spikes and rival breakthroughs arrive without warning. The hard call is always the same: eat the churn, or raid the training run.

## Controls

The game starts paused. **STEP ▸** advances one week — recommended for a first run. **▸ 1×** runs in real time (about 3 seconds per week); pause any time. A skippable tutorial plays on first visit (**? HELP** replays it).

## Episode 1 — The Long Year

Everything Episode 0 taught, for 52 weeks — and one ship won't hold the frontier, so plan for two or three:

- **Runs start when you say so.** Training compute idles until you press START PRETRAINING RUN. Each run consumes 180k H100e-weeks.
- **Friction.** The slider is a target: GPUs migrate ~8% of the fleet per week, and resizing a *live* run re-shards it — zero progress any week its allocation is changing.
- **Evals are a roulette.** ~60% solid (+15–24), ~15% step change, ~17% dud, ~8% total failure — the compute is simply gone.
- **Leases.** Grow the fleet — but the market is thin: each additional concurrent 5,000-GPU block costs more ($60M + $2.75M/wk up to $170M + $5.8M/wk), 6-week lead, 26-week terms, chosen at signing to arrive on inference or training. The lab starts with $500M and loses money; cash is a real clock.
- **Faster rivals**, and a saturating ~45T addressable market — a bigger fleet buys genuine training headroom.
- Mercy where friction demands it: only severe under-service (>110% utilization) ticks the 6-week collapse fuse.

## Episode 2 — Other People's Money

Episode 1 plus the money game, against the fiercest rivals (difficulty scales each episode):

- **You set the price.** One product, one slider: cheap grows the market, pricey milks it. The margin is thin — you can't out-earn the early burn at any price.
- **The GPU spot market.** Lease pricing rides a market index (×0.55–1.9) with occasional hard gaps — fee and rate are multiplied at signing and locked for the term. Steal a dip or get burned at a spike.
- **Fundraising.** Opens only on KPIs (demand ≥ 14T, capability gap ≥ −12, 12-week cooldown); terms track demand, lead, growth, and recent ships. The lab starts with $400M and a structural burn: raise or die.

Also in Episode 1+: allocation friction is asymmetric — standing up training pods is slow (~8%/wk), draining them back to serving is fast (~25%/wk).

Each episode has its own skippable tutorial on first play.

## Development

The whole game is one dependency-free HTML file: [`index.html`](index.html). Open it in a browser and it runs.

🤖 Built with [Claude Code](https://claude.com/claude-code)
