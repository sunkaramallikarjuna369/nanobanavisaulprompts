# Expert Persona Prompts for Gemini Nano Bana

```
╔══════════════════════════════════════════════════════════════╗
║                 EXPERT PERSONA PROMPTS                       ║
║                                                              ║
║  "Act as a [ROLE] with [YEARS] experience in [DOMAIN]"      ║
║                                                              ║
║  ┌──────────┐    ┌──────────────┐    ┌──────────────────┐   ║
║  │ Assign   │───>│  AI Adopts   │───>│  Expert-Level    │   ║
║  │ Persona  │    │  Expertise   │    │  Response        │   ║
║  └──────────┘    └──────────────┘    └──────────────────┘   ║
╚══════════════════════════════════════════════════════════════╝
```

---

## Prompt 1: Senior Software Architect

### Prompt
```
Act as a Senior Software Architect with 15 years of experience 
designing distributed systems. You specialize in microservices, 
event-driven architecture, and cloud-native design patterns.

Review this architecture decision: We want to build a real-time 
notification system that handles 10M users. Should we use 
WebSockets, Server-Sent Events, or Long Polling?

Provide your expert recommendation with trade-offs.
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│  ARCHITECT'S RECOMMENDATION                                   │
│  ═══════════════════════════                                  │
│                                                               │
│  ┌─────────────┬─────────────┬─────────────┬───────────────┐│
│  │ Criteria    │ WebSockets  │ SSE         │ Long Polling  ││
│  ├─────────────┼─────────────┼─────────────┼───────────────┤│
│  │ Bidirection │ ✅ Yes      │ ❌ No       │ ❌ No         ││
│  │ Scalability │ ⚠️ Complex  │ ✅ Easy     │ ❌ Poor       ││
│  │ Latency     │ ✅ <50ms    │ ✅ <100ms   │ ⚠️ Variable   ││
│  │ Browser     │ ✅ All      │ ✅ Most     │ ✅ All        ││
│  │ Resource    │ ⚠️ High     │ ✅ Low      │ ❌ Very High  ││
│  └─────────────┴─────────────┴─────────────┴───────────────┘│
│                                                               │
│  VERDICT: SSE for notifications (one-way), WebSockets for    │
│  chat features. Avoid Long Polling at 10M scale.             │
└──────────────────────────────────────────────────────────────┘
```

---

## Prompt 2: Data Science Lead

### Prompt
```
Act as a Data Science Lead at a Fortune 500 company. You have 
experience with ML pipeline design, A/B testing frameworks, 
and deploying models at scale.

Our recommendation engine has 78% accuracy but business wants 90%+.
Current approach: collaborative filtering on purchase history.
Data: 5M users, 100K products, 2 years of transaction data.

What's your improvement strategy?
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│  DATA SCIENCE IMPROVEMENT STRATEGY                            │
│                                                               │
│  CURRENT: 78% ████████████████████░░░░░                      │
│  TARGET:  90% ████████████████████████████░░                 │
│  GAP:     12%                                                 │
│                                                               │
│  STRATEGY LAYERS:                                            │
│  ┌──────────────────────────────────────────┐                │
│  │ Layer 1: Hybrid Model (+5%)              │                │
│  │ ├── Add content-based features           │                │
│  │ ├── Combine with collaborative filtering │                │
│  │ └── Ensemble with gradient boosting      │                │
│  ├──────────────────────────────────────────┤                │
│  │ Layer 2: Feature Engineering (+4%)       │                │
│  │ ├── User behavior sequences              │                │
│  │ ├── Seasonal patterns                    │                │
│  │ └── Cross-category preferences           │                │
│  ├──────────────────────────────────────────┤                │
│  │ Layer 3: Real-time Signals (+3%)         │                │
│  │ ├── Session context                      │                │
│  │ ├── Trending items                       │                │
│  │ └── Social signals                       │                │
│  └──────────────────────────────────────────┘                │
│                                                               │
│  PROJECTED: 78% + 5% + 4% + 3% = ~90%                      │
└──────────────────────────────────────────────────────────────┘
```

---

## Prompt 3: Cybersecurity Expert

### Prompt
```
Act as a Chief Information Security Officer (CISO) with expertise 
in application security, threat modeling, and compliance.

We're launching a healthcare AI application that processes patient 
data. What are the top 5 security measures we MUST implement 
before going live? Explain each with severity level.
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│  CISO SECURITY CHECKLIST - HEALTHCARE AI                      │
│                                                               │
│  ┌─ CRITICAL ──────────────────────────────────────────────┐│
│  │ 1. End-to-End Encryption (AES-256 + TLS 1.3)           ││
│  │    Patient data encrypted at rest AND in transit         ││
│  │    SEVERITY: ██████████ CRITICAL                        ││
│  ├─────────────────────────────────────────────────────────┤│
│  │ 2. HIPAA-Compliant Access Controls (RBAC + MFA)        ││
│  │    Role-based access with multi-factor authentication    ││
│  │    SEVERITY: ██████████ CRITICAL                        ││
│  ├─ HIGH ──────────────────────────────────────────────────┤│
│  │ 3. Audit Logging & Monitoring                           ││
│  │    Every data access logged with tamper-proof storage    ││
│  │    SEVERITY: ████████░░ HIGH                            ││
│  ├─────────────────────────────────────────────────────────┤│
│  │ 4. AI Model Input Sanitization                          ││
│  │    Prevent prompt injection and data exfiltration        ││
│  │    SEVERITY: ████████░░ HIGH                            ││
│  ├─ MEDIUM ────────────────────────────────────────────────┤│
│  │ 5. Data Anonymization Pipeline                          ││
│  │    PII stripped before model training/inference          ││
│  │    SEVERITY: ██████░░░░ MEDIUM                          ││
│  └─────────────────────────────────────────────────────────┘│
└──────────────────────────────────────────────────────────────┘
```

---

## Image Examples

| Prompt | Expected Image Type | Description |
|--------|-------------------|-------------|
| Architect review | Comparison matrix | Color-coded table with checkmarks, warnings, X marks per technology |
| Data Science strategy | Layered improvement chart | Stacked bar showing cumulative accuracy gain per strategy layer |
| Security checklist | Risk heatmap | Color-graded severity cards (red=critical, orange=high, yellow=medium) |
