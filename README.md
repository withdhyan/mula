# Mūla — your values, on your side

*mūla (मूल) — Sanskrit: root.*

Every app you use profiles you — the feed for your attention, the store for your wallet, all of it optimized for engagement, none of it for you. **Mūla is the other thing: an AI that learns what you actually value, writes it into cards you keep, and works for no one but you.** We call the underlying idea **meaning-maxxing**: AI built to maximize meaning instead of engagement or productivity.

A value card is short, specific, and arguable — not a horoscope:

> **Let them feel the small failures** · *When my kid struggles* — noticing my urge to rush in, and asking whether this fall is one of the ones that teaches.

You endorse, edit, or toss every card. Tossed means deleted — actually deleted.

## Use it — two ways, pick one

### 1. In your own agent (available now, fully local)

If you run an AI agent that supports skills (Claude Code and compatible harnesses), the entire wallet runs on your machine — cards as markdown in your own repo, nothing leaves your device, no account, no server, no us.

```bash
mkdir -p ~/.claude/skills/mula
curl -o ~/.claude/skills/mula/SKILL.md \
  https://raw.githubusercontent.com/withdhyan/mula/main/skill/SKILL.md
```

Then say `/mula` to your agent. Two or three 15-minute interviews produce your first endorsed cards. The skill's rules — per-card endorsement, hard deletion, privacy as an absolute — are in [`skill/SKILL.md`](./skill/SKILL.md).

### 2. The hosted wallet (waitlist)

For everyone who doesn't live in a terminal: the same interview and wallet as a website — cards encrypted at field level (ciphertext even to us), export or delete everything in one tap, consent in four separate logged layers. Waitlist at **[withdhyan.github.io/mula](https://withdhyan.github.io/mula/)** (mula.co soon).

## How it works

- **[WHITEPAPER.md](./WHITEPAPER.md)** — the architecture: value cards and the elicitation method (built on the Meaning Alignment Institute's published Moral Graph Elicitation research), the sovereignty ladder ("crypto enters where trust exits"), and what we'll never do: no ads, no token, no data resale.
- **[The site](https://withdhyan.github.io/mula/)** — includes the system diagram: where your data actually lives, and the ladder from today's hosted wallet to keys-on-your-device to no-operator-at-all.

## How we build

In public, with pre-registered honesty. The company runs on an open-source agent stack; decisions and mistakes become public as we go. Where Mūla goes next is a sealed, pre-registered experiment — hypothesis, methods, and kill criteria hash-stamped (`ddbe9cd`) before we started. Results will be published, pass or fail. Until then we claim nothing beyond the wallet.

## This repo

| Path | What it is |
|---|---|
| [`skill/SKILL.md`](./skill/SKILL.md) | The agent skill — the fully local wallet |
| [`WHITEPAPER.md`](./WHITEPAPER.md) | Architecture + research grounding, v0.1 |
| [`index.html`](./index.html) | The site (served via GitHub Pages) |
| [`LICENSE`](./LICENSE) | MIT |

Status: pre-launch. Built by [Holon Research](https://holonresear.ch). Issues and corrections welcome — the whitepaper is versioned in the open.
