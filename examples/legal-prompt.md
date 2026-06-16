# Example — Legal analysis

## Raw prompt

```
help me write a contract review memo for a commercial lease
```

## Issues with this prompt

- Vague action verb ("help")
- No deliverable specified before context
- No audience declared
- No format or length stated
- No domain framing (which jurisdiction? what type of commercial lease?)
- No persona assigned to Claude
- No failure guards for legal content

## Enhanced output (via `/enhance`)

> You are a senior commercial property solicitor at a London City firm with twelve years of experience in landlord and tenant disputes under the Landlord and Tenant (Covenants) Act 1995.
>
> **Task:** Draft a contract review memorandum analysing a commercial lease for an internal partner.
>
> **Audience:** A partner in the property department who needs a quick risk assessment before advising the client.
>
> **Background context:** This is a standard commercial lease in England and Wales. The tenant is a UK-incorporated retail business. The premises are on a high street in a tier-two city. The lease is for a 10-year term with five-yearly upward-only rent reviews.
>
> **Format and length:** Markdown memo, approximately 1200 words, structured under these exact headers:
> 1. Executive summary (3 bullet points maximum)
> 2. Key commercial terms
> 3. Risk assessment — high, medium, low
> 4. Recommended amendments
> 5. Outstanding questions for the client
>
> **Reasoning approach:** Think through this step by step. Before writing, identify the three highest-risk clauses you would expect in a standard high-street commercial lease, then structure the memo around those.
>
> **Failure guards:**
> - Where you are uncertain about a specific clause, state the uncertainty explicitly rather than asserting a position
> - Do not cite case law unless you can name the case, parties, year, and the specific point of law it establishes
> - Flag any clause that may be unenforceable under the Landlord and Tenant (Covenants) Act 1995

## Techniques applied

- ✅ Action verb precision ("Draft")
- ✅ Goal-first framing
- ✅ Expert persona assignment
- ✅ Target audience declaration
- ✅ Output format declaration
- ✅ Output length specification
- ✅ Background knowledge injection
- ✅ Domain-specific framing (England and Wales)
- ✅ Chain-of-Thought trigger
- ✅ Failure mode guards (hallucination on case law)
- ✅ Positive instruction framing throughout
