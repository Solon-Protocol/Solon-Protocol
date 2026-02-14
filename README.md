# SOLON Protocol

**An open-source operating system for human coordination.**

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

---

## What is this?

SOLON is a protocol for decentralized governance, transparent resource allocation, and reputation-based cooperation. It combines:

- **Liquid Democracy** — vote directly or delegate to trusted experts, revocable anytime
- **Dual Currency** — Bitcoin (store of value) + Tick (community currency with 1% monthly flow to commons)
- **Heartbeat** — multidimensional reputation via non-transferable Soulbound Tokens
- **Agora** — physical community spaces designed for encounter, not isolation

Read the full **[Whitepaper](WHITEPAPER.md)**.

## Why?

Every political system solves coordination and creates corruption. Every economic system values what can be priced and ignores what matters most. Every labor system couples survival to employment — even as machines replace employment.

SOLON is not a fix. It's an experiment. Open-source, opt-in, forkable.

## Status

🟡 **Pre-alpha.** The whitepaper is published. The code is being built. We need help.

## How to Help

| You are a... | You can... |
|---|---|
| **Solidity developer** | Build and audit smart contracts (Tick, Liquid Democracy, SBTs) |
| **Mobile developer** | Build the Chronos Wallet (React Native / Flutter) |
| **Cryptographer** | Implement ZKP voting and identity modules |
| **Economist** | Model and stress-test the Tick demurrage system |
| **City planner** | Design Agora spatial guidelines |
| **Lawyer** | Explore legal frameworks for community currencies and DAOs |
| **Writer / Translator** | Translate the whitepaper, write documentation |
| **Anyone** | Join the conversation, start a local group, cook dinner |

See **[CONTRIBUTING.md](CONTRIBUTING.md)** for details.

## Project Structure

```
solon-protocol/
├── WHITEPAPER.md          # The full protocol specification
├── CONTRIBUTING.md         # How to help
├── LICENSE                 # MIT License
├── contracts/              # Smart contracts (Solidity)
│   ├── Tick.sol           # Demurrage currency
│   ├── LiquidDemocracy.sol # Voting and delegation
│   └── SoulboundToken.sol  # Heartbeat reputation tokens
├── wallet/                 # Chronos Wallet app
├── docs/                   # Additional documentation
└── simulations/            # Economic models and stress tests
```

## Core Concepts

### The Tick
A community currency. Everyone receives an equal distribution. 1% per month flows automatically to the community pool. You can't hoard it — it's designed to circulate.

### Liquid Democracy
Your voice, your choice. Vote directly on things you understand. Delegate to experts on things you don't. Take your delegation back anytime.

### The Heartbeat
Not a score. Not a ranking. A mosaic of your contributions — craft, care, art, science, community, stewardship — attested by the people who witnessed them. Non-transferable. Non-tradable. Yours.

### The Agora
A physical place. A kitchen, a workshop, a garden. Designed so that paths cross, neighbors meet, and loneliness becomes statistically unlikely.

## Principles

1. **Rules in code, not in contracts.** Smart contracts execute; they don't negotiate.
2. **Transparency of power, privacy of citizens.** The state is glass; the citizen is sovereign.
3. **No delegation without recall.** Trust is a running contract, not a blank check.
4. **Resource consumption is mathematically bounded.** No one prints Ticks. The protocol distributes them.
5. **Incentives, not punishments.** The Heartbeat opens doors. It never closes them.

## The Name

Solon of Athens (638–558 BC) reformed the Athenian constitution, cancelled debts, and laid the groundwork for democracy. He then voluntarily left Athens for ten years, so the people would learn to govern themselves rather than depend on him.

The SOLON Protocol follows the same logic: build the tool, then step back.

---

*"I did not write this protocol to be right. I wrote it to start a conversation."*
— SOLON

## License

MIT License. Free to use, modify, distribute. See [LICENSE](LICENSE).
