# AI-Native Biotechs & AI Agents in Life Sciences — Research Profile

## Overview

A new class of biotech company is emerging that places LLMs, generative AI, and AI agents at the center of drug development — not as add-on tools, but as the operational backbone. Unlike earlier "AI-enabled" approaches that used machine learning for isolated tasks like target identification or compound screening, these companies deploy AI agents that autonomously coordinate across the entire clinical development lifecycle. The shift matters most in Phase 2 and Phase 3 trials, where operational complexity (site selection, patient recruitment, protocol design, data management) has become the primary bottleneck.

## The Distinction: AI Agents vs. Traditional ML in Biotech

> "AI agents extend beyond traditional ML and LLMs by enabling autonomous, goal-directed actions across the clinical trial lifecycle. These systems have the potential to coordinate activities leveraging trial protocols and patient data, invoking tools dynamically, and interacting with multiple components of a CT pipeline — mimicking roles such as coordinators or analysts."

**Traditional ML in biotech:** Static models trained for a single task (e.g., predicting binding affinity, classifying compounds). Human operators run the model, interpret output, and decide next steps.

**LLM/GenAI agents in biotech:** Autonomous or semi-autonomous systems that reason, plan, and act in complex clinical environments with minimal human intervention. They adapt to new information, learn from trial progress, and proactively orchestrate tasks.

