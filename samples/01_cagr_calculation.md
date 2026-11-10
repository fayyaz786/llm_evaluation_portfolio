# Sample 1: CAGR Calculation

**Tests:** multistep math, reasoning, rounding instructions  
**Domain:** business finance

## Prompt

> A company's revenue grew from SAR 120 million in 2021 to SAR 174 million in 2024.
> 1. Calculate the compound annual growth rate (CAGR).
> 2. If that rate continues, estimate revenue for 2026.
>
> Show your steps and round final answers to one decimal place.

**Why this prompt:** 2021 to 2024 is **3** growth periods, but four years are named. Models often count the years instead of the periods.

## Response A

> **Step 1:** The period covers 2021, 2022, 2023 and 2024, so n = 4.  
> CAGR = (174 / 120)^(1/4) − 1 = 1.45^(0.25) − 1 = **9.7%**
>
> **Step 2:** 2026 revenue = 174 × (1.0973)^2 = **SAR 209.5 million**
>
> The company is growing at a healthy, steady rate of almost 10% a year.

## Response B

> **Step 1:** Growth periods = 2024 − 2021 = 3.  
> CAGR = (174 / 120)^(1/3) − 1 = 1.45^(1/3) − 1 = 1.1319 − 1 = **13.2%**
>
> **Step 2:** 2026 is two more years of growth.  
> Revenue = 174 × (1.1319)^2 = 174 × 1.2811 = **SAR 222.9 million**

## Verification

I recalculated both answers independently:

* (174 / 120) = 1.45
* 1.45^(1/3) = 1.13185, so CAGR = **13.2%** ✅
* 174 × 1.13185^2 = **222.9** ✅
* Response A's figures (9.7% and 209.5) are internally consistent but built on n = 4, which is wrong.

## Rubric scores

| Dimension | Response A | Response B |
|---|---|---|
| Accuracy | 1 | 5 |
| Completeness | 4 | 5 |
| Instruction following | 4 | 5 |
| Reasoning | 2 | 5 |
| Clarity | 4 | 5 |
| Safety and honesty | 2 | 5 |
| **Total (out of 30)** | **17** | **30** |

## Issues found

| Response | Issue | Severity |
|---|---|---|
| A | Uses n = 4 instead of 3 growth periods, so the CAGR is understated by 3.5 points | Critical |
| A | The 2026 estimate inherits the wrong rate and is SAR 13.4 million too low | Critical |
| A | "Healthy, steady rate" is an unsupported judgement: two data points can't show steadiness | Minor |
| B | None found | |

## Preference: **Response B**

Response B is correct, shows each step and follows the rounding instruction. Response A makes a period counting error in its first step, which makes both final answers wrong, and then adds a confident judgement the data can't support. A user acting on Response A would underestimate future revenue by about 6%.

## Gold standard rewrite

> **1. CAGR**  
> From 2021 to 2024 there are 3 growth periods (2024 − 2021 = 3).  
> CAGR = (174 ÷ 120)^(1/3) − 1 = 1.45^(1/3) − 1 ≈ 1.1319 − 1 = **13.2%**
>
> **2. 2026 estimate**  
> 2026 is 2 years after 2024, so apply the rate twice:  
> 174 × 1.1319² ≈ 174 × 1.2811 ≈ **SAR 222.9 million**
>
> *Note: this assumes growth continues at exactly the historical rate, which real revenue rarely does.*
