# Tiered Summary Prompts for Gemini Nano Bana

```
╔══════════════════════════════════════════════════════════════╗
║              TIERED SUMMARY PROMPTS                           ║
╚══════════════════════════════════════════════════════════════╝
```

---

## Prompt 1: Multi-Level Summary

### Prompt
```
Summarize the following content at 3 levels:

LEVEL 1 - Tweet (max 280 characters):
A single sentence capturing the core message.

LEVEL 2 - Elevator Pitch (50-75 words):
A paragraph for someone with 30 seconds.

LEVEL 3 - Executive Summary (200-300 words):
Detailed summary with key findings, implications, and next steps.

Content: [paste article/document here]
Topic: Kubernetes adoption in enterprise environments
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│  TIERED SUMMARY: Kubernetes Enterprise Adoption              │
│                                                               │
│  ┌─ LEVEL 1: Tweet ─────────────────────────────────────┐   │
│  │ 78% of enterprises now run Kubernetes in production,  │   │
│  │ but 60% struggle with security and cost management.   │   │
│  │ Multi-cloud is the new default.                       │   │
│  │                                              [240 ch] │   │
│  └───────────────────────────────────────────────────────┘   │
│                                                               │
│  ┌─ LEVEL 2: Elevator Pitch ────────────────────────────┐   │
│  │ Kubernetes has become the standard container          │   │
│  │ orchestration platform, with 78% of Fortune 500      │   │
│  │ companies running production workloads. However,      │   │
│  │ organizations face challenges in security posture     │   │
│  │ management, cost optimization, and talent             │   │
│  │ acquisition. Multi-cloud strategies are driving       │   │
│  │ adoption of managed K8s services like EKS and GKE.   │   │
│  │                                            [62 words] │   │
│  └───────────────────────────────────────────────────────┘   │
│                                                               │
│  ┌─ LEVEL 3: Executive Summary ─────────────────────────┐   │
│  │ KEY FINDINGS:                                         │   │
│  │ - 78% enterprise adoption rate (up from 58% in 2023) │   │
│  │ - Average cluster size: 12 nodes                      │   │
│  │ - 60% report security as top concern                  │   │
│  │                                                       │   │
│  │ IMPLICATIONS:                                         │   │
│  │ - Platform engineering teams are essential             │   │
│  │ - GitOps practices reduce deployment failures 40%     │   │
│  │                                                       │   │
│  │ NEXT STEPS:                                           │   │
│  │ 1. Implement policy-as-code (OPA/Gatekeeper)         │   │
│  │ 2. Adopt FinOps practices for cost visibility         │   │
│  │ 3. Invest in internal developer platforms             │   │
│  │                                           [245 words] │   │
│  └───────────────────────────────────────────────────────┘   │
└──────────────────────────────────────────────────────────────┘
```

---

## Image Examples

| Prompt | Expected Image Type | Description |
|--------|-------------------|-------------|
| Tiered summary | Nested card layout | Three expanding cards showing increasing detail levels with word counts |
