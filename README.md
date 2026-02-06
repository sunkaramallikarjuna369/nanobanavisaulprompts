# Gemini Nano Bana Visual Prompt Library

**150 prompts** to transform any content into visual learning materials using Gemini Nano Bana.

Organized by **transformation type**: what you have → what you get.

## Quick Navigation

### Static Visual Prompts (120 prompts)

| # | Category | What You Have | What You Get | Prompts |
|---|----------|--------------|--------------|---------|
| 1 | [PDF to Visual Learning](01-pdf-to-visual-learning/) | PDFs, documents | Whiteboards, infographics, mind maps | 10 |
| 2 | [Text to Diagrams](02-text-to-diagrams/) | Plain text | Flowcharts, architecture, ER diagrams | 10 |
| 3 | [Code to Visual](03-code-to-visual/) | Source code | Execution flows, UML, state machines | 10 |
| 4 | [Data to Visualizations](04-data-to-visualizations/) | Datasets, CSVs | Dashboards, charts, heatmaps | 10 |
| 5 | [Concepts to Comics](05-concepts-to-comics-stories/) | Abstract ideas | Comics, metaphors, roadmaps | 10 |
| 6 | [Notes to Study Materials](06-notes-to-study-materials/) | Lecture notes | Flashcards, cheat sheets, sketchnotes | 10 |
| 7 | [Business to Strategy](07-business-to-visual-strategy/) | Business plans | Canvases, SWOT, dashboards | 10 |
| 8 | [Science to Illustrations](08-science-to-illustrations/) | Scientific text | Diagrams, lab setups, ecosystems | 10 |
| 9 | [Math to Visual Proofs](09-math-to-visual-proofs/) | Equations, theorems | Visual proofs, graphs, distributions | 10 |
| 10 | [Tech Docs to Tutorials](10-technical-docs-to-tutorials/) | API docs, configs | Quick-starts, cheat sheets, pipelines | 10 |
| 11 | [Articles to Social Media](11-articles-to-social-media/) | Blog posts | Carousels, threads, thumbnails | 10 |
| 12 | [Meetings to Action Items](12-meetings-to-action-items/) | Meeting notes | Kanban, RACI, Gantt charts | 10 |

### Dynamic / Interactive Prompts (30 prompts)

| # | Category | Description | Prompts |
|---|----------|-------------|---------|
| 13 | [Dynamic Interactive](13-dynamic-interactive-prompts/) | Interactive UI with clicks, hovers, filters | 30 |

### Resources

| Resource | Description |
|----------|-------------|
| [GUIDE.md](GUIDE.md) | How to use this library, where to apply prompts |
| [sample-outputs/](sample-outputs/) | SVG notebook + HTML interactive whiteboard examples |
| [gemini_visual_prompts.csv](gemini_visual_prompts.csv) | All 120 static prompts in CSV format |

## How It Works

```
┌─────────────┐     ┌──────────────────┐     ┌─────────────────┐
│  Your Input  │ ──→ │  Pick a Prompt   │ ──→ │  Visual Output  │
│  (PDF/Code/  │     │  from category   │     │  (Diagram/Chart │
│   Data/etc)  │     │  + customize     │     │   /Dashboard)   │
└─────────────┘     └──────────────────┘     └─────────────────┘
```

1. **Identify your input** → PDF? Code? Notes? Data?
2. **Pick a category** → Match input type to one of 12 categories
3. **Choose a prompt** → Each category has 10 visual styles
4. **Copy, paste, customize** → Replace example with your content
5. **Make interactive** (optional) → Add dynamic view wrapper from Category 13

## Folder Structure

```
├── 01-pdf-to-visual-learning/     (prompts 1-10)
├── 02-text-to-diagrams/           (prompts 11-20)
├── 03-code-to-visual/             (prompts 21-30)
├── 04-data-to-visualizations/     (prompts 31-40)
├── 05-concepts-to-comics-stories/ (prompts 41-50)
├── 06-notes-to-study-materials/   (prompts 51-60)
├── 07-business-to-visual-strategy/(prompts 61-70)
├── 08-science-to-illustrations/   (prompts 71-80)
├── 09-math-to-visual-proofs/      (prompts 81-90)
├── 10-technical-docs-to-tutorials/(prompts 91-100)
├── 11-articles-to-social-media/   (prompts 101-110)
├── 12-meetings-to-action-items/   (prompts 111-120)
├── 13-dynamic-interactive-prompts/(30 interactive prompts)
├── sample-outputs/                (SVG + HTML examples)
├── GUIDE.md                       (usage guide)
├── gemini_visual_prompts.csv      (CSV export)
└── README.md                      (this file)
```

## Each Prompt Includes

- **Prompt text** ready to copy-paste
- **Input → Output example** showing what to expect
- **Visual style description** for the expected output

## Target Platform

Designed for **Gemini Nano Bana** but works with any Gemini model:
- Google AI Studio
- Chrome DevTools (on-device)
- Android AICore
- Gemini API
