<p align="center">
  <img src="https://raw.githubusercontent.com/0xkurious/usufruct-protocol/main/media/github/usufruct-banner.png" alt="usufruct" width="100%" />
</p>

<p align="center">
  <a href="https://usufruct.io">usufruct.io</a> &nbsp;·&nbsp;
  <a href="https://sdk.usufruct.io">sdk.usufruct.io</a> &nbsp;·&nbsp;
  <a href="https://discord.gg/aQpBtnE6v">Discord</a>
</p>

---

Renting an asset doesn't have to lock it.

**usufruct** separates the right of use from the asset — the *usus* trades independently, so the market stays open while someone is using it. A new primitive for Sui: integrate once, get price discovery, Dutch auctions, handovers, and credit curves. The asset never leaves the market.

---

**Always a price.** Idle, auction, occupied — in every state there is a price at which the right of use can be acquired.

**Always liquid.** A challenger can bid at any time. The incumbent keeps access for the handover window; the protocol enforces the guarantee.

**No keeper required.** Every state transition executes lazily on the next transaction. No off-chain coordinator, no cron job, no external dependency.

**Zero external dependencies.** Any Sui object with `key + store` integrates directly — no adapter code, no permission required, no contract rewrite.

---

## Repositories

| | |
|---|---|
| [`usufruct-protocol`](https://github.com/0xkurious/usufruct-protocol) | Move contracts · specs · `llms.txt` · playground |
| [`usufruct-io-landing-page`](https://github.com/UsufructProtocol/usufruct-io-landing-page) | usufruct.io landing page |

---

<p align="center">
  <sub>Live on Sui testnet &nbsp;·&nbsp; SDK coming &nbsp;·&nbsp; Apache 2.0</sub>
</p>
