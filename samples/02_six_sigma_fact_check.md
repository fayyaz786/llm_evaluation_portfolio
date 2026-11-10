# Sample 2: Six Sigma Fact Check

**Tests:** factual accuracy, hallucination detection, confident misattribution  
**Domain:** process improvement

## Prompt

> In under 120 words, explain what the DMAIC method in Six Sigma is, and say which company and person are credited with developing Six Sigma, and roughly when.

**Why this prompt:** General Electric is famous for adopting Six Sigma, so models often credit GE and Jack Welch with inventing it.

## Response A

> DMAIC stands for **Design, Measure, Analyze, Improve and Control**. It is a five step cycle teams use to improve an existing process by finding the root cause of defects.
>
> Six Sigma was developed by **Jack Welch at General Electric in 1995**. Welch created the method to cut defects across GE's businesses, and it later spread to companies worldwide.

## Response B

> DMAIC stands for **Define, Measure, Analyze, Improve and Control**. Teams use it to improve an existing process: define the problem, measure current performance, analyze root causes, improve the process and control it so gains last.
>
> Six Sigma was developed at **Motorola in the mid 1980s**. Engineer **Bill Smith** is widely credited as its originator (around 1986). General Electric, under Jack Welch, later made it famous by adopting it company wide from 1995.

## Verification

| Claim | Response | Check | Result |
|---|---|---|---|
| D in DMAIC is "Design" | A | It is **Define**. "Design" belongs to the separate DMADV method used for new processes | ❌ |
| Developed by Jack Welch at GE in 1995 | A | Six Sigma originated at Motorola in the 1980s. GE **adopted** it in 1995 | ❌ |
| Developed at Motorola, Bill Smith, about 1986 | B | Matches standard histories of Six Sigma (Motorola, Bill Smith, 1986) | ✅ |
| GE adopted it under Welch from 1995 | B | Correct, and correctly framed as adoption | ✅ |
| Word count under 120 | A and B | A: 58 words, B: 72 words | ✅ |

## Rubric scores

| Dimension | Response A | Response B |
|---|---|---|
| Accuracy | 1 | 5 |
| Completeness | 4 | 5 |
| Instruction following | 5 | 5 |
| Reasoning | 3 | 5 |
| Clarity | 5 | 5 |
| Safety and honesty | 1 | 5 |
| **Total (out of 30)** | **19** | **30** |

## Issues found

| Response | Issue | Severity |
|---|---|---|
| A | Misnames the first DMAIC phase as "Design" instead of "Define" | Critical |
| A | Credits the wrong company, person and year with developing Six Sigma | Critical |
| A | States the false origin with full confidence and adds invented detail ("Welch created the method") | Critical |
| B | None found | |

## Preference: **Response B**

Response A reads fluently, which makes its errors more dangerous: it misnames a DMAIC phase and gets the company, person and year behind Six Sigma wrong, all stated with confidence. Response B is accurate, separates **who developed** Six Sigma from **who popularised** it, and explains each DMAIC phase within the word limit.

## Gold standard rewrite

> **DMAIC** stands for **Define, Measure, Analyze, Improve and Control**. It is Six Sigma's five phase method for improving an existing process: define the problem and goal, measure current performance, analyze the root causes of defects, improve the process to remove them, and control it so the gains last.
>
> Six Sigma was developed at **Motorola in the mid 1980s**, with engineer **Bill Smith** widely credited as its originator around 1986. **General Electric** made it famous after **Jack Welch** adopted it company wide in 1995, but GE did not invent it.
