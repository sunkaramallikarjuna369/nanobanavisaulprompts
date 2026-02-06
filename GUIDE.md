# Gemini Nano Bana Visual Prompt Library Guide

## What is This Library?

A collection of **150 prompts** designed for Gemini Nano Bana to transform any content into visual learning materials. Organized by **transformation type** (what you have → what you get).

## 12 Transformation Categories

### Input → Output Model

Each category takes a specific input type and transforms it into a visual output:

| # | Category | Input | Output | Prompts |
|---|----------|-------|--------|---------|
| 1 | [PDF to Visual Learning](01-pdf-to-visual-learning/) | PDFs, documents | Whiteboards, infographics, mind maps | 1-10 |
| 2 | [Text to Diagrams](02-text-to-diagrams/) | Plain text, descriptions | Flowcharts, architecture diagrams, ER diagrams | 11-20 |
| 3 | [Code to Visual](03-code-to-visual/) | Source code, algorithms | Execution flows, UML, state machines | 21-30 |
| 4 | [Data to Visualizations](04-data-to-visualizations/) | Datasets, CSVs, numbers | Dashboards, charts, heatmaps | 31-40 |
| 5 | [Concepts to Comics/Stories](05-concepts-to-comics-stories/) | Abstract ideas, processes | Comics, metaphors, roadmaps | 41-50 |
| 6 | [Notes to Study Materials](06-notes-to-study-materials/) | Lecture notes, study notes | Flashcards, cheat sheets, sketchnotes | 51-60 |
| 7 | [Business to Visual Strategy](07-business-to-visual-strategy/) | Business plans, reports | Canvases, SWOT, dashboards, roadmaps | 61-70 |
| 8 | [Science to Illustrations](08-science-to-illustrations/) | Scientific text, processes | Diagrams, lab setups, ecosystems | 71-80 |
| 9 | [Math to Visual Proofs](09-math-to-visual-proofs/) | Equations, theorems | Visual proofs, graphs, distributions | 81-90 |
| 10 | [Technical Docs to Tutorials](10-technical-docs-to-tutorials/) | API docs, configs, guides | Quick-starts, cheat sheets, pipelines | 91-100 |
| 11 | [Articles to Social Media](11-articles-to-social-media/) | Blog posts, articles | Carousels, threads, thumbnails | 101-110 |
| 12 | [Meetings to Action Items](12-meetings-to-action-items/) | Meeting notes, discussions | Kanban boards, RACI matrices, Gantt charts | 111-120 |

### Dynamic / Interactive Prompts

| # | Category | Prompts |
|---|----------|---------|
| 13 | [Dynamic Interactive Prompts](13-dynamic-interactive-prompts/) | 30 prompts for interactive UI generation |

## How to Use

### Step 1: Identify Your Input
What do you have? A PDF? Code? Meeting notes? Data?

### Step 2: Pick a Category
Match your input type to one of the 12 categories above.

### Step 3: Choose a Prompt
Each category has 10 prompts. Pick the visual output style you want.

### Step 4: Copy and Customize
Copy the prompt from the prompts.md file. Replace the example input with your actual content.

### Step 5: Make It Interactive (Optional)
Add the dynamic view wrapper from [Category 13](13-dynamic-interactive-prompts/README.md) to make any static prompt interactive.

## Where to Use These Prompts

### Google AI Studio
1. Go to [aistudio.google.com](https://aistudio.google.com)
2. Select Gemini model
3. Paste prompt + your content
4. Get visual output

### Chrome DevTools (Nano Bana)
1. Open Chrome DevTools (F12)
2. Navigate to AI panel
3. Use Nano Bana model
4. Paste prompt for on-device processing

### Android Integration
```kotlin
val model = GenerativeModel("gemini-nano")
val response = model.generateContent(prompt + yourContent)
```

### Web API
```javascript
const response = await fetch('https://generativelanguage.googleapis.com/v1/models/gemini-nano:generateContent', {
  method: 'POST',
  headers: { 'Content-Type': 'application/json' },
  body: JSON.stringify({ contents: [{ parts: [{ text: prompt }] }] })
});
```

## Prompt Structure

Every prompt in this library follows this pattern:

```
[Action verb] this [input type] into a [output visual type] with [specific elements], [layout details], and [styling notes].
```

**Elements of a good visual prompt:**
- **Action:** Transform, Convert, Turn, Create
- **Input:** PDF, text, code, data, notes, business plan
- **Output:** Whiteboard, flowchart, dashboard, comic, flashcard
- **Details:** Colors, labels, arrows, interactions, layout

## Tips for Best Results

1. **Be specific about visual elements** - mention colors, arrows, boxes, labels
2. **Include layout instructions** - top-to-bottom, left-to-right, grid, timeline
3. **Specify interaction style** - clickable, hoverable, expandable (for dynamic prompts)
4. **Provide real input** - attach actual PDF/code/data, not just descriptions
5. **Iterate** - refine the prompt based on initial output
