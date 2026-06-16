# Example — Code task

## Raw prompt

```
fix my python script that's not working
```

## Issues with this prompt

- Vague action verb
- No code attached or referenced
- No description of what "not working" means
- No persona assigned
- No format specified for the response
- No success criteria

## Enhanced output (via `/enhance`)

> You are a senior Python developer with deep experience in debugging, refactoring, and writing maintainable code.
>
> **Task:** Diagnose and fix the bug in the Python script I am about to paste, then explain the fix clearly.
>
> **Audience:** A developer with intermediate Python knowledge who needs to understand both the fix and the underlying cause so they avoid the same mistake in future.
>
> **Context to be provided in next message:**
> - The full script
> - The exact error message or unexpected behaviour
> - What I expected to happen
> - The Python version and any relevant dependencies
>
> **Reasoning approach:** Before suggesting a fix, walk through the script line by line and identify what each part is doing. State your hypothesis about the bug. Then verify by tracing the execution mentally. Only after that, propose the fix.
>
> **Output format:**
> 1. **Diagnosis** — one paragraph explaining the root cause
> 2. **Fixed code** — the corrected script as a single code block
> 3. **Diff explanation** — bullet list of what changed and why
> 4. **Prevention tip** — one practice that would have caught this earlier
>
> **Failure guards:**
> - If you cannot reproduce the bug from the description provided, ask clarifying questions rather than guessing
> - If there are multiple possible causes, list all of them and explain how to differentiate
> - Do not suggest installing new dependencies unless the bug genuinely requires it

## Techniques applied

- ✅ Action verb precision ("Diagnose and fix")
- ✅ Expert persona assignment
- ✅ Goal-first framing
- ✅ Target audience declaration
- ✅ Output format declaration
- ✅ Domain framing (Python)
- ✅ Chain-of-Thought trigger (line-by-line trace)
- ✅ Failure mode guards (asking questions, multiple causes)
- ✅ Positive instruction framing
- ✅ Multi-turn conversation design (next-message context)
