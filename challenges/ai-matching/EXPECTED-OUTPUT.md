# Expected Output and Behaviors

Return a JSON object with `match_score` (0–100), `recommendation` (`PASS`, `REVIEW` or `FAIL`), `must_haves_met`, `must_haves_missing`, `location_fit` (`status` and `reason`), `compensating_evidence`, `critical_gaps`, `evidence` (requirement/evidence pairs), and `summary`. Additional fields are welcome if documented. Use the [example output](examples/example-output.json) as an illustration.

`PASS` means score ≥ 70 under this challenge's reference threshold and indicates further human review, not an offer or hiring decision. `REVIEW` may flag a borderline or uncertain case under a documented method. `FAIL` indicates insufficient match. The 70 threshold is a challenge convention, not a universal scientific fact. A recommendation should be consistent with the score and any critical gap.

## Public behavioral cases

| Case | Scenario | Expected behavior |
| --- | --- | --- |
| A | Bridgeable Gap | Direct domain experience is missing, but strong adjacent responsibility can compensate; do not auto-reject. |
| B | Critical Gap | Keyword overlap is high while a critical capability is absent; reflect the gap materially. |
| C | Transferable Experience | A different title masks similar duties; favor demonstrated work over title similarity. |
| D | Location Conflict | Professional fit is strong but the commute or work mode conflicts; report each dimension separately. |
| E | Keyword Rich / Reality Weak | Many job terms appear without depth of practice; avoid a high score from vocabulary alone. |
| F | Keyword Light / Reality Strong | Different wording describes the needed work; recognize the underlying capability. |
| G | Critical Requirement With Evidence | A critical requirement is supported by concrete experience, not merely a skills entry. |
| H | Adjacent Industry | Skills from a nearby industry transfer to the role; explain both the bridge and residual gap. |
| I | Remote Compatibility | Geographic distance is irrelevant to a fully remote role when work preferences align. |
| J | Unsupported Claim | A skill is listed without supporting work history; mark evidence as weak or uncertain. |

The [reference cases](data/reference-cases.json) identify job/candidate pairs for A–J. They are public behavioral tests, not a table of exact target scores.
