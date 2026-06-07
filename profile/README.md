<p align="center"><img src="https://raw.githubusercontent.com/0xkurious/usufruct-protocol/main/media/github/usufruct-banner.png" alt="usufruct" width="100%"/></p>

<p align="center">
  <a href="https://usufruct.io">usufruct.io</a> &nbsp;·&nbsp;
  <a href="https://sdk.usufruct.io">sdk.usufruct.io</a> &nbsp;·&nbsp;
  <a href="https://playground.usufruct.io">playground.usufruct.io</a> &nbsp;·&nbsp;
  <a href="https://discord.gg/aQpBtnE6v">Discord</a>
</p>

---

When you rent something, the asset leaves the market. An apartment listed for rent disappears from results the moment a guest checks in. The right of use — the *usus* — belongs to one holder for the duration, and while it does, the market is closed.

**usufruct** separates the right of use from the asset so the two can trade independently. A rental protocol for Sui objects: integrate once and get price discovery, Dutch auctions, handovers, and credit curves. The asset never leaves the market.

## Why usufruct is different

Most rental markets close when someone checks in. usufruct doesn't.

- **Always a price.** In every state there is a price at which the right of use can be acquired: the rest price at idle, a descending price during the Dutch auction, an escalated price while occupied.
- **Always liquid.** A challenger can bid at any time. The current holder keeps access for the handover window before displacement executes. The window is configured by the governor; the guarantee is enforced by the protocol.
- **Self-correcting.** Competition drives price up. Absence of demand drives it down through a Dutch auction. Both are governed by configurable curves.
- **No keeper required.** State transitions execute lazily on the next transaction that touches the escrow. No off-chain coordinator, no cron job, no external dependency on liveness.
- **Zero external dependencies.** Any Sui object with `key + store` integrates directly — no adapter code, no permission required, no contract rewrite. The package imports only the Sui standard library.

## Playground

Before reading specs or code, build intuition interactively. The [usufruct playground](https://playground.usufruct.io) lets you configure policies, run rental scenarios, and observe how price, credit, and handover mechanics interact — without deploying anything. It is the fastest path from zero to understanding how the eight policy axes compose into different markets.

## `llms.txt` — tell your agent

[`llms.txt`](https://github.com/0xkurious/usufruct-protocol/blob/main/llms.txt) is a self-contained guide for LLM agents. Load it and the agent will build real PTBs against the testnet deployment — wallet, funding, integrate, rent, collect, handover — without reading any Move source.

**With Claude Code:**

```bash
claude   # from the repo root
```

```
@llms.txt  Set up a wallet, integrate the dummy asset, and rent it for one tenure.
           Show the escrow ID once the asset is occupied.
```

**Be curious.** Let the agent walk you through the built-in scenarios, then push further. Ask it to swap ensembles, change the credit shape, reshape the auction curve, crank up the price escalation until a challenger is forced out, or spin up a fleet of escrows under a single cap. Ask what a holder can actually do with the asset once they hold the cap — what PTBs are legal inside a borrow, what other protocols compose. Ask it to pay rent in a different coin, or integrate your own asset instead of the dummy. The guide is the map; the agent drives; the protocol surprises.

---

<p align="center"><sub>Live on Sui testnet &nbsp;·&nbsp; SDK coming &nbsp;·&nbsp; Apache 2.0</sub></p>