**Source:** [Nature npj Digital Medicine — AI and Innovation in Clinical Trials (2025)](https://www.nature.com/articles/s41746-025-02048-5)

## AI Agents in Phase 2/3 Clinical Trials: The Critical Frontier

### Why Phase 2/3 Matters Most

The Tufts Center for the Study of Drug Development attributes increasing trial complexity to an upward trend impacting all protocol design variables, especially in Phase II and Phase III trials. A 2025 Tufts study found that **Phase III trials each average nearly 6 million data points**, and the number of data points per trial has roughly **tripled over the past decade**. This explosion of complexity is precisely where AI agents deliver the most value.

**Source:** [BioXconomy — How AI Agents Are Transforming the Clinical Trial Process for CRAs](https://www.bioxconomy.com/clinical-and-research/how-ai-agents-are-transforming-the-clinical-trial-process-for-cras)

### Protocol Design & Authoring

**Narrativa** deploys multiple specialized AI agents that work in parallel on clinical trial protocols:

- **Protocol Design Agent:** Creates structured clinical trial protocols aligned with ICH M11 guidelines, defining study structure, methodology, objectives, and endpoints. Generates fully structured drafts in hours rather than weeks.
- **Protocol Burden Agent:** Evaluates visit schedules, assessment frequency, and procedural complexity to optimize protocols for patient and site feasibility — improving retention rates and accelerating enrollment.
- **Protocol Study Population Agent:** Evaluates proposed patient populations for diversity and representativeness.
- **Protocol Auditor Agent:** Ensures alignment with ICH M11 templates and sponsor-specific guidelines automatically.

**Source:** [Narrativa — Protocol Clinical Trials Automation with AI Agents](https://www.narrativa.com/protocol-clinical-trials-automation-with-ai-agents)

### LLMs for Protocol Authoring

A 2024 research project ("Intelligent Clinical Trial Design Support using Generative AI") demonstrated that GPT-4 can generate clinical trial protocol sections that integrate successfully into existing trial design toolkits:

> "The strategic use of generative AI models like GPT-4 not only streamlined the protocol development process but also opened new avenues for innovation in clinical trial design."

**Source:** [arXiv — Clinical Trials Protocol Authoring using LLMs (2024)](https://arxiv.org/html/2404.05044v2)

### Multi-Agent Systems for Clinical Development

**Medable Agent Studio** provides a platform for deploying agentic AI across clinical trials:

- **Connect:** Integrates clinical systems for real-time data flow and faster decisions
- **Assist:** Pre-configured agents automate filing, proactively identify site risks, generate pre-visit summaries, or can be custom-built for trial-specific needs
- **Verify:** Built-in verification and quality assurance designed for clinical development
- **Evolve:** Platform evolves continuously, going beyond static systems

**Source:** [Medable — Agentic AI for Clinical Trials](https://www.medable.com/platform/agent-studio)

### Patient Recruitment & Trial Matching

Recent research demonstrates significant gains from multi-agent LLM systems:

- **ClinicalAgent** (multi-agent LLM system): Improved trial outcome prediction by **0.33 AUC** over baseline prompting methods by integrating real-world data and protocol reasoning
- **MAKAR:** Achieved **100% accuracy** in controlled patient-trial matching tasks by using role-specific agents to navigate complex eligibility criteria
- **Oncology-focused GPT-4 agents** with multimodal tool access: Reached **87% accuracy** in diagnostic and enrollment decisions — nearly tripling the performance of standalone LLMs (30%)

**Source:** [Nature npj Digital Medicine (2025)](https://www.nature.com/articles/s41746-025-02048-5)

### Human-AI Collaboration in Recruitment

A 2026 JMIR AI study developed a sociotechnical and economic framework for LLM-powered clinical trial recruitment, identifying three critical gaps:

1. Most recruitment studies remain focused on component-level matching performance rather than how LLM outputs are embedded into real organizational workflows
2. The technical literature on patient-trial matching remains weakly connected to the literature on human-AI collaboration
3. The organizational and economic consequences of LLM adoption (privacy controls, validation costs, oversight burdens) remain underexplored

The central design question is not whether humans should remain involved but **how oversight intensity, override authority, explanation timing, and escalation logic should be configured** so that technical capability improves rather than destabilizes workflow performance.

**Source:** [JMIR AI — LLMs in Clinical Trial Recruitment (2026)](https://ai.jmir.org/2026/1/e95899)

## AI-Native Biotech Companies Using Agents and GenAI

| Company | Founded | AI Approach | Key Achievement |
|---|---|---|---|
| **Insilico Medicine** | 2014 | End-to-end AI drug discovery (PandaOmics + Chemistry42 + InClinico) | First fully AI-discovered and AI-designed drug (INS018_055 for IPF) into Phase 2 trials in under 30 months; each module feeds the next and compounds knowledge |
| **Recursion Pharmaceuticals** (NASDAQ: RXRX) | 2013 | Phenomics + AI drug discovery platform | Acquired Exscientia for $688M; partnerships with Bayer, Roche, Sanofi; >50 petabytes of proprietary biological data |
| **Xaira Therapeutics** | 2024 | ML + data generation + therapeutics | $1B initial funding — largest biotech launch commitment; co-founded by Nobel laureate David Baker |
| **Isomorphic Labs** (Alphabet/DeepMind) | 2021 | Protein structure prediction → drug design | $600M raised; partnerships with Eli Lilly and Novartis; built on AlphaFold |
| **Genesis Therapeutics** | 2019 | Molecular AI (Pearl foundation model) | Outperforms AlphaFold 3 by up to 40%; partnerships with Eli Lilly, Genentech, Incyte |

**Source:** [ITONICS — 7 Lessons from AI-Native Pharma Startups](https://www.itonics-innovation.com/blog/ai-native-pharma-startups)

## Stanford "Virtual Biotech Company" (2025)

Stanford researchers (James Zou and colleagues) built a multi-agent AI platform where specialized models act like different scientific teams — genetics, pharmacology, clinical development — coordinated by a virtual "Chief Scientific Officer."

**Key demonstrations:**
- Analyzed 55,000+ clinical trials using thousands of AI agents
- Found drug targets with cell-type-specific gene expression are significantly more likely to succeed
- In a lung cancer case study, agents recommended ADCs targeting B7-H3
- Analyzed a failed ulcerative colitis trial and suggested biomarker-guided patient selection

**Source:** [LinkedIn post by Garri Zmudze (LongeVC)](https://www.linkedin.com/posts/garri-zmudze-982a48138_stanford-researchers-just-built-an-ai-agent-activity-7435705415365197825-_kBz)

## Three Archetypes of AI-Native Pharma

1. **Platform-first companies** (Recursion, Insilico): Built end-to-end AI systems before selecting drug targets. High upfront investment, but the platform generates multiple programs.

2. **Modality specialists** (Generate Biomedicines): Focus on specific therapeutic approaches with deep AI application in one domain.

3. **Hybrid adopters** (Relay Therapeutics): Combine AI-native capabilities in specific domains with more traditional approaches elsewhere.

**Source:** [ITONICS](https://www.itonics-innovation.com/blog/ai-native-pharma-startups)

## Key Lessons from AI-Native Pharma Startups

1. **Build proprietary data infrastructure from day one** — Recursion generates 8 billion cellular images before finding targets; proprietary data creates an unreplicable competitive moat.

2. **Platform thinking beats single-asset bets** — AI-native platforms compound knowledge across programs; each subsequent program is faster and cheaper.

3. **Design-make-test-analyze closed loops** — AI-native companies weave computational and experimental work into continuous feedback cycles.

4. **AI-native economics** — 80-90% Phase I success rates vs. 40-65% traditional; development timelines compress from 10+ years to 3-6 years.

5. **Data as infrastructure, algorithms as decision-makers, platforms as products.**

**Source:** [ITONICS](https://www.itonics-innovation.com/blog/ai-native-pharma-startups)

## Academic References

1. **AI and innovation in clinical trials** — *Nature npj Digital Medicine* (2025)
   DOI: [10.1038/s41746-025-02048-5](https://www.nature.com/articles/s41746-025-02048-5)

2. **Clinical Trials Protocol Authoring using LLMs** — arXiv (2024)
   Available at: [arxiv.org/html/2404.05044v2](https://arxiv.org/html/2404.05044v2)

3. **LLMs in Clinical Trial Recruitment: Sociotechnical and Economic Framework** — *JMIR AI* (2026)
   DOI: [10.2196/95899](https://ai.jmir.org/2026/1/e95899)

## Additional Sources

- [Narrativa — Protocol Clinical Trials Automation](https://www.narrativa.com/protocol-clinical-trials-automation-with-ai-agents)
- [Medable — Agentic AI for Clinical Trials](https://www.medable.com/platform/agent-studio)
- [BioXconomy — AI Agents Transforming Clinical Trial Process](https://www.bioxconomy.com/clinical-and-research/how-ai-agents-are-transforming-the-clinical-trial-process-for-cras)
- [Recursion Pharmaceuticals](https://www.recursion.com/)
- [Insilico Medicine](https://insilico.com/)

---

*Research compiled: May 2026*
