# Analogy-Based Explanation Prompts for Gemini Nano Bana

```
╔══════════════════════════════════════════════════════════════╗
║          ANALOGY-BASED EXPLANATION PROMPTS                    ║
╚══════════════════════════════════════════════════════════════╝
```

---

## Prompt 1: Technical Concept via Everyday Analogy

### Prompt
```
Explain how a load balancer works using the analogy of a 
restaurant host seating guests. Cover:
- What the host (load balancer) does
- What the tables (servers) represent
- What happens when all tables are full (server overload)
- How the host decides which table to seat guests at (algorithms)
Make it understandable for someone with zero tech background.
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│  LOAD BALANCER = RESTAURANT HOST                             │
│                                                               │
│  🏠 Restaurant = Your Application                            │
│                                                               │
│        Guests (Requests) arrive at the door                  │
│                     │                                         │
│                     ▼                                         │
│            ┌─────────────────┐                                │
│            │   HOST (Load    │                                │
│            │   Balancer)     │                                │
│            └──┬─────┬─────┬─┘                                │
│               │     │     │                                   │
│               ▼     ▼     ▼                                   │
│           Table1  Table2  Table3                              │
│          (Server) (Server)(Server)                            │
│           2 seats 4 seats 1 seat                             │
│                                                               │
│  HOST STRATEGIES:                                             │
│  Round Robin = Seat at each table in order (1,2,3,1,2,3...) │
│  Least Busy  = Seat at table with most empty chairs          │
│  Weighted    = Big tables get more guests                    │
│                                                               │
│  When ALL tables full?                                        │
│  → Waiting area (request queue)                              │
│  → "Sorry, we're full" (503 error)                           │
│  → Open more tables (auto-scaling!)                          │
└──────────────────────────────────────────────────────────────┘
```

---

## Prompt 2: Complex System via Story

### Prompt
```
Explain how Git version control works using the analogy of 
writing a book with co-authors. Cover: commits (saving chapters),
branches (alternate storylines), merge (combining chapters),
conflicts (two authors editing the same paragraph).
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│  GIT = CO-WRITING A BOOK                                     │
│                                                               │
│  COMMIT = Saving a chapter draft                             │
│  "Chapter 3 - Draft v2" ← snapshot of your work             │
│                                                               │
│  BRANCH = Writing an alternate storyline                     │
│  Main story: Hero goes to mountain                           │
│  Branch:     Hero goes to ocean (experimental)               │
│                                                               │
│  Main ────●────●────●────●──── (original story)             │
│                 \                                             │
│  Branch          ●────●────●── (ocean storyline)             │
│                                                               │
│  MERGE = Combining the best of both                          │
│  Main ────●────●────●────●────●── (combined!)               │
│                 \              /                              │
│  Branch          ●────●────●──                               │
│                                                               │
│  CONFLICT = Two authors edited the same paragraph            │
│  Author A: "The sky was blue"                                │
│  Author B: "The sky was gray"                                │
│  Git says: "Which version do you want to keep?"              │
└──────────────────────────────────────────────────────────────┘
```

---

## Image Examples

| Prompt | Expected Image Type | Description |
|--------|-------------------|-------------|
| Load balancer analogy | Illustrated diagram | Restaurant scene with host directing guests to tables |
| Git analogy | Book/branching visual | Book with branching storylines showing merge points |
