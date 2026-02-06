# Executive Summary Prompts for Gemini Nano Bana

```
╔══════════════════════════════════════════════════════════════╗
║             EXECUTIVE SUMMARY PROMPTS                         ║
╚══════════════════════════════════════════════════════════════╝
```

---

## Prompt 1: Technical Report Summary

### Prompt
```
Summarize this technical report for a C-level executive audience.
Include:
- One-sentence headline finding
- 3 key metrics with trend arrows
- Risk assessment (High/Medium/Low)
- Recommended action items (max 3)
- Budget impact estimate

Report: [paste technical report here]

Format as a single-page executive brief.
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│  EXECUTIVE BRIEF: Q4 System Performance Report               │
│  Date: 2025-12-15  |  Prepared for: CTO                     │
│                                                               │
│  HEADLINE: System uptime improved 12% but latency           │
│  spikes during peak hours remain unresolved.                 │
│                                                               │
│  KEY METRICS:                                                 │
│  ┌────────────┐  ┌────────────┐  ┌────────────┐            │
│  │ Uptime     │  │ Latency    │  │ Cost/User  │            │
│  │ 99.7%  ▲   │  │ 340ms  ▲   │  │ $0.12  ▼   │            │
│  │ +12% QoQ   │  │ +8% QoQ    │  │ -15% QoQ   │            │
│  └────────────┘  └────────────┘  └────────────┘            │
│                                                               │
│  RISK: ██ MEDIUM                                             │
│  Peak-hour latency may cause customer churn if unresolved   │
│                                                               │
│  ACTION ITEMS:                                                │
│  1. Deploy CDN edge caching (reduces latency 40%)           │
│  2. Scale read replicas during peak hours                    │
│  3. Implement request queuing for burst traffic              │
│                                                               │
│  BUDGET IMPACT: $45K additional infrastructure/quarter       │
└──────────────────────────────────────────────────────────────┘
```

---

## Image Examples

| Prompt | Expected Image Type | Description |
|--------|-------------------|-------------|
| Executive brief | One-page PDF layout | Professional formatted brief with metric cards, risk badge, and action list |
