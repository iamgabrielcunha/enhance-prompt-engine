# Technique Reference

The full catalogue of prompting techniques used by `/enhance`, drawn from the DAIR.AI Prompt Engineering Guide and the Google Cloud Prompt Engineering Guide.

---

## From DAIR.AI (promptingguide.ai)

### 1. Zero-shot prompting
Asking the model to perform a task with no examples. Relies entirely on pretrained knowledge.
**When `/enhance` uses it:** Default fallback when the task is unambiguous and self-contained.

### 2. Few-shot prompting
Providing 2-5 worked input/output examples so the model learns the expected pattern.
**When `/enhance` uses it:** When output format matters significantly (classification, extraction, style matching).

### 3. Chain-of-Thought (CoT)
Prompting the model to show intermediate reasoning steps before producing the final answer.
**When `/enhance` uses it:** Every enhancement runs through a mandatory 10-step CoT reasoning chain in Phase 2.

### 4. Zero-shot CoT
The minimal CoT trigger — appending "Let's think step by step" without examples.
**When `/enhance` uses it:** Added to enhanced prompts where reasoning is needed but few-shot examples are not.

### 5. Meta prompting
Using the model to design, critique, or improve prompts. The model thinks about thinking.
**When `/enhance` uses it:** `/enhance` IS meta prompting. The entire command is the model designing better prompts for itself.

### 6. Self-consistency
Generating multiple independent reasoning paths and selecting the most consistent answer.
**When `/enhance` uses it:** Applied across the Tree of Thoughts paths — if two paths agree an element is essential, it's kept.

### 7. Generate Knowledge
Generating relevant domain knowledge BEFORE attempting the main task.
**When `/enhance` uses it:** Phase 1C generates expert-level domain knowledge before any enhancement is written.

### 8. Prompt Chaining
Breaking a task into sequential subtasks where each output feeds the next prompt as input.
**When `/enhance` uses it:** The output always includes a multi-step prompt chain with explicit handoffs.

### 9. Tree of Thoughts (ToT)
Exploring multiple reasoning branches, evaluating each, and selecting the best path.
**When `/enhance` uses it:** Phase 1D generates 3 enhancement paths and synthesises the strongest.

### 10. ReAct
Interleaving Reasoning and Action. Think, act with a tool, observe the result, think again.
**When `/enhance` uses it:** Phase 1A is a ReAct loop — observe (filesystem) → reason → act (enhance).

### 11. Reflexion
The agent verbally reflects on its own output, identifies what went wrong, and improves.
**When `/enhance` uses it:** Every output includes a Reflexion self-critique identifying 2 weaknesses and fixes.

### 12. Directional Stimulus Prompting (DSP)
Providing a hint, keyword, or cue that steers the model toward the desired answer type.
**When `/enhance` uses it:** Added as keyword anchors when the enhanced prompt risks drifting toward generic output.

### 13. Automatic Prompt Engineer (APE)
Generating and scoring candidate instructions automatically.
**When `/enhance` uses it:** The APE section offers 3 alternative phrasings (direct command, role+task, hypothetical).

### 14. RAG-style context engineering
Retrieving relevant external context and injecting it into the prompt.
**When `/enhance` uses it:** Phase 1A ecosystem scan reads skills, agents, and memory files — a form of RAG.

---

## From Google Cloud

### 15. Action verb precision
Opening prompts with strong, unambiguous action verbs rather than vague openers like "help me".
**When `/enhance` uses it:** Every enhanced prompt is rewritten to open with a strong verb.

### 16. Goal-first framing
Stating the desired deliverable before context or constraints.
**When `/enhance` uses it:** Restructures any prompt where the ask is buried under background.

### 17. Output format declaration
Explicitly declaring structure: prose, bullet list, table, JSON, markdown, code block.
**When `/enhance` uses it:** Every enhanced prompt has explicit format instructions.

### 18. Output length specification
Word count, paragraph count, or item count constraint.
**When `/enhance` uses it:** Always included to prevent bloated or truncated outputs.

### 19. Target audience declaration
Specifying expertise level, role, age, cultural context of the reader.
**When `/enhance` uses it:** Mandatory field in every enhanced prompt.

### 20. Background knowledge injection
Including relevant facts and data directly in the prompt rather than expecting the model to infer them.
**When `/enhance` uses it:** Surfaced as a Missing Context Checklist item every time.

### 21. Expert persona assignment
Assigning Claude a specific expert role ("You are a senior commercial lawyer at a Magic Circle firm").
**When `/enhance` uses it:** Mandatory in every enhanced prompt.

### 22. Positive instruction framing
Saying what TO do, not what NOT to do. "Write concisely" beats "Don't be verbose".
**When `/enhance` uses it:** All negative instructions in enhanced prompts are converted to positive equivalents.

### 23. Failure mode guards
Explicit instructions to address common failure modes (hallucination, uncertainty, scope drift).
**When `/enhance` uses it:** Added for high-stakes domains — legal, medical, financial, factual claims.

### 24. Domain-specific framing
Tagging the domain explicitly (legal, code, creative, theological) to activate the right reasoning mode.
**When `/enhance` uses it:** Phase 1B classifies the task into one of 10 domain types.

### 25. Source and document reference
Anchoring reasoning by referencing specific files, documents, or data sources.
**When `/enhance` uses it:** Pulled from the ecosystem scan — surfaces relevant files to reference by name.

---

## Sources

- **DAIR.AI Prompt Engineering Guide:** https://www.promptingguide.ai/
- **Google Cloud Prompt Engineering Guide:** https://cloud.google.com/discover/what-is-prompt-engineering

Both are extraordinary open resources. If you find this project useful, consider starring their repositories too.
