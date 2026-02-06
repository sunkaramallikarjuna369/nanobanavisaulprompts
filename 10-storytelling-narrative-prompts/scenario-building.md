# Scenario Building Prompts for Gemini Nano Bana

```
╔══════════════════════════════════════════════════════════════╗
║              SCENARIO BUILDING PROMPTS                        ║
╚══════════════════════════════════════════════════════════════╝
```

---

## Prompt 1: Real-World Problem Scenario

### Prompt
```
Create a realistic scenario: A startup's e-commerce site crashes
on Black Friday. Walk through the incident as a story:
- Setup: What the system looked like before
- Trigger: What caused the crash
- Escalation: How problems cascaded
- Resolution: Step-by-step recovery
- Lessons: What they changed afterward
Include timestamps and character roles (CTO, SRE, Developer).
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│  INCIDENT SCENARIO: Black Friday Crash                       │
│                                                               │
│  09:00 ─── Setup                                             │
│  │  System: 3 servers, single database, no auto-scaling     │
│  │  Traffic: Normal 1K requests/min                          │
│  │                                                            │
│  10:30 ─── Trigger                                           │
│  │  Traffic spikes to 50K req/min (flash sale starts)        │
│  │  CTO: "Why are pages loading in 12 seconds?"             │
│  │                                                            │
│  10:45 ─── Escalation                                        │
│  │  Database connections maxed (100/100)                      │
│  │  Server 2 runs out of memory → crashes                    │
│  │  SRE: "We've lost server 2, DB is at 100% CPU"           │
│  │                                                            │
│  11:00 ─── Resolution                                        │
│  │  Developer: Adds read replicas for DB                     │
│  │  SRE: Spins up 5 emergency servers                        │
│  │  CTO: Enables CDN for static assets                       │
│  │                                                            │
│  11:30 ─── Recovery                                          │
│  │  All systems stable. Revenue loss: $45K                   │
│  │                                                            │
│  POST-MORTEM LESSONS:                                         │
│  1. Implement auto-scaling BEFORE peak events                │
│  2. Load test at 10x expected traffic                        │
│  3. Set up alerting at 70% capacity                          │
└──────────────────────────────────────────────────────────────┘
```

---

## Image Examples

| Prompt | Expected Image Type | Description |
|--------|-------------------|-------------|
| Incident scenario | Timeline infographic | Vertical timeline with color-coded severity stages and character avatars |
