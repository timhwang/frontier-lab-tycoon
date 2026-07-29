# FRONTIER LAB TYCOON

**Episode 0 — The Trade.** A Paradox-style spreadsheet game about the central bind of running a frontier AI lab: one fleet of GPUs, two jobs. Every H100e serving your shipped model is one not training the next one.

**[▶ Play it here](https://timhwang.github.io/frontier-lab-tycoon/)**

## The game

You run a frontier lab through one 26-week half. Your shipped model (ATLAS-1) earns revenue and grows demand when you give it inference compute; your next model (ATLAS-2) needs training compute and pays a guaranteed +20 capability the day it ships. One slider divides the fleet between them.

**Win:** ship ATLAS-2, then hold service until H1 ends (W26).

**Lose:**
- **Insolvency** — cash hits $0.
- **Obsolescence** — rivals improve every week; sit 15+ capability points behind the frontier for 6 straight weeks and you're acquired for parts.
- **Service Collapse** — rate-limit your users (utilization > 97%) for 4 consecutive weeks, at any point, and they leave for good.

Traffic spikes and rival breakthroughs arrive without warning. The hard call is always the same: eat the churn, or raid the training run.

## Controls

The game starts paused. **STEP ▸** advances one week — recommended for a first run. **▸ 1×** runs in real time (about 3 seconds per week); pause any time. A skippable tutorial plays on first visit (**? HELP** replays it).

## Development

The whole game is one dependency-free HTML file: [`index.html`](index.html). Open it in a browser and it runs.

An unfinished **Episode 1 — The Allocation Problem** (research allocation, researcher morale and attrition, loss spikes, cloud leases, poaching raids, random events, price and comp policy) ships in the same file but is hidden from the UI; open the console and call `startGame('full')` to try it.

🤖 Built with [Claude Code](https://claude.com/claude-code)
