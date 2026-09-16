# The AI Matching Challenge

Traditional recruitment matching often relies too heavily on keyword overlap. Real recruitment decisions are more complex. Candidate A may lack an explicitly named domain requirement while having adjacent experience that reasonably compensates. Candidate B may repeat nearly every keyword while lacking a genuinely critical capability. The challenge is to distinguish these situations.

## Input and output

A system receives one `job` and one `candidate` from the synthetic data set. It returns a structured, explainable assessment, using the fields in [EXPECTED-OUTPUT.md](EXPECTED-OUTPUT.md). Ground claims in the supplied experience rather than a title or skill list alone. Identify uncertainty when evidence is thin.

## Three core dimensions

### 1. Must-Have Requirements

Identify which essential requirements are supported by actual experience and which are missing. One missing must-have must not automatically disqualify a candidate. Examine whether relevant or transferable responsibility can bridge the gap. A critical capability with no credible bridge should materially affect the assessment. Do not confuse a listed skill with evidence that the candidate used it.

### 2. Location Fit

Compare candidate location and work preferences with the job location and onsite, hybrid or remote structure. Keep professional fit distinct from location fit and explain a practical conflict.

### 3. Overall Match

Return a score from 0 to 100. For this challenge, 70 or above is a reference threshold for a candidate generally worth further human review; it is not a universal scientific cutoff. The score supports a decision. It is never an automated hiring decision.

## What Makes This Challenge Different?

We are not looking for “Candidate has 7 out of 10 keywords.” We want reasoning about work performed, responsibility held, capability demonstrated, gaps, adjacent experience and whether evidence is credible. Strong semantic similarity cannot substitute for an essential missing capability.

## Freedom of Approach

There is no required model, provider or technology stack. Use LLMs, embeddings, semantic search, rules, machine learning, knowledge graphs, hybrid systems or another approach. Document how it works and where it may fail. See the [rules](RULES.md), [reference cases](data/reference-cases.json) and [evaluation framework](EVALUATION.md).

How should AI determine whether a person is genuinely suitable for a job — beyond keywords?
