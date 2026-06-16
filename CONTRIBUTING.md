# Contributing to /enhance

Thank you for considering a contribution. This project exists to make prompt engineering accessible to everyone, and every contribution — from typo fixes to entirely new techniques — moves that mission forward.

## Ways to contribute

There are five ways to contribute, in roughly increasing order of effort:

### 1. Report a bug or unclear behaviour
If `/enhance` produces something unexpected, file an issue using the bug report template. Include the raw prompt you sent and the output you received.

### 2. Suggest a new technique
Found a prompt engineering technique not yet included? Open a feature request issue and link the source (paper, guide, blog post). The bar is: the technique must come from a credible source and demonstrably improve outputs.

### 3. Add a worked example
Examples are the most valuable contribution after techniques themselves. If you have a domain `/enhance` doesn't cover well — academic writing, sales emails, theology, music production, fitness coaching — write up a worked example showing raw prompt, enhanced prompt, and which techniques fired. Add it to `examples/` and open a PR.

### 4. Translate
The command is currently in English. Portuguese and Spanish translations are welcomed. Other languages are equally valuable. Keep the technique names in their original form (Chain-of-Thought, Tree of Thoughts, etc) since they are proper nouns in the literature.

### 5. Improve the core command
Changes to `commands/enhance.md` itself are the highest-impact contributions and require the most care. Open a discussion issue before submitting a PR for these — major changes should have community input first.

## Pull request process

1. Fork the repository
2. Create a branch named after your change: `feat/new-technique-name` or `fix/typo-in-readme`
3. Make your changes
4. Update relevant documentation (especially `docs/techniques.md` if you add a technique)
5. Update `CHANGELOG.md` under "Unreleased"
6. Submit the PR using the template
7. Wait for review — usually within 48 hours

## What we look for in PRs

- **Clarity** — Can a stranger understand what changed and why from the PR description alone?
- **Scope** — Does the PR do one thing? Multi-purpose PRs are harder to review and more likely to be rejected.
- **Sources** — Are new techniques backed by credible references?
- **Tone** — Is the documentation written in clear British English (or Portuguese / Spanish for translated files)?
- **No personal data** — No API keys, no personal file paths, no real names other than the contributor's.

## Code of conduct

By contributing you agree to abide by the [Code of Conduct](CODE_OF_CONDUCT.md). In short: be kind, be patient, be specific.

## Questions?

Open an issue with the label `question` or start a discussion. There are no stupid questions, only unwritten documentation.
