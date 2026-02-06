# Technology Comparison Prompts for Gemini Nano Bana

```
╔══════════════════════════════════════════════════════════════╗
║            TECHNOLOGY COMPARISON PROMPTS                      ║
╚══════════════════════════════════════════════════════════════╝
```

---

## Prompt 1: Framework Comparison

### Prompt
```
Compare React, Vue, and Angular for building a large-scale 
enterprise dashboard. Evaluate on these criteria:
- Learning curve (1-5 scale)
- Performance (bundle size, rendering speed)
- Ecosystem & community support
- Enterprise features (TypeScript, testing, state management)
- Hiring availability
Present as a comparison table with a final recommendation.
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│  FRAMEWORK COMPARISON: Enterprise Dashboard                  │
│                                                               │
│  ┌─────────────────┬─────────┬─────────┬──────────┐        │
│  │ Criteria        │ React   │ Vue     │ Angular  │        │
│  ├─────────────────┼─────────┼─────────┼──────────┤        │
│  │ Learning Curve  │ ★★★☆☆  │ ★★☆☆☆  │ ★★★★☆   │        │
│  │ Performance     │ ★★★★☆  │ ★★★★★  │ ★★★☆☆   │        │
│  │ Ecosystem       │ ★★★★★  │ ★★★★☆  │ ★★★★☆   │        │
│  │ Enterprise      │ ★★★★☆  │ ★★★☆☆  │ ★★★★★   │        │
│  │ Hiring Pool     │ ★★★★★  │ ★★★☆☆  │ ★★★★☆   │        │
│  ├─────────────────┼─────────┼─────────┼──────────┤        │
│  │ TOTAL           │ 21/25   │ 19/25   │ 20/25   │        │
│  └─────────────────┴─────────┴─────────┴──────────┘        │
│                                                               │
│  RECOMMENDATION: React for flexibility + hiring pool         │
│  Angular if you need opinionated enterprise structure        │
└──────────────────────────────────────────────────────────────┘
```

---

## Prompt 2: Database Technology Comparison

### Prompt
```
Compare PostgreSQL vs MongoDB vs Redis for a real-time analytics 
platform that processes 10,000 events/second. Include:
- Data model suitability
- Query performance for aggregations
- Scalability approach
- Cost at scale
- Use case fit rating (1-10)
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│  DATABASE COMPARISON: Real-Time Analytics                    │
│                                                               │
│  PostgreSQL          MongoDB            Redis                │
│  ┌──────────┐       ┌──────────┐       ┌──────────┐        │
│  │ Relational│       │ Document │       │ Key-Value│        │
│  │ ACID      │       │ Flexible │       │ In-Memory│        │
│  │ SQL       │       │ JSON     │       │ Sub-ms   │        │
│  └──────────┘       └──────────┘       └──────────┘        │
│                                                               │
│  Aggregation:  ★★★★☆     ★★★★☆          ★★☆☆☆             │
│  10K evt/sec:  ★★★☆☆     ★★★★☆          ★★★★★             │
│  Scale:        Vertical   Horizontal     Cluster             │
│  Cost/month:   $200       $350           $150                │
│  Fit Score:    7/10       8/10           6/10                │
│                                                               │
│  VERDICT: MongoDB for flexible schema + good aggregation    │
│  Use Redis as a caching layer in front of MongoDB            │
└──────────────────────────────────────────────────────────────┘
```

---

## Image Examples

| Prompt | Expected Image Type | Description |
|--------|-------------------|-------------|
| Framework comparison | Radar/spider chart | Overlapping colored polygons showing strengths per framework |
| Database comparison | Column comparison cards | Three side-by-side cards with metrics and star ratings |
