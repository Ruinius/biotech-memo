# Synthetic Panel of Experts Using GenAI — Research Profile

## Overview

Synthetic panels use generative AI to create virtual respondents or expert personas that can participate in surveys, interviews, and other research studies. These AI-generated "panelists" simulate opinions and behaviors based on real-world data, offering a faster, cheaper, and more scalable alternative to traditional human panels. Applications range from consumer feedback and market research to simulating Key Opinion Leader (KOL) panels in pharmaceuticals.

## What Are Synthetic Panels?

> "Synthetic panels are built using generative AI models — often trained on consumer data — and consist of synthetic respondents that can participate in surveys, interviews, and other synthetic research studies."

Synthetic panels create multiple "synthetic respondents" — virtual participants that act as stand-ins for original human respondents. The training data can be public or private, including user demographics, buying behavior, purchase preferences, and more.

**Source:** [Delve AI — Using Synthetic Panels To Find Quality Customer Insights](https://www.delve.ai/blog/synthetic-panels)

## Three Types of Synthetic Research Models

1. **LLM wrappers** built around larger LLMs like ChatGPT — Lack distinctiveness because responses derive from publicly available information.

2. **Machine learning-powered models** — Learn from past research to generate unique responses; output depends entirely on input data quality.

3. **Foundational large language models** — Leverage both internal and external data sources, filling gaps for more nuanced and contextually informed output. Most effective for highly specific market segments.

**Source:** [Delve AI](https://www.delve.ai/blog/synthetic-panels), citing Qualtrics

## Commercial Platforms

| Platform | Approach | Key Feature |
|---|---|---|
| **Delve AI** | Combines customer data + 40+ public data sources to create AI personas; then generates synthetic panels from persona segments | $0.99 per synthetic user; supports quantitative and qualitative studies |
| **NIQ (NielsenIQ)** | Synthesizes respondents using proprietary consumer-panelist data + in-market transactional data | Calibrated against real sales data; category-specific accuracy |
| **Reply** | Generative AI synthetic consumer data based on real data samples | Consumer behavior simulation for marketing |

**Sources:**
- [Delve AI](https://www.delve.ai/blog/synthetic-panels)
- [NIQ — The Rise of Synthetic Respondents](https://nielseniq.com/global/en/insights/education/2024/the-rise-of-synthetic-respondents)
- [Reply — Simulation of Consumer Behavior](https://www.reply.com/en/artificial-intelligence/simulation-of-consumer-behavior-with-generative-ai)

## Cost Comparison

| Method | Cost Per Participant |
|---|---|
| **Synthetic panels (Delve AI)** | ~$0.99–$2.00 per user |
| **Online surveys (human)** | $50–$150 per person |
| **In-depth interviews (human)** | $400–$600 per person |
| **Focus groups (human)** | $15,000–$30,000 per session |

**Source:** [Delve AI](https://www.delve.ai/blog/synthetic-panels), citing Blackridge Research

## Synthetic KOL (Key Opinion Leader) Panels

### Concept

In pharmaceutical and biotech contexts, a synthetic KOL panel would use GenAI to simulate the opinions, clinical perspectives, and prescribing behaviors of key opinion leaders in a specific therapeutic area. This could be used to:

- Pre-test messaging and clinical positioning before engaging real KOLs
- Simulate how different clinical profiles might be received by the medical community
- Rapidly gather "directional" insights on competitive clinical strategies
- Stress-test regulatory or commercial hypotheses against a panel of simulated experts

### Challenges Specific to KOL Simulation

1. **Expert knowledge depth** — KOL opinions are shaped by decades of clinical experience, unpublished observations, and institutional context that may not be captured in training data.
2. **Novelty suppression** — LLMs are architecturally disposed to predict the most probable next token, which suppresses the very novel insights that KOLs provide.
3. **Missing 23% problem** — One study found that an LLM hybrid recovered 77% of themes identified by human analysts. The missing 23% may contain the only themes that mattered.
4. **Confirmation at scale** — Synthetic respondents can produce "plausible data — data that looks rich, reads well, and leads to the comforting conclusion that the researcher's hypotheses were correct all along."

**Source:** [MIT Sloan Management Review — Gain Consumer Insight with Generative AI](https://sloanreview.mit.edu/article/gain-consumer-insight-with-generative-ai/) (commentary/critique)

## NIQ's Three Principles for Best-in-Class Synthetic Models

1. **Test, calibrate, and validate response accuracy across every category** — Controlling for model biases requires continual adjustment of methodology, instructions, and prompting order.

2. **Leverage the latest granular data to drive accuracy** — Prompting models with the latest in-market behavioral data rather than training on historical preferences.

3. **Place data in context to navigate next steps** — Synthetic feedback should be placed in comparative context against other ideas and real-world data.

**Source:** [NIQ — The Rise of Synthetic Respondents](https://nielseniq.com/global/en/insights/education/2024/the-rise-of-synthetic-respondents)

## Critical Limitations & Risks

### The "Researcher Becomes the Demiurge" Problem

> "The researcher who constructs both the synthetic respondent and the AI moderator is, in effect, conducting a conversation with a sophisticated echo of their own assumptions. The 'human oversight' the authors advocate for is necessary but insufficient if the human doing the overseeing is also the one who built the simulation."

**Recommended safeguard:** Adversarial separation — the person who designs synthetic respondents should not be the same person who evaluates the output.

**Source:** MIT Sloan Management Review commentary

### Key Risks

1. **Lack of extreme opinions** — Synthetic panels tend toward middle-ground answers and lack the variation found in human responses.
2. **Reproduction of known patterns** — They tend to reproduce what is already known rather than generating original insights.
3. **Scale destroys quality** — At 100+ interviews, a researcher can no longer review every transcript; at 1,000, the researcher is operating a factory.
4. **Epistemic concentration** — The researcher creates the respondents, scripts their personalities, and programs the interviewer's judgment — an extraordinary concentration of epistemic power.

## Academic Reference

> "Generative AI framework for sensory and consumer research"
> — *Social Science & Medicine* (2025)
> DOI: [10.1016/j.socscimed.2025.117552](https://www.sciencedirect.com/science/article/pii/S0950329325001752)
> First paper to propose a comprehensive framework for integrating GenAI into R&D in sensory and consumer science.

## Implications for Biotech/Life Sciences

1. **Synthetic KOL panels** could dramatically reduce the cost and time of pre-launch clinical positioning research.
2. **Synthetic patient/consumer feedback** could accelerate early-stage product concept testing before committing to expensive human studies.
3. **The confirmation bias risk is amplified in biotech** — where the cost of a wrong strategic decision (e.g., pursuing the wrong indication) is measured in hundreds of millions of dollars.
4. **Adversarial separation is critical** — The person designing synthetic KOLs should not be the same person making go/no-go decisions based on their output.
5. **Synthetic panels are a supplement, not a replacement** — Best used for early-stage directional insights, with human validation for consequential decisions.

---

*Research compiled: May 2026*
