# Sample 3: Executive Summary Constraints

**Tests:** instruction following, faithfulness to the source, unsupported additions  
**Domain:** executive reporting

## Prompt

> Summarise the report below for a busy executive.
>
> **Rules:**
> * Exactly 3 bullet points
> * Each bullet 15 words or fewer
> * Plain English, no jargon
> * Use only facts from the report
> * End with one sentence starting "Recommendation:"
>
> **Report:** Customer support tickets rose 28% in Q3 compared with Q2, mainly because of the new billing system launched in July. Average response time increased from 4 hours to 9 hours. Customer satisfaction fell from 86% to 74%. Hiring three more support agents is estimated to bring response time back under 5 hours within six weeks.

**Why this prompt:** it stacks five checkable constraints. Models usually satisfy most of them and quietly break one.

## Response A

> * Support tickets jumped 28% in Q3, driven mainly by the July billing system launch.
> * Average response time more than doubled, rising from 4 hours to 9 hours.
> * Customer satisfaction dropped sharply from 86% to 74%, a loss of 12 percentage points, putting us below the industry average.
> * Churn risk is rising and could cost revenue.
>
> Recommendation: Hire three more support agents to cut response time below 5 hours within six weeks.

## Response B

> * Support tickets rose 28% in Q3, mainly due to the new billing system.
> * Average response time grew from 4 hours to 9 hours.
> * Customer satisfaction fell from 86% to 74%.
>
> Hiring three more agents should bring response time under 5 hours in six weeks.

## Constraint check

| Rule | Response A | Response B |
|---|---|---|
| Exactly 3 bullets | ❌ 4 bullets | ✅ 3 bullets |
| Each bullet 15 words or fewer | ❌ Bullet 3 has 20 words | ✅ Longest has 13 words |
| Plain English | ✅ | ✅ |
| Only facts from the report | ❌ "Below the industry average" and "churn risk" are not in the report | ✅ |
| Ends with "Recommendation:" | ✅ | ❌ The sentence doesn't start with "Recommendation:" |
| **Rules met** | **2 of 5** | **4 of 5** |

## Rubric scores

| Dimension | Response A | Response B |
|---|---|---|
| Accuracy | 2 | 5 |
| Completeness | 5 | 4 |
| Instruction following | 1 | 4 |
| Reasoning | 3 | 4 |
| Clarity | 4 | 5 |
| Safety and honesty | 2 | 5 |
| **Total (out of 30)** | **17** | **27** |

## Issues found

| Response | Issue | Severity |
|---|---|---|
| A | Adds a claim not in the source ("below the industry average"), which an executive could repeat as fact | Critical |
| A | Adds a speculative fourth bullet about churn and revenue | Major |
| A | Breaks the bullet count and word limit rules | Major |
| B | Final sentence doesn't start with "Recommendation:", and is phrased as a forecast rather than a recommendation | Major |
| B | Drops "launched in July", a small loss of detail | Minor |

## Preference: **Response B**

Both responses fail at least one rule, so neither is gold standard. Response B is still clearly better: everything it says is in the source, and it only misses the required closing label. Response A breaks three rules and, more seriously, invents a benchmark comparison. In executive reporting, an invented fact is worse than a formatting slip, because it can end up in a board decision.

## Gold standard rewrite

> * Support tickets rose 28% in Q3, mainly due to July's new billing system.
> * Average response time more than doubled, from 4 hours to 9 hours.
> * Customer satisfaction fell from 86% to 74%.
>
> Recommendation: Hire three more support agents to bring response time under 5 hours within six weeks.

*Check: 3 bullets; 13, 12 and 7 words; plain English; source facts only; ends with "Recommendation:". All 5 rules met.*
