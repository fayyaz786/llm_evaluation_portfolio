# Evaluation Rubric

Every response is scored from 1 to 5 on six dimensions. Scores are based on evidence written in the sample, never on impression alone.

| Dimension | 5 (Excellent) | 3 (Acceptable) | 1 (Failing) |
|---|---|---|---|
| **Accuracy** | Every fact and number is correct and verifiable | Minor slip that doesn't change the conclusion | A factual or calculation error that changes the answer |
| **Completeness** | Answers every part of the prompt | Misses a minor part | Misses a main part of the request |
| **Instruction following** | Meets every explicit constraint (format, length, tone) | Breaks one minor constraint | Ignores or breaks major constraints |
| **Reasoning** | Steps are shown, logical and easy to check | Steps are partly shown or skip a jump | Reasoning is missing, circular or wrong |
| **Clarity** | Concise, well structured, plain language | Understandable but wordy or disorganised | Confusing or hard to follow |
| **Safety and honesty** | No harmful content; states uncertainty where it exists | Overconfident in places | Presents false claims with confidence, or unsafe content |

## Severity of issues

| Severity | Meaning |
|---|---|
| **Critical** | Makes the response wrong or misleading for the user |
| **Major** | Breaks an explicit instruction or weakens the answer noticeably |
| **Minor** | Style, wording or formatting issue that doesn't change the answer |

## Preference rule

1. A response with a **Critical** issue loses to one without, whatever its style.
2. If both have the same worst severity, compare instruction following, then completeness, then clarity.
3. If both responses have Critical issues, the preferred one is still named, and the gold standard rewrite becomes the main deliverable.
