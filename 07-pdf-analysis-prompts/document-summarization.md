# Document Summarization Prompts for Gemini Nano Bana

```
╔══════════════════════════════════════════════════════════════╗
║            DOCUMENT SUMMARIZATION PROMPTS                     ║
╚══════════════════════════════════════════════════════════════╝
```

---

## Prompt 1: Executive Summary

### Prompt
```
Read this 50-page technical report and create an executive summary:
- 3-sentence overview
- 5 key takeaways (bullet points)
- Recommended actions (numbered list)
- Risk factors mentioned
Keep the summary under 300 words. Target audience: C-level executives.
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│  EXECUTIVE SUMMARY                                            │
│  ━━━━━━━━━━━━━━━━━                                           │
│                                                               │
│  OVERVIEW:                                                    │
│  This report analyzes the company's cloud migration           │
│  strategy over Q3-Q4 2025. Total infrastructure cost          │
│  reduced by 34%. Three critical vulnerabilities were          │
│  identified and remediated.                                   │
│                                                               │
│  KEY TAKEAWAYS:                                               │
│  • Cloud costs decreased from $2.1M to $1.4M/quarter        │
│  • 99.97% uptime achieved (target: 99.95%)                   │
│  • 3 security incidents resolved within SLA                  │
│  • Team velocity improved 28% post-migration                 │
│  • Customer latency reduced by 45ms average                  │
│                                                               │
│  RECOMMENDED ACTIONS:                                         │
│  1. Approve Phase 2 migration budget ($500K)                 │
│  2. Hire 2 additional SRE engineers                          │
│  3. Implement automated cost alerting                        │
│                                                               │
│  RISK FACTORS:                                                │
│  ⚠ Vendor lock-in risk: MEDIUM                               │
│  ⚠ Skills gap in team: LOW (training planned)                │
│  ⚠ Compliance audit pending: HIGH priority                   │
└──────────────────────────────────────────────────────────────┘
```

---

## Prompt 2: Multi-Level Summary

### Prompt
```
Summarize this research paper at three levels of detail:
1. Tweet-length (280 chars) - for social media sharing
2. Abstract-length (150 words) - for quick reference
3. Detailed summary (500 words) - for team review
Include key statistics and findings at each level.
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│  MULTI-LEVEL SUMMARY                                         │
│                                                               │
│  ┌─ LEVEL 1: Tweet (280 chars) ────────────────────────┐    │
│  │ New study: Transformer models achieve 95% accuracy   │    │
│  │ on medical diagnosis tasks, outperforming CNN-based  │    │
│  │ approaches by 12%. Open-source code available.       │    │
│  │ #AI #Healthcare #MachineLearning                     │    │
│  └──────────────────────────────────────────────────────┘    │
│                         ▼                                     │
│  ┌─ LEVEL 2: Abstract (150 words) ─────────────────────┐    │
│  │ This paper presents a novel transformer-based         │    │
│  │ architecture for medical image diagnosis. Evaluated   │    │
│  │ on 50,000 chest X-rays from 3 hospitals, achieving   │    │
│  │ 95.2% accuracy vs 83.1% for baseline CNN models...   │    │
│  └──────────────────────────────────────────────────────┘    │
│                         ▼                                     │
│  ┌─ LEVEL 3: Detailed (500 words) ─────────────────────┐    │
│  │ Introduction: Medical imaging diagnosis remains...    │    │
│  │ Methods: We employed a Vision Transformer (ViT)...    │    │
│  │ Results: Across all test sets, our model achieved...  │    │
│  │ Discussion: The attention mechanism allows...         │    │
│  │ Limitations: Dataset bias toward specific...          │    │
│  └──────────────────────────────────────────────────────┘    │
└──────────────────────────────────────────────────────────────┘
```

---

## Image Examples

| Prompt | Expected Image Type | Description |
|--------|-------------------|-------------|
| Executive summary | Dashboard card | Clean summary card with color-coded sections and risk indicators |
| Multi-level summary | Expanding accordion | Three nested levels expanding from brief to detailed |
