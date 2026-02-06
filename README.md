# Gemini Nano Bana - Prompt Engineering Library

```
╔══════════════════════════════════════════════════════════════════════════╗
║                                                                          ║
║     ██████╗ ███████╗███╗   ███╗██╗███╗   ██╗██╗                        ║
║    ██╔════╝ ██╔════╝████╗ ████║██║████╗  ██║██║                        ║
║    ██║  ███╗█████╗  ██╔████╔██║██║██╔██╗ ██║██║                        ║
║    ██║   ██║██╔══╝  ██║╚██╔╝██║██║██║╚██╗██║██║                        ║
║    ╚██████╔╝███████╗██║ ╚═╝ ██║██║██║ ╚████║██║                        ║
║     ╚═════╝ ╚══════╝╚═╝     ╚═╝╚═╝╚═╝  ╚═══╝╚═╝                        ║
║                                                                          ║
║     NANO BANA VISUAL PROMPT ENGINEERING LIBRARY                          ║
║     360° Coverage | 15 Concepts | 45+ Types | 90+ Examples              ║
║                                                                          ║
╚══════════════════════════════════════════════════════════════════════════╝
```

> A comprehensive prompt engineering library for **Gemini Nano Bana** with visual examples, animated diagrams, dynamic visual procedures, and complete integration guides.

---

## Quick Navigation

| # | Concept Folder | Description | Prompt Types |
|---|---------------|-------------|-------------|
| 01 | [Foundational Prompts](01-foundational-prompts/) | Zero-shot, direct instruction, template-based | 3 |
| 02 | [Chain-of-Thought](02-chain-of-thought-prompts/) | Step-by-step reasoning and problem solving | 3 |
| 03 | [Few-Shot Prompts](03-few-shot-prompts/) | Learning from examples, pattern matching | 3 |
| 04 | [Role-Based Prompts](04-role-based-prompts/) | Expert persona assignment | 3 |
| 05 | [Visual & Diagram](05-visual-diagram-prompts/) | Flowcharts, architecture, ASCII diagrams | 3 |
| 06 | [Tutorial Generation](06-tutorial-generation-prompts/) | Step-by-step guides, project-based learning | 3 |
| 07 | [PDF Analysis](07-pdf-analysis-prompts/) | Document extraction, summarization, tables | 3 |
| 08 | [Dynamic Interactive](08-dynamic-interactive-prompts/) | Conversational flow, conditional, exercises | 3 |
| 09 | [Comparative Analysis](09-comparative-analysis-prompts/) | Tech comparison, pros/cons, decision matrix | 3 |
| 10 | [Storytelling & Narrative](10-storytelling-narrative-prompts/) | Analogies, scenarios, narrative structure | 3 |
| 11 | [Code Gen & Debug](11-code-generation-debug-prompts/) | Code generation, debugging, code review | 3 |
| 12 | [Assessment & Quiz](12-assessment-quiz-prompts/) | MCQ, coding challenges, skill assessment | 3 |
| 13 | [Data Visualization](13-data-visualization-prompts/) | Charts, dashboards, infographics | 3 |
| 14 | [Summarization](14-summarization-prompts/) | Executive briefs, tiered summaries, key points | 3 |
| 15 | [Creative & Brainstorming](15-creative-brainstorming-prompts/) | SCAMPER, reverse thinking, mind mapping | 3 |

---

## Guides & Special Sections

| Guide | Description |
|-------|-------------|
| [GUIDE.md](GUIDE.md) | Master guide explaining all 15 prompt concepts with usage tips |
| [WHERE_TO_USE_NANO_BANA.md](WHERE_TO_USE_NANO_BANA.md) | Where & how to apply prompts (Chrome, Android, Web API) |
| [DYNAMIC_VISUALS_GUIDE.md](DYNAMIC_VISUALS_GUIDE.md) | Executive guide for SVG, Mermaid, D3.js, CSS animations |
| [linkedin_special/](linkedin_special/) | Animated HTML diagrams with flowing lines (open in browser) |

---

## LinkedIn-Style Animated Diagrams

The `linkedin_special/` folder contains **6 runnable HTML files** with animated flowing diagrams:

| File | Animation |
|------|-----------|
| [AI Systems Roadmap](linkedin_special/01-flowing-roadmap.html) | Flowing path with pulsing milestone nodes |
| [Prompt Engineering Mind Map](linkedin_special/02-animated-mindmap.html) | Animated mind map with branching connections |
| [Tech Stack Flow](linkedin_special/03-tech-stack-flow.html) | Animated data pipeline through system layers |
| [ML Pipeline](linkedin_special/04-process-pipeline.html) | Flowing gradient lines through ML stages |
| [Neural Network](linkedin_special/05-network-visualization.html) | Animated signal propagation visualization |
| [Career Timeline](linkedin_special/06-timeline-flow.html) | Animated milestone timeline flow |

