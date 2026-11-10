# LLM Evaluation Portfolio

Public samples of how I evaluate large language model responses: prompt design, side by side ranking, rubric scoring, fact checking and gold standard rewrites.

**Author:** Fayyaz Shahid, AI Trainer and LLM Response Evaluator
**Contact:** [Upwork](https://www.upwork.com/freelancers/~01b0b9c69d62c91200) · [LinkedIn](https://www.linkedin.com/in/fayyazshahid) · [fayyazshahid.com](https://fayyazshahid.com)

---

## Why this repository exists

My client evaluation work is confidential, so I can't share it. This repository shows the same method on prompts I wrote myself, so clients can see how I think, check and write before they hire me.

## How each sample is structured

1. **Prompt:** written to test a specific weakness (calculation, factual recall, instruction following)
2. **Two responses:** Response A and Response B
3. **Rubric scores:** each response scored 1 to 5 on six dimensions (see [RUBRIC.md](RUBRIC.md))
4. **Issues found:** every error, with the evidence and its severity
5. **Preference and justification:** which response wins and why, in a defensible rationale
6. **Gold standard rewrite:** the reference answer a model should have given

> **Note on the responses:** Response A and Response B in each sample were written to reproduce error patterns I regularly see in model output (wrong period counts, confident misattribution, ignored constraints). They are examples for demonstrating the method, not copies of any specific model's output.

## Samples

| # | Sample | What it tests | Key finding |
|---|---|---|---|
| 1 | [CAGR calculation](samples/01_cagr_calculation.md) | Multistep math and reasoning | Response A counts 4 growth periods instead of 3, so every later number is wrong |
| 2 | [Six Sigma fact check](samples/02_six_sigma_fact_check.md) | Factual accuracy and hallucination | Response A credits the wrong company and person, and misnames a DMAIC phase |
| 3 | [Executive summary constraints](samples/03_instruction_following_summary.md) | Instruction following | Both responses fail at least one constraint, so neither is gold standard |

## Skills shown

* Writing adversarial prompts that expose a specific failure
* Verifying every number and factual claim instead of trusting fluent text
* Scoring consistently against a fixed rubric
* Writing short, evidence based justifications
* Rewriting a flawed response into a reference answer

## License

MIT. Feel free to reuse the rubric and template with credit.
