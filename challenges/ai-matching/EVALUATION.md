# Evaluation Framework

There is no official leaderboard or measured benchmark yet. The [reference cases](data/reference-cases.json) are public behavioral tests. A future held-out **synthetic** evaluation set could test generalization, but none is claimed here.

Reviewers should assess:

| Dimension | What good performance shows |
| --- | --- |
| Must-have reasoning | Separates supported, missing and partially bridged requirements. |
| Critical-gap detection | Detects an essential capability with no convincing evidence despite keyword overlap. |
| Transferable-experience reasoning | Recognizes comparable responsibilities under different titles or industries. |
| Evidence grounding | Points to specific candidate experience and distinguishes claims from practice. |
| Location/work-mode reasoning | Explains onsite, hybrid or remote compatibility independently of capability. |
| Explainability | Provides a concise, auditable account of score and recommendation. |
| Consistency | Applies similar reasoning to similar cases and keeps score and recommendation aligned. |
| Resistance to keyword gaming | Does not reward repeated terms without demonstrated depth. |

Exact agreement with a numeric score is less useful than correct behavior and defensible evidence. Review across all cases, including uncertainty and failure modes. Human reviewers should examine results before any recruitment decision.
