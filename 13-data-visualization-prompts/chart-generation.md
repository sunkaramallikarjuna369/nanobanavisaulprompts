# Chart Generation Prompts for Gemini Nano Bana

```
╔══════════════════════════════════════════════════════════════╗
║              CHART GENERATION PROMPTS                         ║
╚══════════════════════════════════════════════════════════════╝
```

---

## Prompt 1: Multi-Chart Data Analysis

### Prompt
```
Given this sales data for 2025:
Q1: $120K, Q2: $185K, Q3: $142K, Q4: $210K
Products: Software (60%), Services (25%), Hardware (15%)

Create 3 different chart representations:
1. Line chart showing quarterly trend
2. Pie chart showing product breakdown
3. Bar chart comparing quarters
Include insights from each visualization.
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│  1. QUARTERLY TREND (Line Chart)                             │
│                                                               │
│  $210K │                                          ●          │
│  $185K │              ●                          /           │
│  $142K │                          ●             /            │
│  $120K │  ●                        \           /             │
│        │   \          /             \         /              │
│        └────Q1───────Q2──────────Q3─────────Q4───           │
│                                                               │
│  Insight: Strong recovery in Q4 after Q3 dip (+47.9%)       │
│                                                               │
│  2. PRODUCT MIX (Pie Chart)                                  │
│                                                               │
│  ████████████████████████ Software 60%                       │
│  ██████████ Services 25%                                     │
│  ██████ Hardware 15%                                         │
│                                                               │
│  Insight: Software dominates; consider growing Services      │
│                                                               │
│  3. QUARTERLY COMPARISON (Bar Chart)                         │
│                                                               │
│  Q1 ████████████░░░░░░░░░░░░░░░░░░ $120K                   │
│  Q2 ██████████████████░░░░░░░░░░░░ $185K                    │
│  Q3 ██████████████░░░░░░░░░░░░░░░░ $142K                    │
│  Q4 █████████████████████░░░░░░░░░ $210K ← Peak            │
│                                                               │
│  Insight: Q4 highest revenue, Q1 needs improvement          │
└──────────────────────────────────────────────────────────────┘
```

---

## Image Examples

| Prompt | Expected Image Type | Description |
|--------|-------------------|-------------|
| Multi-chart analysis | Dashboard with 3 panels | Line chart, pie chart, and bar chart arranged in a grid with insight cards |
