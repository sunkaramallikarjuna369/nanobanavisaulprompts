# Decision Matrix Prompts for Gemini Nano Bana

```
╔══════════════════════════════════════════════════════════════╗
║               DECISION MATRIX PROMPTS                        ║
╚══════════════════════════════════════════════════════════════╝
```

---

## Prompt 1: Weighted Scoring Matrix

### Prompt
```
Create a decision matrix to choose a cloud provider (AWS, GCP, Azure)
for a healthcare startup. Criteria and weights:
- HIPAA compliance (weight: 5)
- Cost for startup tier (weight: 4)
- AI/ML services (weight: 4)
- Documentation quality (weight: 3)
- Support response time (weight: 3)
Score each 1-10 and calculate weighted totals.
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│  CLOUD PROVIDER DECISION MATRIX                              │
│                                                               │
│  Criteria         │ Wt │ AWS     │ GCP     │ Azure   │     │
│  ─────────────────┼────┼─────────┼─────────┼─────────┤     │
│  HIPAA Compliance │  5 │ 9 (45)  │ 8 (40)  │ 9 (45)  │     │
│  Startup Cost     │  4 │ 7 (28)  │ 8 (32)  │ 7 (28)  │     │
│  AI/ML Services   │  4 │ 9 (36)  │ 9 (36)  │ 8 (32)  │     │
│  Documentation    │  3 │ 8 (24)  │ 9 (27)  │ 7 (21)  │     │
│  Support Speed    │  3 │ 7 (21)  │ 7 (21)  │ 8 (24)  │     │
│  ─────────────────┼────┼─────────┼─────────┼─────────┤     │
│  WEIGHTED TOTAL   │ 19 │   154   │   156   │   150   │     │
│                                                               │
│  WINNER: GCP (156 pts) ← Best for AI + cost efficiency      │
│  Runner-up: AWS (154 pts) ← Best ecosystem breadth          │
└──────────────────────────────────────────────────────────────┘
```

---

## Image Examples

| Prompt | Expected Image Type | Description |
|--------|-------------------|-------------|
| Weighted matrix | Heatmap table | Color-coded cells (green=high, red=low) with bold winner row |
