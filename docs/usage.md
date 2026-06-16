# Usage Guide

## Basic usage

In any Claude Code session, type `/enhance` followed by your raw prompt:

```
/enhance write a contract review memo for a client
```

Claude Code will run the full 5-phase pipeline and return:

1. **Task classification** — what type of prompt this is
2. **Enhanced prompt** — the production-ready rewrite
3. **Missing context checklist** — what you might want to add
4. **Prompt chain** — multi-step sequence with handoffs
5. **APE alternatives** — three different phrasings to try
6. **Reflexion critique** — weaknesses identified and fixed
7. **Alfred's Recommendation** — personal strategic counsel

## When to use `/enhance`

Use it whenever:

- You have a complex task and aren't sure how to phrase it
- You've tried a prompt and the output missed the mark
- You're entering a new domain (legal, code, research) and don't know the best framing
- You want a multi-step workflow rather than a single message
- You're preparing a prompt you'll reuse across many runs

## When NOT to use `/enhance`

Skip it when:

- The task is genuinely simple ("what time is it in Tokyo")
- You already have a refined prompt
- Speed matters more than quality

## Example workflows

### Workflow 1 — Direct use
1. Type `/enhance your raw prompt`
2. Copy the enhanced prompt from the output
3. Send it as a new message to Claude

### Workflow 2 — Prompt chain execution
1. Type `/enhance your task`
2. Use the multi-step chain section
3. Send Prompt 1, take the output
4. Paste into Prompt 2, take the output
5. Continue through the chain

### Workflow 3 — APE comparison
1. Type `/enhance your task`
2. Run all three APE phrasings in separate sessions
3. Compare outputs and pick the strongest

## Tips

**Be specific in the raw prompt.** "Help me with my essay" gives `/enhance` very little to work with. "Help me write a 2000-word essay on Article 267 TFEU for a first-year LLB module" gives it everything.

**Include domain markers.** Mention if it's legal, code, theological, financial, fitness — `/enhance` uses these to activate the right strategy set.

**Use the Missing Context Checklist.** After the enhancement, look at that section. It tells you what would make the prompt even stronger if you add it.

**Re-run if the first output isn't right.** `/enhance` is itself a prompt. If the enhanced version doesn't match what you wanted, re-run with more detail in the raw prompt.

## Troubleshooting

**The command doesn't activate.** Confirm the file is at `~/.claude/commands/enhance.md` with read permissions.

**Output is too long.** Add "Keep your enhancement concise" to your raw prompt, or use the APE phrasing A (direct command) which tends to produce shorter outputs.

**Output misses my ecosystem context.** Check that your Obsidian vault path matches what's referenced in Phase 1A of the command. Edit the path if needed.

**`/enhance` keeps asking clarifying questions.** Your raw prompt was too short — try adding more detail upfront.
