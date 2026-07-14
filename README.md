# Meeting Intelligence Orchestrator

**An AI-powered Business Analyst that transforms raw meeting transcripts into structured, evidence-traceable business artifacts.**

Instead of immediately generating user stories or meeting notes, the orchestrator first determines **what kind of meeting actually took place**, then produces the appropriate business artifact.

🌐 **Live Demo**

https://sahiyapnajeeb.github.io/meeting-orchestrator/

No installation required.

- **See Example Output** → Instant demo (no API key required)
- **Analyze Your Own Transcript** → Bring your own Claude API key and analyze any meeting transcript

---

# Screenshot

![Meeting Intelligence Orchestrator — classified output with requirement package](images/screenshot.png)

*Requirement package detail:*

![Requirement package detail view](images/screenshot-detail.png)

---

# Overview

Meetings generate decisions, requirements, risks, action items, and open questions—but turning a raw transcript into useful documentation is still largely a manual task for Business Analysts.

This project explores how AI can automate that work.

Rather than jumping straight into writing user stories or meeting minutes, the orchestrator first asks:

> **"What kind of meeting was this?"**

Only after classifying the meeting does it generate the appropriate business artifact.

The result behaves more like a Business Analyst than a chatbot.

---

# Project Origin

This project began as an idea for a **Microsoft 365 Copilot + Power Automate** solution.

The original vision was simple:

```
Teams Meeting Ends
        │
        ▼
Transcript Generated
        │
        ▼
Power Automate Trigger
        │
        ▼
Meeting Intelligence Orchestrator
        │
        ▼
Classify Meeting Type
        │
        ▼
Generate Appropriate Business Artifact
        │
        ▼
SharePoint / Teams / Outlook
```

Before integrating with Microsoft 365, I wanted to validate the AI reasoning independently.

This standalone web application focuses entirely on the intelligence layer:

- understanding the meeting
- selecting the appropriate workflow
- generating structured business artifacts

while remaining deployable as a simple static website.

---

# What It Does

The orchestrator automatically classifies a meeting into one of several categories:

- Requirement Elicitation
- Status Update
- Sprint Planning
- Design Discussion
- Bug / Issue Review
- Decision Meeting
- General Discussion

Each classification includes:

- Confidence level
- Classification reasoning
- Supporting evidence from the transcript

---

## Requirement Elicitation Workflow

When the transcript represents a requirement gathering session, the AI generates a structured Requirement Package including:

- Requirement ID
- Requirement Type
- Business Goal
- Priority
- Dependencies
- Risks / Gaps
- Open Questions
- Evidence Quotes
- Requirement Quality Score

Every requirement links back to the original transcript so nothing is invented.

---

## Other Meeting Types

For all other meeting types, the orchestrator produces:

- Meeting Minutes
- Discussion Summary
- Decisions Made
- Action Items
- Owners
- Due Dates
- Risks / Blockers
- Next Steps

---

# How It Works

```
Meeting Transcript
        │
        ▼
Meeting Classification
        │
        ▼
Confidence & Reasoning
        │
        ▼
Workflow Selection
        │
        ├───────────────┐
        │               │
        ▼               ▼
Requirement       Meeting Minutes
Package           Decision Log
                  Action Items
                  Status Summary
        │
        ▼
Structured Business Artifact
```

---

# Technologies

| Technology | Purpose |
|------------|---------|
| Claude Sonnet (Anthropic API) | Meeting reasoning and artifact generation |
| HTML / CSS / Vanilla JavaScript | User interface and application logic |
| JSON Schema | Ensures structured, renderable AI output |
| GitHub Pages | Free static hosting |
| GitHub | Source control and project hosting |

---

# Product Decisions

This project intentionally makes several design decisions that prioritize usability and transparency.

### Structured JSON instead of free-form AI responses

Rather than producing long paragraphs of text, the AI returns structured JSON.

This makes the output:

- consistent
- renderable
- easier to validate
- easier to integrate into future workflows

---

### Classify before generating

Most AI meeting assistants immediately begin producing user stories or meeting summaries.

This project first determines:

> **What business artifact should exist?**

That mirrors how an experienced Business Analyst approaches a meeting.

---

### Evidence Traceability

Every requirement, conclusion, and recommendation includes evidence from the transcript.

Nothing should appear without being supported by something that was actually said.

---

### Cached Demo Mode

A complete example output is bundled with the application.

Visitors can evaluate the project instantly without:

- creating an account
- obtaining an API key
- spending API credits

---

### Bring Your Own API Key

Live analysis happens entirely in the browser.

Your Claude API key:

- never leaves your browser except when sent directly to Anthropic
- is never stored
- is never sent to any third-party server

This keeps the project free to host while still allowing anyone to test it on their own meeting transcript.

A production version would move this behind a secure backend with authentication, rate limiting, and key management.

---

# Future Roadmap

This prototype validates the AI reasoning layer.

Potential future enhancements include:

- Microsoft Teams integration
- Power Automate workflow
- Automatic transcript ingestion
- SharePoint document generation
- Outlook summary emails
- Planner task creation
- Multi-agent BA workflow
- Jira integration
- Azure DevOps integration
- Secure server-side API architecture
- Organization-wide deployment

---

# Why This Project

Business Analysts spend significant time reviewing meeting transcripts to determine:

- What was actually decided?
- Which statements are real requirements?
- What still needs clarification?
- What documentation should be produced?

This project explores how AI can perform that reasoning step while keeping every generated artifact traceable back to the original conversation.

The goal is not to replace Business Analysts.

The goal is to reduce repetitive documentation work so they can spend more time on analysis, stakeholder collaboration, and product thinking.

---

# Author

**Sahiyap Najeeb**

Business Analyst • AI Workflow Builder • Product Thinking

GitHub

https://github.com/Sahiyapnajeeb

LinkedIn

https://www.linkedin.com/in/sahiya-p-najeeb/

Portfolio

(Add your portfolio URL)

---

⭐ If you found this project interesting, feel free to star the repository or connect with me on LinkedIn.
