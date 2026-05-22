# Company Brain / Second Brain — Research Profile

## Overview

"Company Brain" is one of the 15 categories in Y Combinator's Summer 2026 Request for Startups (RFS). It represents YC's explicit bet that the next major startup category is a system that pulls fragmented organizational knowledge into a structured, AI-usable format — enabling reliable AI automation across every business function.

## Y Combinator's Request for Startups (S26)

### YC's Exact Language on "Company Brain"

> "The biggest blocker to AI automation of companies is no longer the models — they just got so good so quickly. Now the blocker is the domain knowledge. Every company has critical know-how scattered everywhere. Some of it lives in people's heads. Some of it is buried in old email accounts, Slack threads, support tickets, and databases. The company works because humans vaguely remember where that knowledge is and how to apply it. But AI agents can't operate like that. If we want every company to run on AI automation, we need a new primitive: a company brain. We need Garry's G-Brain, but for every business in the world. A system that pulls knowledge out of all these fragmented sources, structures it, keeps it current, and turns it into an executable skills file for AI. This isn't a company-wide search or a chatbot over documents. It's a living map of how a company works: how refunds get handled, how pricing exceptions are decided, or how engineers respond to incidents. Then AI systems can use that skills file to actually do the work safely and consistently. The company brain becomes the missing layer between raw company data and reliable AI automation. I think every company in the world is going to need one."

