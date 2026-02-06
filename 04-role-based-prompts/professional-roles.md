# Professional Role Prompts for Gemini Nano Bana

```
╔══════════════════════════════════════════════════════════════╗
║               PROFESSIONAL ROLE PROMPTS                      ║
║                                                              ║
║  Assign business/industry roles for specialized outputs!     ║
╚══════════════════════════════════════════════════════════════╝
```

---

## Prompt 1: Product Manager

### Prompt
```
Act as a Senior Product Manager at a SaaS company. Write a PRD 
(Product Requirements Document) for a new AI-powered search 
feature. Include: Problem statement, User stories, Success 
metrics, MVP scope, and Timeline estimate.
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│  PRD: AI-POWERED SEARCH FEATURE                              │
│  ┌────────────────────────────────────────────────────────┐  │
│  │ PROBLEM: Users abandon search after 2 failed queries   │  │
│  │ IMPACT: 35% drop-off rate on search page              │  │
│  ├────────────────────────────────────────────────────────┤  │
│  │ USER STORIES:                                          │  │
│  │ • As a user, I want natural language search            │  │
│  │ • As a user, I want typo-tolerant results              │  │
│  │ • As an admin, I want search analytics dashboard       │  │
│  ├────────────────────────────────────────────────────────┤  │
│  │ SUCCESS METRICS:                                       │  │
│  │ Search success rate: 60% → 85%  ████████████████████   │  │
│  │ Avg queries/session: 4.2 → 1.8  ████████░░░░░░░░░░   │  │
│  │ Time to result: 8s → 2s          ██░░░░░░░░░░░░░░░░   │  │
│  ├────────────────────────────────────────────────────────┤  │
│  │ MVP SCOPE: Semantic search + autocomplete (6 weeks)    │  │
│  │ PHASE 2: Personalization + filters (4 weeks)           │  │
│  │ PHASE 3: Analytics dashboard (3 weeks)                 │  │
│  └────────────────────────────────────────────────────────┘  │
└──────────────────────────────────────────────────────────────┘
```

---

## Prompt 2: Technical Writer

### Prompt
```
Act as a Technical Writer specializing in developer documentation.
Write API documentation for a user authentication endpoint.
Include: endpoint URL, method, headers, request body, response 
codes, and a curl example. Format it like Stripe's API docs.
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│  POST /api/v1/auth/login                                     │
│  ━━━━━━━━━━━━━━━━━━━━━━                                     │
│  Authenticates a user and returns a JWT token.               │
│                                                               │
│  HEADERS:                                                     │
│  ┌────────────────────┬──────────────────────────┐           │
│  │ Content-Type       │ application/json          │           │
│  │ X-API-Key          │ your_api_key_here         │           │
│  └────────────────────┴──────────────────────────┘           │
│                                                               │
│  REQUEST BODY:                                                │
│  {                                                            │
│    "email": "user@example.com",                              │
│    "password": "securepass123"                                │
│  }                                                            │
│                                                               │
│  RESPONSES:                                                   │
│  ┌───────┬─────────────────────────────────────┐             │
│  │ 200   │ { "token": "eyJhbG...", "exp": ..} │             │
│  │ 401   │ { "error": "Invalid credentials" }  │             │
│  │ 429   │ { "error": "Rate limit exceeded" }   │             │
│  └───────┴─────────────────────────────────────┘             │
└──────────────────────────────────────────────────────────────┘
```

---

## Image Examples

| Prompt | Expected Image Type | Description |
|--------|-------------------|-------------|
| Product Manager PRD | Kanban board layout | Columns for problem, stories, metrics with colored cards |
| Technical Writer API | Dark-themed API doc | Syntax-highlighted JSON with tabbed request/response panels |
| Business Analyst | Dashboard mockup | KPI cards with trend arrows and comparison charts |
