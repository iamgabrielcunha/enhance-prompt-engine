# /enhance — Prompt Enhancement Engine for Claude Code

> Transform rough prompts into production-ready, technique-enriched instructions in seconds. Powered by 16 prompting techniques from DAIR.AI and Google Cloud.

![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)
![Claude Code](https://img.shields.io/badge/Claude-Code-orange.svg)
![Version](https://img.shields.io/badge/version-1.0.0-green.svg)
![Status](https://img.shields.io/badge/status-active-success.svg)

---

note that I'm new to github repo and welcome feedback

## The problem

You know what you want Claude to do, but you're not getting the output you need. Most people send vague, underpowered prompts and accept mediocre results. Even experienced users default to "help me with X" instead of engineering their prompts properly.

The cost is invisible but enormous: time wasted on re-prompting, outputs that miss the mark, and tasks that should take minutes taking hours.

## The solution

`/enhance` is a Claude Code slash command that runs a full prompt engineering pipeline on any rough prompt you give it. It reads your skills, agents, and memory files, classifies your task, applies the right techniques from the academic and industry literature, and returns:

- A fully engineered, production-ready prompt
- A missing context checklist
- A multi-step prompt chain with explicit input → output handoffs
- Three alternative phrasings (APE technique)
- A Reflexion self-critique identifying remaining weaknesses

All in one command. All in seconds. All for free.

## Demo

![Demo](assets/demo.gif)

*Coming soon*

---

## Quick install

```bash
mkdir -p ~/.claude/commands
curl -o ~/.claude/commands/enhance.md \
  https://raw.githubusercontent.com/iamgabrielcunha/enhance-prompt-engine/main/commands/enhance.md
```

That's it. Open Claude Code and type:

```
/enhance write a contract review memo for a client
```

Watch it engineer your prompt before sending.

---

## How it works

`/enhance` runs a five-phase pipeline before showing you anything:

| Phase | What it does | Technique source |
|-------|--------------|------------------|
| **1A — Ecosystem Scan** | Reads your `~/.claude/`, skills, agents, Obsidian vault, and project files | ReAct (DAIR.AI) |
| **1B — Task Classification** | Categorises your prompt against 10 task types | Task Taxonomy (Google Cloud) |
| **1C — Knowledge Generation** | Generates domain expertise before enhancing | Generate Knowledge (DAIR.AI) |
| **1D — Tree of Thoughts** | Drafts 3 enhancement paths and synthesises the best | Tree of Thoughts (DAIR.AI) |
| **1E — Quality Checklist** | Audits the raw prompt against 13 quality criteria | Google Cloud strategies |
| **Phase 2 — CoT Reasoning** | 10-step mandatory reasoning chain | Chain-of-Thought (DAIR.AI) |
| **Phase 3 — Output** | Delivers enhanced prompt, chain, APE alternatives, Reflexion critique | Multiple |

The full technique reference is in [docs/techniques.md](docs/techniques.md).

---

## Usage examples

Three worked examples are included in [`examples/`](examples/):

- [Legal analysis prompt](examples/legal-prompt.md) — UK commercial contract review
- [Code task](examples/code-task.md) — debugging a Python function
- [Research task](examples/research-task.md) — multi-source comparative analysis

Each example shows the raw prompt, the enhanced output, and which techniques fired.

---

## Why this exists

I built `/enhance` because I was tired of getting mediocre outputs from a model I knew could do much better. I'm a law student and a small business owner — I use Claude for everything from contract analysis to sales strategy to theology study. Each domain demands different prompting techniques, and I was spending more time formulating prompts than actually working.

I read every page of the [DAIR.AI Prompt Engineering Guide](https://www.promptingguide.ai/) and the [Google Cloud Prompt Engineering Guide](https://cloud.google.com/discover/what-is-prompt-engineering). I distilled both into a single Claude Code command. This is the result.

---

## Documentation

- 📖 [Installation guide](docs/installation.md)
- 🛠 [Usage guide](docs/usage.md)
- 🧠 [Full technique reference](docs/techniques.md)

## Contributing

I welcome contributions. New techniques, better examples, prompt chains for new domains, translations into other languages — all are appreciated. See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

## Roadmap

- [ ] Add demo GIF
- [ ] Add examples for theological study, BJJ strategy, business planning
- [ ] Add Portuguese and Spanish translations of the command
- [ ] Add an `/enhance-quick` variant for shorter, faster runs
- [ ] Add integration with project-specific `CLAUDE.md` files

## Credits

This project stands on the shoulders of two extraordinary open resources:

- **[DAIR.AI Prompt Engineering Guide](https://www.promptingguide.ai/)** — for the academic technique foundation
- **[Google Cloud Prompt Engineering Guide](https://cloud.google.com/discover/what-is-prompt-engineering)** — for the practical strategy layer

Built for [Claude Code](https://www.anthropic.com/claude-code) by Anthropic.

## Licence

MIT — see [LICENSE](LICENSE).

---

*If `/enhance` saves you time, consider giving the repo a star. It is the single most useful signal for future contributors deciding whether to invest their effort.*
