# Chart & Data Visualization Prompts for Gemini Nano Bana

```
╔══════════════════════════════════════════════════════════════╗
║            CHART & DATA VISUALIZATION PROMPTS                ║
╚══════════════════════════════════════════════════════════════╝
```

---

## Prompt 1: Bar Chart with Comparison

### Prompt
```
Create a horizontal bar chart comparing the performance of 5 LLMs:
GPT-4 (92%), Claude 3 (89%), Gemini Ultra (88%), Llama 3 (82%),
Mistral (79%). Use color-coded bars and show percentage labels.
```

### Expected Visual Output
```
  LLM Performance Benchmark (MMLU Score)
  ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

  GPT-4      ████████████████████████████████████████████░░ 92%
  Claude 3   ██████████████████████████████████████████░░░░ 89%
  Gemini     █████████████████████████████████████████░░░░░ 88%
  Llama 3    ████████████████████████████████████░░░░░░░░░░ 82%
  Mistral    ██████████████████████████████████░░░░░░░░░░░░ 79%

  Legend: ████ Score  ░░░░ Remaining
```

---

## Prompt 2: Pie Chart Distribution

### Prompt
```
Create a text-based pie chart showing cloud market share:
AWS 31%, Azure 25%, Google Cloud 11%, Alibaba 4%, Others 29%.
Include a visual representation and percentage labels.
```

### Expected Visual Output
```
  Cloud Market Share 2025
  ━━━━━━━━━━━━━━━━━━━━━━

         ┌───────────────┐
        /  AWS    31%    \
       / ████████████     \
      |  Azure   25%      |
      |  ▓▓▓▓▓▓▓▓▓        |
      |  GCP     11%      |
       \ ░░░░░            /
        \ Others  33%    /
         └───────────────┘

  ████ AWS (31%)     ▓▓▓▓ Azure (25%)
  ░░░░ GCP (11%)    ▒▒▒▒ Alibaba (4%)
  ···· Others (29%)
```

---

## Prompt 3: Timeline/Gantt Chart

### Prompt
```
Create a Gantt chart for a 12-week AI project with phases:
Research (weeks 1-3), Data Collection (weeks 2-5),
Model Development (weeks 4-8), Testing (weeks 7-10),
Deployment (weeks 9-12). Show overlapping phases.
```

### Expected Visual Output
```
  AI Project Timeline (12 Weeks)
  ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  Week:    1  2  3  4  5  6  7  8  9  10 11 12
           │  │  │  │  │  │  │  │  │  │  │  │
  Research ████████████
  Data        ████████████████
  Model             ████████████████████
  Testing                    ████████████████
  Deploy                           ████████████

  ████ Active Phase    Overlaps show parallel work
```

---

## Image Examples

| Prompt | Expected Image Type | Description |
|--------|-------------------|-------------|
| Bar chart | Colored horizontal bars | Gradient bars with value labels, sorted by performance |
| Pie chart | Donut/pie chart | Color-coded segments with percentage labels and legend |
| Gantt chart | Timeline bars | Overlapping colored bars showing project phases |
