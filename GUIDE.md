# Master Guide: Gemini Nano Bana Prompt Engineering

```
╔══════════════════════════════════════════════════════════════════════╗
║                                                                      ║
║     MASTER PROMPT ENGINEERING GUIDE                                  ║
║     For Gemini Nano Bana                                             ║
║                                                                      ║
║     15 Prompt Concepts | 45+ Prompt Types | 90+ Examples            ║
║                                                                      ║
╚══════════════════════════════════════════════════════════════════════╝
```

---

## Table of Contents

1. [How to Use This Guide](#how-to-use-this-guide)
2. [Prompt Concept Overview](#prompt-concept-overview)
3. [Concept 1: Foundational Prompts](#concept-1-foundational-prompts)
4. [Concept 2: Chain-of-Thought Prompts](#concept-2-chain-of-thought-prompts)
5. [Concept 3: Few-Shot Prompts](#concept-3-few-shot-prompts)
6. [Concept 4: Role-Based Prompts](#concept-4-role-based-prompts)
7. [Concept 5: Visual & Diagram Prompts](#concept-5-visual--diagram-prompts)
8. [Concept 6: Tutorial Generation Prompts](#concept-6-tutorial-generation-prompts)
9. [Concept 7: PDF Analysis Prompts](#concept-7-pdf-analysis-prompts)
10. [Concept 8: Dynamic Interactive Prompts](#concept-8-dynamic-interactive-prompts)
11. [Concept 9: Comparative Analysis Prompts](#concept-9-comparative-analysis-prompts)
12. [Concept 10: Storytelling & Narrative Prompts](#concept-10-storytelling--narrative-prompts)
13. [Concept 11: Code Generation & Debug Prompts](#concept-11-code-generation--debug-prompts)
14. [Concept 12: Assessment & Quiz Prompts](#concept-12-assessment--quiz-prompts)
15. [Concept 13: Data Visualization Prompts](#concept-13-data-visualization-prompts)
16. [Concept 14: Summarization Prompts](#concept-14-summarization-prompts)
17. [Concept 15: Creative & Brainstorming Prompts](#concept-15-creative--brainstorming-prompts)
18. [Choosing the Right Prompt Type](#choosing-the-right-prompt-type)
19. [Tips & Best Practices](#tips--best-practices)

---

## How to Use This Guide

```
NAVIGATION:
┌──────────────────────────────────────────────────────────────┐
│                                                               │
│  1. READ THIS GUIDE for an overview of all 15 concepts       │
│                                                               │
│  2. BROWSE CONCEPT FOLDERS for detailed examples             │
│     Each folder: README + 2-3 prompt type files              │
│                                                               │
│  3. COPY & ADAPT prompts for your specific use case          │
│     Replace [placeholders] with your actual content          │
│                                                               │
│  4. CHECK WHERE_TO_USE_NANO_BANA.md for integration guides   │
│     Learn how to use prompts in Chrome, Android, or Web API  │
│                                                               │
│  5. SEE DYNAMIC_VISUALS_GUIDE.md for animated diagrams       │
│     SVG, Mermaid, D3.js, CSS animation techniques            │
│                                                               │
│  6. EXPLORE linkedin_special/ for animated HTML examples     │
│     Open .html files in browser to see flowing animations    │
│                                                               │
└──────────────────────────────────────────────────────────────┘
```

---

## Prompt Concept Overview

```
THE 15 PROMPT CONCEPTS AT A GLANCE:

┌─ BASICS ──────────────────────────────────────────────────┐
│  01 Foundational    │ Zero-shot, direct, template-based   │
│  02 Chain-of-Thought│ Step-by-step reasoning              │
│  03 Few-Shot        │ Learning from examples              │
│  04 Role-Based      │ Expert persona assignment           │
└───────────────────────────────────────────────────────────┘

┌─ CONTENT CREATION ────────────────────────────────────────┐
│  05 Visual/Diagram  │ Flowcharts, architecture diagrams   │
│  06 Tutorial Gen    │ Step-by-step guides, quick starts   │
│  07 PDF Analysis    │ Document extraction & summarization │
└───────────────────────────────────────────────────────────┘

┌─ ADVANCED TECHNIQUES ─────────────────────────────────────┐
│  08 Dynamic         │ Conversational, conditional, games  │
│  09 Comparative     │ Technology comparisons, matrices    │
│  10 Storytelling    │ Analogies, scenarios, narratives    │
│  11 Code Gen/Debug  │ Generation, debugging, review       │
└───────────────────────────────────────────────────────────┘

┌─ SPECIALIZED ─────────────────────────────────────────────┐
│  12 Assessment/Quiz │ MCQ, coding challenges, evaluation  │
│  13 Data Viz        │ Charts, dashboards, infographics    │
│  14 Summarization   │ Executive briefs, tiered summaries  │
│  15 Creative        │ SCAMPER, reverse thinking, mind maps│
└───────────────────────────────────────────────────────────┘
```

---

## Concept 1: Foundational Prompts

**Folder:** [01-foundational-prompts/](01-foundational-prompts/)

The building blocks of prompt engineering. Start here if you're new.

```
TYPES:
├─ Zero-Shot:     Ask directly without examples
├─ Direct:        Clear, specific instructions
└─ Template-Based: Structured output format
```

**When to Use:** Simple questions, quick answers, structured output needs.

**Example:**
```
Prompt: "List the top 5 JavaScript frameworks for 2025 with one-line descriptions."
```

**Best Platform:** All platforms (Chrome, Android, Web API)

---

## Concept 2: Chain-of-Thought Prompts

**Folder:** [02-chain-of-thought-prompts/](02-chain-of-thought-prompts/)

Force the model to show its reasoning step by step.

```
TYPES:
├─ Step-by-Step:  "Think through this step by step..."
├─ Reasoning:     "Show your reasoning at each stage..."
└─ Problem Solve: "Break down the problem, then solve..."
```

**When to Use:** Math problems, debugging, complex analysis, decision-making.

**Example:**
```
Prompt: "A server handles 100 requests/sec. If traffic doubles every hour
starting at 9 AM, when will it exceed 10,000 req/sec? Show your work."
```

**Best Platform:** Web API (longer outputs), Chrome (shorter problems)

---

## Concept 3: Few-Shot Prompts

**Folder:** [03-few-shot-prompts/](03-few-shot-prompts/)

Teach the model by providing examples before your actual request.

```
TYPES:
├─ Classification:   Show labeled examples, then classify new input
├─ Format Matching:  Show output format, then apply to new input
└─ Pattern Learning: Show a pattern, then extend it
```

**When to Use:** Consistent formatting, classification tasks, custom output styles.

**Example:**
```
Prompt:
"Convert to formal English:
 Input: 'gonna grab lunch brb' → Output: 'I will be taking a lunch break shortly.'
 Input: 'cant make it tmrw' → Output: 'I will be unable to attend tomorrow.'
 Input: 'lmk if u need help' → Output: ?"
```

**Best Platform:** All platforms (keep to 2-3 examples for on-device)

---

## Concept 4: Role-Based Prompts

**Folder:** [04-role-based-prompts/](04-role-based-prompts/)

Assign an expert persona to get specialized responses.

```
TYPES:
├─ Technical Expert:  "You are a senior DevOps engineer..."
├─ Teacher/Tutor:     "You are a patient CS professor..."
└─ Domain Specialist: "You are a cybersecurity analyst..."
```

**When to Use:** Expert-level advice, teaching, domain-specific answers.

**Example:**
```
Prompt: "You are a database performance expert. My PostgreSQL query takes 30
seconds on a 10M row table. The query joins 3 tables with WHERE clauses on
non-indexed columns. Diagnose and fix this."
```

**Best Platform:** All platforms (use systemPrompt for Chrome/Android)

---

## Concept 5: Visual & Diagram Prompts

**Folder:** [05-visual-diagram-prompts/](05-visual-diagram-prompts/)

Generate flowcharts, architecture diagrams, and visual representations.

```
TYPES:
├─ Flowcharts:     Process flows with decision points
├─ Architecture:   System design diagrams
└─ ASCII Diagrams: Text-based visual representations
```

**When to Use:** Documentation, system design, explaining processes.

**Best Platform:** Web API (complex diagrams), Chrome (simple flowcharts)

---

## Concept 6: Tutorial Generation Prompts

**Folder:** [06-tutorial-generation-prompts/](06-tutorial-generation-prompts/)

Create step-by-step learning content.

```
TYPES:
├─ Quick Start:      5-minute getting-started guides
├─ Project-Based:    Build something from scratch
└─ Deep Dive:        Comprehensive topic coverage
```

**When to Use:** Onboarding docs, learning materials, README creation.

**Best Platform:** Web API (long tutorials), Chrome (quick starts)

---

## Concept 7: PDF Analysis Prompts

**Folder:** [07-pdf-analysis-prompts/](07-pdf-analysis-prompts/)

Extract and analyze information from documents.

```
TYPES:
├─ Content Extraction:   Pull specific data from text
├─ Summarization:        Condense document content
└─ Table Extraction:     Parse structured data from text
```

**When to Use:** Report analysis, data extraction, document processing.

**Best Platform:** Web API (large documents), Android (small docs)

---

## Concept 8: Dynamic Interactive Prompts

**Folder:** [08-dynamic-interactive-prompts/](08-dynamic-interactive-prompts/)

Create conversational and adaptive interactions.

```
TYPES:
├─ Conversational Flow:     Multi-turn guided dialogue
├─ Conditional Responses:   Branch based on user input
└─ Interactive Exercises:   Gamified learning activities
```

**When to Use:** Chatbots, tutoring apps, interactive guides.

**Best Platform:** Android (apps), Chrome (web apps)

---

## Concept 9: Comparative Analysis Prompts

**Folder:** [09-comparative-analysis-prompts/](09-comparative-analysis-prompts/)

Compare options systematically with structured analysis.

```
TYPES:
├─ Technology Comparison:  Side-by-side tech evaluation
├─ Pros/Cons Analysis:     Weighted advantage comparison
└─ Decision Matrix:        Scored criteria evaluation
```

**When to Use:** Technology selection, architecture decisions, vendor evaluation.

**Best Platform:** Web API (detailed analysis), Chrome (quick comparisons)

---

## Concept 10: Storytelling & Narrative Prompts

**Folder:** [10-storytelling-narrative-prompts/](10-storytelling-narrative-prompts/)

Explain complex topics through stories and analogies.

```
TYPES:
├─ Analogy-Based:     Explain tech using real-world parallels
├─ Scenario Building: Create realistic problem scenarios
└─ Narrative:         Structure explanations as stories
```

**When to Use:** Teaching, presentations, making complex topics accessible.

**Best Platform:** All platforms

---

## Concept 11: Code Generation & Debug Prompts

**Folder:** [11-code-generation-debug-prompts/](11-code-generation-debug-prompts/)

Generate, debug, and review code.

```
TYPES:
├─ Code Generation:   Create functions/APIs from specs
├─ Debugging:         Systematic bug analysis
└─ Code Review:       Security and performance review
```

**When to Use:** Development, code review automation, learning to code.

**Best Platform:** Web API (complex generation), Chrome (snippets)

---

## Concept 12: Assessment & Quiz Prompts

**Folder:** [12-assessment-quiz-prompts/](12-assessment-quiz-prompts/)

Create quizzes, challenges, and knowledge assessments.

```
TYPES:
├─ Multiple Choice:       MCQ with explanations
├─ Coding Challenges:     Algorithm problems with solutions
└─ Knowledge Assessment:  Skill-level evaluation
```

**When to Use:** Education apps, interview prep, self-assessment.

**Best Platform:** Android (study apps), Web API (generation)

---

## Concept 13: Data Visualization Prompts

**Folder:** [13-data-visualization-prompts/](13-data-visualization-prompts/)

Transform data into charts, dashboards, and infographics.

```
TYPES:
├─ Chart Generation:  Line, bar, pie charts from data
├─ Dashboard Design:  KPI dashboards and monitoring layouts
└─ Infographics:      Visual data storytelling
```

**When to Use:** Reports, dashboards, data presentations.

**Best Platform:** Web API (generates chart code)

---

## Concept 14: Summarization Prompts

**Folder:** [14-summarization-prompts/](14-summarization-prompts/)

Condense information at different levels of detail.

```
TYPES:
├─ Executive Summary:    C-level brief format
├─ Tiered Summary:       Tweet → Paragraph → Detailed
└─ Key Points:           Ranked extraction with priorities
```

**When to Use:** Report writing, email digests, meeting notes.

**Best Platform:** All platforms (excellent for on-device)

---

## Concept 15: Creative & Brainstorming Prompts

**Folder:** [15-creative-brainstorming-prompts/](15-creative-brainstorming-prompts/)

Generate ideas using structured creative thinking methods.

```
TYPES:
├─ Idea Generation:    SCAMPER method brainstorming
├─ Reverse Thinking:   Inversion-based problem solving
└─ Mind Mapping:       Hierarchical topic exploration
```

**When to Use:** Product ideation, problem solving, planning sessions.

**Best Platform:** All platforms

---

## Choosing the Right Prompt Type

```
DECISION FLOWCHART:

What do you need?
│
├─ Quick answer → 01 Foundational (Zero-Shot)
├─ Show reasoning → 02 Chain-of-Thought
├─ Consistent format → 03 Few-Shot
├─ Expert opinion → 04 Role-Based
├─ Visual diagram → 05 Visual/Diagram
├─ Teaching content → 06 Tutorial Generation
├─ Analyze document → 07 PDF Analysis
├─ Interactive chat → 08 Dynamic Interactive
├─ Compare options → 09 Comparative Analysis
├─ Explain simply → 10 Storytelling
├─ Write/fix code → 11 Code Gen/Debug
├─ Test knowledge → 12 Assessment/Quiz
├─ Show data → 13 Data Visualization
├─ Shorten content → 14 Summarization
└─ Generate ideas → 15 Creative/Brainstorming
```

---

## Tips & Best Practices

### General Tips

```
┌──────────────────────────────────────────────────────────────┐
│  TOP 10 PROMPT ENGINEERING TIPS                               │
│                                                               │
│  1. BE SPECIFIC: "List 5 items" not "list some items"        │
│  2. SET FORMAT: "Respond as a table/list/JSON"               │
│  3. SET CONSTRAINTS: "Max 100 words" or "3 sentences"        │
│  4. GIVE CONTEXT: "For a beginner audience..."               │
│  5. USE EXAMPLES: Show desired output format first           │
│  6. ITERATE: Refine prompts based on output quality          │
│  7. CHAIN PROMPTS: Break complex tasks into steps            │
│  8. SET TONE: "Professional/casual/technical"                │
│  9. REQUEST STRUCTURE: "Use headers and bullet points"       │
│ 10. VALIDATE: Ask model to verify its own output             │
└──────────────────────────────────────────────────────────────┘
```

### Prompt Length Guidelines

```
ON-DEVICE (Chrome/Android Nano Bana):
├─ Prompt: Keep under 500 tokens
├─ Few-Shot: Max 2-3 examples
├─ Response: Expect 100-500 tokens
└─ Best for: Quick, simple tasks

WEB API (Gemini Pro/Flash):
├─ Prompt: Up to 30,000 tokens
├─ Few-Shot: 5-10 examples fine
├─ Response: Up to 8,000 tokens
└─ Best for: Complex, detailed tasks
```

### Combining Prompt Types

```
POWER COMBINATIONS:
┌───────────────────────────────────────────────────────────┐
│ Role-Based + Chain-of-Thought                             │
│ = Expert who shows their reasoning                        │
│                                                           │
│ Few-Shot + Summarization                                  │
│ = Consistently formatted summaries                        │
│                                                           │
│ Storytelling + Tutorial                                   │
│ = Engaging learning content                               │
│                                                           │
│ Comparative + Decision Matrix                             │
│ = Data-driven technology selection                        │
│                                                           │
│ Code Generation + Code Review                             │
│ = Self-reviewed code output                               │
└───────────────────────────────────────────────────────────┘
```
