# Topic 8 — Real Industry Case Studies: How Companies Are Integrating AI into Software Engineering

**Student:** Axel Baci  
**Student ID:** 020525108  
**Course:** SWE101

---

## Introduction

Artificial Intelligence is no longer an experimental concept in software engineering — it is now being embedded into the daily workflows of some of the world's largest and most influential technology companies. This research investigates how four major companies — **Microsoft (GitHub)**, **Google**, **Shopify**, and **Duolingo** — have integrated AI into their software engineering processes, what results they have observed, and what challenges they have encountered along the way.

The goal is not just to document what these companies are doing, but to analyze *why* they are doing it, what it means for developers, and what lessons can be drawn from their experiences.

---

## Case Study 1: Microsoft and GitHub Copilot

### Background

Microsoft is arguably the most influential company in the AI-assisted development space, largely because of its investment in OpenAI and its ownership of GitHub. In 2021, Microsoft launched **GitHub Copilot**, an AI pair programmer that suggests code completions in real time inside code editors.

### Adoption and Scale

GitHub Copilot has grown rapidly. By early 2025, the tool reached over **15 million users** — a roughly 400% increase in just one year. It is integrated into editors like Visual Studio Code, JetBrains IDEs, and others, making it accessible to developers across virtually every major platform.

### What the Research Shows

Microsoft Research conducted a controlled experiment where developers were asked to implement an HTTP server in JavaScript as quickly as possible. The group that had access to GitHub Copilot completed the task **55.8% faster** than the control group without it. This is one of the most cited productivity studies in AI-assisted development.

A larger multi-company study involving Microsoft, Accenture, and a Fortune 100 enterprise — covering nearly 5,000 developers — found an average **26% productivity increase** when using GitHub Copilot. The researchers described it as turning an 8-hour workday into 10 hours of equivalent output. Importantly, this study found no significant drop in code quality, and Copilot users actually showed slightly better build success rates.

Beyond speed, GitHub Copilot is used for:
- Generating boilerplate code
- Writing unit tests and documentation
- Suggesting function implementations from comments
- Onboarding new engineers to unfamiliar codebases

### Limitations and Concerns

The picture is not entirely positive. According to an analysis of major studies from 2024–2025:

- Copilot writes approximately **46% of the average developer's code**, reaching as high as **61% in Java projects**
- **67% of developers use Copilot 5 or more days per week**, raising questions about dependency
- It takes approximately **11 weeks** for developers to realize the full productivity benefits — many abandon the tool before that point
- There are growing concerns about **skill atrophy**, particularly in junior developers who begin using AI before developing fundamental programming skills
- Because many developers receive similar AI-generated suggestions, this can introduce **systemic vulnerabilities** across codebases

Microsoft's own internal engineering blog acknowledges that while Copilot reduces onboarding friction and documentation burden, it requires engineers to actively supervise the output. The tool assists; it does not replace engineering judgment.

---

## Case Study 2: Google

### Background

Google has been integrating AI into its internal developer tooling for several years. Unlike GitHub Copilot, which is a commercial product, Google's tools were first built and deployed internally before being offered publicly.

### Internal AI Tooling

Google's internal software development environment covers both the *inner loop* (IDE, code review, code search) and the *outer loop* (bug management, project planning). AI capabilities have been embedded across both areas. Google engineers have access to ML-based code autocompletion and a natural language-to-code assistant that integrates directly with Google's internal build and test systems.

### Controlled Research Results

In 2024, Google conducted an internal randomized controlled trial (RCT) with approximately **100 of its own software engineers**. The task was a realistic enterprise-level coding assignment: adding a new logging feature across 10 files (~474 lines of code). Developers using AI tools completed the task in roughly **96 minutes**, compared to **114 minutes** for those without AI — about a **21% improvement**.

While this number is smaller than Copilot's 55% figure, the task was significantly more complex and realistic. This makes Google's result arguably more representative of real-world engineering work.

### DORA 2025 Report

Google Cloud publishes the annual **DORA (DevOps Research and Assessment) Report**, which tracks trends across thousands of technology professionals globally. The **2025 DORA Report** surveyed nearly **5,000 professionals** and found:

- AI adoption among software professionals has risen to **90%**, a 14% increase from the prior year
- Professionals now spend a **median of two hours per day** working with AI tools
- The report's central finding: **"AI doesn't fix a team; it amplifies what's already there."** Strong teams get better with AI; struggling teams see their problems intensified
- **Platform engineering** was identified as the foundation: 90% of organizations had adopted at least one internal platform, and there is a direct link between platform quality and the ability to unlock AI's value

### Gemini Code Assist

At Google Cloud Next 2025, Google announced expanded AI agents under the **Gemini Code Assist** and **Gemini Cloud Assist** portfolio. These agents can:
- Generate code from product specifications written in natural language
- Migrate code from one programming language to another
- Automatically create code to address issues filed in GitHub repositories
- Generate and run tests
- Produce documentation

This represents a shift from AI as a code *suggester* to AI as an autonomous development *agent*.

---

## Case Study 3: Shopify

### Background

Shopify, the Canadian e-commerce platform, has become one of the most discussed examples of aggressive AI adoption in an engineering organization. Unlike the research-driven approaches of Microsoft and Google, Shopify's integration story is largely driven by cultural and managerial decisions made at the executive level.

### The Tobi Lütke Memo (April 2025)

In April 2025, Shopify CEO **Tobi Lütke** circulated an internal memo declaring that AI usage was now a **"baseline expectation"** for all employees. The memo became widely discussed across the technology industry after Lütke posted it publicly on X.

