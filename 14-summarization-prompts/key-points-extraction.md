# Key Points Extraction Prompts for Gemini Nano Bana

```
╔══════════════════════════════════════════════════════════════╗
║           KEY POINTS EXTRACTION PROMPTS                       ║
╚══════════════════════════════════════════════════════════════╝
```

---

## Prompt 1: Prioritized Key Points

### Prompt
```
Extract the top 5 key points from this article/document.
For each key point:
- Rank by importance (1=most critical)
- Provide a one-line summary
- Rate confidence level (High/Medium/Low)
- Tag the category (Technical/Business/Strategic)
- Note any dependencies between points

Document: [paste content here]
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│  KEY POINTS EXTRACTION                                        │
│                                                               │
│  #1 [CRITICAL] [Technical] [Confidence: HIGH]                │
│  ├─ Database migration must complete before API v2 launch    │
│  └─ Dependencies: None (start first)                         │
│                                                               │
│  #2 [HIGH] [Business] [Confidence: HIGH]                     │
│  ├─ Customer churn increased 15% due to latency issues       │
│  └─ Dependencies: Related to #1 (DB performance)             │
│                                                               │
│  #3 [HIGH] [Strategic] [Confidence: MEDIUM]                  │
│  ├─ Competitor launched similar feature 2 months ahead       │
│  └─ Dependencies: Accelerate #4 timeline                     │
│                                                               │
│  #4 [MEDIUM] [Technical] [Confidence: HIGH]                  │
│  ├─ New caching layer reduces response time by 60%           │
│  └─ Dependencies: Requires #1 completion                     │
│                                                               │
│  #5 [LOW] [Business] [Confidence: LOW]                       │
│  ├─ Partnership opportunity with cloud provider              │
│  └─ Dependencies: Independent                                │
│                                                               │
│  DEPENDENCY MAP:                                              │
│  #1 ──→ #2 (resolves)                                        │
│  #1 ──→ #4 (enables)                                         │
│  #3 ──→ #4 (accelerates)                                     │
│  #5    (independent)                                          │
└──────────────────────────────────────────────────────────────┘
```

---

## Image Examples

| Prompt | Expected Image Type | Description |
|--------|-------------------|-------------|
| Key points | Priority matrix | Numbered cards with color-coded importance levels and dependency arrows |
