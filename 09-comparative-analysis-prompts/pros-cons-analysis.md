# Pros & Cons Analysis Prompts for Gemini Nano Bana

```
╔══════════════════════════════════════════════════════════════╗
║             PROS & CONS ANALYSIS PROMPTS                     ║
╚══════════════════════════════════════════════════════════════╝
```

---

## Prompt 1: Weighted Pros/Cons

### Prompt
```
Analyze the pros and cons of migrating from a monolithic 
architecture to microservices for a mid-size e-commerce platform 
(50K daily users). Weight each pro/con by impact (High/Med/Low) 
and effort required. Give a final recommendation with confidence %.
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│  MONOLITH → MICROSERVICES ANALYSIS                           │
│                                                               │
│  PROS                          │ Impact │ Effort │          │
│  ──────────────────────────────┼────────┼────────┤          │
│  ✅ Independent deployments    │ HIGH   │ Medium │          │
│  ✅ Technology flexibility     │ MEDIUM │ Low    │          │
│  ✅ Team autonomy              │ HIGH   │ Medium │          │
│  ✅ Horizontal scaling         │ HIGH   │ High   │          │
│  ✅ Fault isolation            │ MEDIUM │ Medium │          │
│                                                               │
│  CONS                          │ Impact │ Effort │          │
│  ──────────────────────────────┼────────┼────────┤          │
│  ❌ Network complexity         │ HIGH   │ High   │          │
│  ❌ Data consistency issues    │ HIGH   │ High   │          │
│  ❌ Operational overhead       │ MEDIUM │ High   │          │
│  ❌ Initial migration cost     │ HIGH   │ High   │          │
│  ❌ Debugging difficulty       │ MEDIUM │ Medium │          │
│                                                               │
│  VERDICT: PROCEED with caution (65% confidence)              │
│  Start with 2-3 bounded contexts, not full decomposition     │
└──────────────────────────────────────────────────────────────┘
```

---

## Image Examples

| Prompt | Expected Image Type | Description |
|--------|-------------------|-------------|
| Weighted pros/cons | Balance scale diagram | Visual scale with weighted items on each side, tilting toward recommendation |