> Open any `.html` file in your browser to see the animations!

---

## How to Use This Library

```
START HERE
    │
    ├─── New to prompts? ──→ Read GUIDE.md first
    │
    ├─── Know what you need? ──→ Browse concept folders (01-15)
    │
    ├─── Want animated visuals? ──→ See linkedin_special/ folder
    │
    ├─── Building an app? ──→ Read WHERE_TO_USE_NANO_BANA.md
    │
    └─── Want dynamic diagrams? ──→ Read DYNAMIC_VISUALS_GUIDE.md
```

### Quick Start

1. **Pick a concept folder** (e.g., `04-role-based-prompts/`)
2. **Read the README** in that folder for an overview
3. **Open a prompt type file** (e.g., `technical-expert.md`)
4. **Copy the prompt template** and replace `[placeholders]` with your content
5. **Use it** in Chrome DevTools, Android app, or via Web API

---

## Platform Support

```
┌────────────────────┬──────────┬──────────┬──────────┐
│ Feature            │ Chrome   │ Android  │ Web API  │
├────────────────────┼──────────┼──────────┼──────────┤
│ On-device AI       │    ✓     │    ✓     │    ✗     │
│ Privacy (no cloud) │    ✓     │    ✓     │    ✗     │
│ Complex prompts    │  Basic   │  Basic   │    ✓     │
│ Long outputs       │  Short   │  Short   │    ✓     │
│ Offline capable    │    ✗     │    ✓     │    ✗     │
│ Streaming          │    ✓     │    ✓     │    ✓     │
└────────────────────┴──────────┴──────────┴──────────┘
```

---

## Repository Structure

```
nanobanavisaulprompts/
├── README.md                          ← You are here
├── GUIDE.md                           ← Master prompt guide
├── WHERE_TO_USE_NANO_BANA.md          ← Integration guide
├── DYNAMIC_VISUALS_GUIDE.md           ← Dynamic visuals guide
│
├── 01-foundational-prompts/           ← Basic prompt types
│   ├── README.md
│   ├── zero-shot-prompts.md
│   ├── direct-instruction.md
│   └── template-based.md
│
├── 02-chain-of-thought-prompts/       ← Reasoning prompts
│   └── ...
├── 03-few-shot-prompts/               ← Example-based prompts
│   └── ...
├── 04-role-based-prompts/             ← Expert persona prompts
│   └── ...
├── 05-visual-diagram-prompts/         ← Visual generation
│   └── ...
├── 06-tutorial-generation-prompts/    ← Tutorial creation
│   └── ...
├── 07-pdf-analysis-prompts/           ← Document analysis
│   └── ...
├── 08-dynamic-interactive-prompts/    ← Interactive prompts
│   └── ...
├── 09-comparative-analysis-prompts/   ← Comparison prompts
│   └── ...
├── 10-storytelling-narrative-prompts/ ← Narrative prompts
│   └── ...
├── 11-code-generation-debug-prompts/  ← Code prompts
│   └── ...
├── 12-assessment-quiz-prompts/        ← Quiz prompts
│   └── ...
├── 13-data-visualization-prompts/     ← Data viz prompts
│   └── ...
├── 14-summarization-prompts/          ← Summary prompts
│   └── ...
├── 15-creative-brainstorming-prompts/ ← Creative prompts
│   └── ...
│
└── linkedin_special/                  ← Animated HTML diagrams
    ├── README.md
    ├── prompts-for-dynamic-visuals.md
    ├── 01-flowing-roadmap.html
    ├── 02-animated-mindmap.html
    ├── 03-tech-stack-flow.html
    ├── 04-process-pipeline.html
    ├── 05-network-visualization.html
    └── 06-timeline-flow.html
```

---

## Contributing

Feel free to add new prompt types, improve examples, or create additional animated diagrams. Each concept folder follows the same structure:

```
XX-concept-name/
├── README.md              ← Overview + links
├── prompt-type-1.md       ← Prompt + example + ASCII visual
├── prompt-type-2.md       ← Prompt + example + ASCII visual
└── prompt-type-3.md       ← Prompt + example + ASCII visual
```

---

*Built with prompt engineering expertise for the Gemini Nano Bana community.*