**Source:** [Y Combinator RFS — ycombinator.com/rfs](https://www.ycombinator.com/rfs)

### Related RFS Categories

The Company Brain concept intersects with two other YC S26 categories:

- **"The AI Operating System for Companies"** — Make everything a company produces queryable by an AI layer. Meetings, tickets, customer calls, all of it. The goal is a closed loop where the system flags problems and adjusts rather than waiting for someone to notice weeks later.
- **"Software for Agents"** — AI agents are doing real work but through interfaces built for humans. They need APIs, MCPs, CLIs. Every software category needs a version built with agents in mind first.

### Full S26 RFS List

1. AI for Low-Pesticide Agriculture
2. AI-Native Service Companies
3. AI Personalized Medicine
4. **Company Brain**
5. Counter-Swarm Defense
6. Dynamic Software Interfaces
7. Electronics in Space
8. Hardware Supply Chain
9. Industrial Capabilities in Space
10. Inference Chips for Agent Workflows
11. SaaS Challengers
12. Software for Agents
13. Startups That Want to Sell to Huge Companies
14. Supply Chain 2.0 for Semiconductors
15. **The AI Operating System for Companies**

**Source:** [Reddit — YC RFS Discussion](https://www.reddit.com/r/startups/comments/1tcxdoz/y_combinator_just_released_their_requests_for)

## How the Market Is Interpreting "Company Brain"

### Christophe Pasquier (Slite / Super.work, YC W16)

> "Companies need something that takes cross-tool context from Slack, Linear etc. → synthesises automatically into SOPs and guides → served as skill files and context for agents."

Slite (knowledge base) + Super.work (retrieval engine) are building this. Super connects context to create true knowledge; Slite is where it lives and updates automatically.

**Source:** [LinkedIn Post by Christophe Pasquier](https://www.linkedin.com/posts/christophepasquier_yc-just-put-company-brain-on-their-2026-activity-7455211223639523328-4qJ5)

### Wissem Golli (Sagy AI)

> "A system that pulls knowledge from Slack, Jira, GitHub, docs, meetings, structures it, keeps it current, and turns it into something AI agents can actually reason over. Not a wiki. Not a chatbot. A living company memory."

**Source:** [LinkedIn Post by Wissem Golli](https://www.linkedin.com/posts/wissemgolli_ai-ycombinator-aiagents-activity-7455326829202214912-hRRG)

### Key Interpretations

1. **Not a search tool or a chatbot over documents** — It must produce *executable* knowledge, not just retrievable text.
2. **The "Skills File" concept** — Knowledge must be structured as actionable skills that AI agents can execute, not just reference.
3. **Cross-tool context aggregation** — Must pull from Slack, Linear, Jira, GitHub, email, docs, meetings, tickets.
4. **Living and self-healing** — Must stay current as the company changes; not a static wiki.
5. **Agent-first design** — The output must be consumable by AI agents, not just humans.

## Companies Building in This Space

| Company | Approach | Notes |
|---|---|---|
| **Slite + Super.work** | Knowledge base + retrieval engine | YC W16; 2+ years building |
| **Sagy AI** | AI agent knowledge memory | Start It Accelerate |
| **Aligno** | Feedback + roadmap + codebase → unified system | Targets product teams |
| **Garry's GBrain** (referenced by YC) | Internal knowledge system | The archetype YC references |
## The "LLM Wiki" Paradigm — Technical Realization of the Second Brain (Andrej Karpathy)

Andrej Karpathy has formulated a concrete design pattern for implementing personal and organizational "Second Brains" using LLM agents, which he terms the **LLM Wiki**. This pattern moves beyond traditional Retrieval-Augmented Generation (RAG) toward a persistent, compounding knowledge codebase.

### The Core Paradigm: Compounding Artifacts vs. Ephemeral RAG

Most traditional RAG-based systems retrieve raw chunks of document data dynamically at query time (as seen in standard NotebookLM or ChatGPT document uploads). This approach forces the LLM to re-evaluate, synthesize, and resolve contradictions from scratch on every single prompt, leading to repetitive computation and no accumulation of structured knowledge.

Conversely, the **LLM Wiki** is a persistent, compounding artifact. The LLM agent acts as the programmer, and the knowledge base behaves as the codebase. When a new source is introduced, the LLM compiles and integrates it once, resolving contradictions and updating relevant concept pages, ensuring the knowledge is always structured and pre-compiled for future queries.

### Three-Layer Architecture

An LLM Wiki implementation consists of three distinct conceptual layers:

1. **Raw Sources (Immutable)**: The curated raw repository of truth (articles, scientific papers, meeting transcripts, PDFs). The LLM reads from these but never alters them.
2. **The Wiki (Persistent Markdown)**: A structured directory of LLM-generated and maintained markdown files (summaries, concept maps, entity profiles, comparisons). The LLM entirely owns the write and edit operations of this directory.
3. **The Schema (Rules & Metacognition)**: A configuration file (such as `AGENTS.md` or `CLAUDE.md` / `pyproject.toml`) defining conventions, directory layouts, and ingestion/maintenance workflows. This serves as the "programming instructions" that turn the LLM into a disciplined wiki maintainer rather than a generic chatbot.

### Core Operations and Workflows

* **Ingest**: Dropping a new source triggers the LLM to read the source, discuss key takeaways with the operator, generate a dedicated summary page, update the main index, and update 10–15 related concept or entity pages across the wiki to maintain cross-tool cohesion.
* **Query**: Rather than relying on fragile real-time embeddings, the LLM reads a highly structured index catalog to pinpoint highly relevant pages and synthesize answers with exact citations. Complex syntheses can be permanently written back to the wiki as new pages.
* **Lint**: Periodically, the LLM runs a health check across the wiki to detect factual contradictions between older and newer sources, surface stale claims, locate orphan pages, identify data gaps to fill via web searches, and build missing cross-references.

### Structured Navigation: Indexing and Logging

The system relies on two critical system files to facilitate scale and navigation:

* **index.md (Content Directory)**: A comprehensive, categorized catalog of all wiki pages containing links and one-line summaries. This structured file enables the LLM to map out the entire knowledge corpus without needing complex vector database infrastructure at moderate scales (~100s of pages).
* **log.md (Chronological Log)**: An append-only, chronologically sorted journal of all operations (e.g., `## [2026-05-21] ingest | Source Title`). This chronological list enables standard terminal tools (like `grep` or `tail`) to quickly track history and current state.

### Recommended Tooling and Implementation Tips

* **Obsidian Web Clipper**: A browser extension to capture clean markdown representations of web articles.
* **Local Asset Syncing**: Downloading and storing image attachments locally in fixed directories (e.g., `raw/assets/`), allowing multi-modal LLMs to reference spatial and diagrammatic contexts.
* **Obsidian Graph View**: Visualizes structural links, highlighting hubs, concept clusters, and orphan nodes.
* **Marp Slide Decks & Dataview**: Marp translates markdown directly into executive slide presentations. Dataview parses YAML frontmatter to generate dynamic, automated tables of content and metrics.
* **Git Version Control**: Utilizing git for the entire wiki repository provides branching, rollback capabilities, change history, and multi-user collaboration for free.
* **Hybrid Local Search**: Employing local tools like `qmd` (hybrid BM25/vector search engine with LLM re-ranking) or MCP servers to enable native, programmatic search directly within the LLM's workspace.

### The Operational Rationale

> Maintaining a corporate or personal knowledge base fails not because of the reading or thinking, but due to the high manual cost of bookkeeping (updating links, reconciling details, maintaining indexes). By delegating the grunt work of maintenance to LLM agents—which do not experience fatigue or forget details—the cost of keeping organizational knowledge current drops to near zero.
>
> This idea is related in spirit to Vannevar Bush's Memex (1945)—a personal, curated knowledge store with associative trails between documents. Bush's vision was closer to this than to what the web became: private, actively curated, with the connections between documents as valuable as the documents themselves. The LLM handles the one part Bush could not solve: the manual burden of ongoing maintenance.

**Source:** [Andrej Karpathy — LLM Wiki Gist](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f)

## Strategic Significance

1. **YC's signal is strong** — When YC publicly names a category, it directs founder attention, investor capital, and talent flows. Previous RFS categories have preceded major market movements.
2. **Enterprise AI is the center of gravity** — Three of the fifteen S26 categories are some flavor of "run the company on AI."
3. **SaaS disruption** — YC's "SaaS Challengers" and "AI-Native Service Companies" on the same list signals that the next version of SaaS doesn't look like the last.
4. **The "missing layer" thesis** — Company Brain is positioned as the infrastructure between raw company data and reliable AI automation. Without it, AI agents cannot operate consistently.
5. **Implications for biotech/life sciences** — A "company brain" for a biotech would need to integrate clinical trial data, regulatory documents, competitive intelligence, scientific literature, and institutional knowledge — a significantly more complex knowledge domain than typical SaaS companies.

*Research compiled: May 2026*
*Sources: Y Combinator RFS (ycombinator.com/rfs), LinkedIn posts, Reddit discussions, Andrej Karpathy's LLM Wiki Gist (gist.github.com/karpathy/442a6bf555914893e9891c11519de94f)*