Key points from the memo:
- All employees are required to use AI effectively in their daily work
- Before requesting additional headcount or resources, **teams must demonstrate why AI cannot do the work** instead
- AI competency will be evaluated in **performance reviews** and **hiring decisions**
- Shopify product designers are expected to use AI tools for **all platform feature prototypes**

Lütke's framing was direct: he compared the shift to mobile computing in 2013, arguing that waiting to adopt AI would be as costly as being late to mobile. "When there's a shift this big, the worst thing you can do is wait," he wrote.

### Engineering Infrastructure

Shopify's Head of Engineering, **Farhan Thawar**, revealed that the company had been adopting AI tools earlier than most. GitHub Copilot was brought into Shopify before it was even publicly available. By 2025, the company had built:

- An **internal LLM proxy** giving engineers controlled access to multiple AI models
- Over **24 Model Context Protocol (MCP) servers** for AI integration with internal systems
- Company-wide access to Cursor, GitHub Copilot, Claude Code, and other tools — not just for engineers, but for **support, sales, and operations teams** as well

Thawar noted that the fastest-growing users of Cursor inside Shopify were not engineers — they were support and revenue teams. This suggests AI tools are valuable well beyond the coding context.

### Results

Shopify has reported productivity gains of up to **tenfold** when AI tools are properly integrated into the right workflows. Product prototyping became faster and more exploratory. The company was able to do more with smaller teams, reducing reliance on contractors for tasks now handled by AI systems.

### Challenges

The Shopify approach is not without criticism. The memo triggered significant debate in the tech community about whether mandating AI use creates pressure on employees or devalues human expertise. The requirement to justify why a job cannot be automated before hiring signals a fundamental shift in how the company views human labor — pragmatic for productivity, but concerning from a workforce development perspective.

---

## Case Study 4: Duolingo

### Background

Duolingo is the world's largest language learning platform. In April 2025, its CEO **Luis von Ahn** announced an "AI-first" strategy through a company-wide email that was later shared publicly on LinkedIn.

### The AI-First Declaration

Von Ahn's message was unambiguous: Duolingo would restructure how it operates around AI. Key policies announced:
- The company will **gradually stop using contractors** for work that AI can handle
- New headcount will only be approved **if a team cannot automate more of their work**
- AI usage will be evaluated in **hiring and performance reviews**
- The goal is to have employees focus on **creative work and real problems**, not repetitive tasks

Von Ahn framed this as a cultural transformation, not just a tooling change, calling it "a fundamental cultural shift" that requires departments to "reconsider their workflows" entirely. He emphasized that "making minor tweaks to systems designed for humans won't get us there."

### Content Generation at Scale

The most striking result from Duolingo's AI adoption is in content creation. The company announced that in one year with AI, it **built more language courses than in the previous twelve years combined** — creating **148 new courses** and making seven popular languages available across all **28 app languages**.

This is a case where AI did not simply make existing workflows faster — it made previously impossible workflows achievable. At Duolingo's previous rate of content production, those 148 courses would have taken over a decade.

### Engineering Impact

Beyond content, Duolingo's engineering teams use AI to:
- Generate and test language exercises at scale
- Automate quality assurance processes
- Assist with localization across dozens of languages
- Accelerate onboarding of new engineers

The company explicitly supports its employees through the transition by providing training, mentorship, and access to AI tools within each function.

### Challenges

Duolingo's announcement generated backlash, particularly regarding the contractor workforce. Critics pointed out that many of the people replaced by AI systems were freelance translators, language experts, and content creators. The company maintained that AI frees human employees for higher-value work, but the impact on the contracted talent pool is real and significant.

---

## Cross-Company Analysis

### Common Themes

Across all four companies, several patterns emerge:

1. **AI is becoming a baseline, not a bonus.** What was once an optional productivity tool is now an expected competency. Shopify and Duolingo have made this explicit through policy; Google and Microsoft have embedded it structurally.

2. **Productivity gains are real but uneven.** Studies show 21–55% speed improvements in controlled settings, but real-world gains depend on the complexity of the task, the experience of the developer, and the quality of the surrounding infrastructure.

3. **Junior developers are most affected.** Multiple studies and industry observations highlight that newer developers either benefit most from AI assistance — or risk never developing core skills by relying on it too early.

4. **Quality of human oversight matters.** Google's DORA report made it explicit: AI amplifies existing team culture and practices. A team with poor engineering discipline using AI will produce poor results faster. The human layer of judgment, review, and architecture remains critical.

5. **The role of software engineers is changing.** Engineers are increasingly becoming supervisors, architects, and reviewers of AI-generated work rather than purely writers of code. This is a significant shift in professional identity and required skill set.

### Differences in Approach

| Company | Approach | Scope | Mandate Level |
|---------|----------|-------|---------------|
| Microsoft / GitHub | Research + commercial product | Global, 15M+ users | Optional (product) |
| Google | Internal R&D + external tools | Entire engineering org | Embedded in tooling |
| Shopify | Executive mandate + infrastructure | All employees | Required |
| Duolingo | CEO directive + contractor reduction | Entire company | Required |

---

## Conclusion

The companies examined in this research represent a spectrum of AI integration strategies — from research-driven and measured (Microsoft, Google) to culturally mandated and aggressive (Shopify, Duolingo). What is consistent across all four is that AI is no longer peripheral to software engineering. It is becoming infrastructure.

The key insight for software engineers entering the industry is this: AI tools will not replace thoughtful engineers — but engineers who know how to use AI effectively will have a significant advantage over those who do not. At the same time, the cases of Shopify and Duolingo raise important questions about what happens to the workforce when productivity is measured primarily by what AI cannot yet do.

The transition is already underway. Understanding it through real examples, as this research attempts to do, is essential for any software professional who wants to navigate the next decade with clarity.

---

*Word count: ~1,800 words*  
*References are listed in references.md*
