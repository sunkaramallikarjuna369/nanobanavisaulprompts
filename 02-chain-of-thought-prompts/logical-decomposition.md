# Logical Decomposition Prompts for Gemini Nano Bana

```
╔══════════════════════════════════════════════════════════════╗
║              LOGICAL DECOMPOSITION PROMPTS                    ║
║                                                              ║
║  Break complex problems into smaller, solvable pieces!       ║
║                                                              ║
║  ┌──────────────┐     ┌─────┐ ┌─────┐ ┌─────┐             ║
║  │   COMPLEX    │ ──> │ Sub │ │ Sub │ │ Sub │             ║
║  │   PROBLEM    │     │  1  │ │  2  │ │  3  │             ║
║  └──────────────┘     └──┬──┘ └──┬──┘ └──┬──┘             ║
║                          └───────┼───────┘                   ║
║                                  ▼                           ║
║                          ┌──────────────┐                   ║
║                          │   COMPLETE   │                   ║
║                          │   SOLUTION   │                   ║
║                          └──────────────┘                   ║
╚══════════════════════════════════════════════════════════════╝
```

---

## Prompt 1: System Architecture Decomposition

### Prompt
```
Decompose the architecture of a ride-sharing application (like Uber) 
into its core components. For each component:
1. Name and purpose
2. Key functions it performs
3. How it connects to other components
4. Technologies typically used

Break this down layer by layer from user-facing to backend.
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────────┐
│         RIDE-SHARING APP: LOGICAL DECOMPOSITION                  │
│                                                                   │
│  LAYER 1: USER INTERFACE                                         │
│  ┌──────────────────┐  ┌──────────────────┐                     │
│  │  Rider App       │  │  Driver App       │                     │
│  │  - Request ride  │  │  - Accept rides   │                     │
│  │  - Track driver  │  │  - Navigate       │                     │
│  │  - Payment       │  │  - Earnings       │                     │
│  │  [React Native]  │  │  [React Native]   │                     │
│  └────────┬─────────┘  └────────┬──────────┘                    │
│           └────────┬────────────┘                                │
│                    ▼                                              │
│  LAYER 2: API GATEWAY                                            │
│  ┌──────────────────────────────────────────┐                   │
│  │  API Gateway (Kong / AWS API Gateway)     │                   │
│  │  - Authentication  - Rate Limiting        │                   │
│  │  - Load Balancing  - Request Routing      │                   │
│  └────────────────────┬─────────────────────┘                   │
│                       ▼                                          │
│  LAYER 3: MICROSERVICES                                          │
│  ┌──────────┐ ┌──────────┐ ┌──────────┐ ┌──────────┐          │
│  │  User    │ │ Matching │ │ Payment  │ │ Pricing  │          │
│  │ Service  │ │ Service  │ │ Service  │ │ Service  │          │
│  │ [Node.js]│ │ [Python] │ │ [Java]   │ │ [Go]     │          │
│  └────┬─────┘ └────┬─────┘ └────┬─────┘ └────┬─────┘          │
│       └─────────────┼────────────┼─────────────┘               │
│                     ▼            ▼                               │
│  LAYER 4: DATA & MESSAGING                                      │
│  ┌──────────┐ ┌──────────┐ ┌──────────┐ ┌──────────┐          │
│  │PostgreSQL│ │  Redis   │ │  Kafka   │ │ MongoDB  │          │
│  │ (Users)  │ │ (Cache)  │ │(Events)  │ │ (Logs)   │          │
│  └──────────┘ └──────────┘ └──────────┘ └──────────┘          │
│                                                                   │
│  LAYER 5: INFRASTRUCTURE                                         │
│  ┌──────────────────────────────────────────┐                   │
│  │  AWS / GCP / Azure                        │                   │
│  │  [Kubernetes] [Docker] [Terraform]        │                   │
│  └──────────────────────────────────────────┘                   │
└──────────────────────────────────────────────────────────────────┘
```

---

## Prompt 2: Learning Path Decomposition

### Prompt
```
Decompose "Becoming a Full-Stack Developer" into a logical learning path.
Break it into phases, each phase into topics, each topic into skills.
Show the dependencies between topics.
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────────┐
│       FULL-STACK DEVELOPER LEARNING PATH                         │
│                                                                   │
│  PHASE 1: FOUNDATIONS (Months 1-2)                               │
│  ┌────────┐  ┌────────┐  ┌────────┐                            │
│  │  HTML  │─>│  CSS   │─>│   JS   │                            │
│  │ Basics │  │ Basics │  │ Basics │                            │
│  └────┬───┘  └────┬───┘  └────┬───┘                            │
│       └───────────┼───────────┘                                  │
│                   ▼                                               │
│  PHASE 2: FRONTEND (Months 3-4)                                  │
│  ┌────────┐  ┌────────┐  ┌────────┐                            │
│  │ React  │─>│ State  │─>│  API   │                            │
│  │  /Vue  │  │ Mgmt   │  │ Calls  │                            │
│  └────┬───┘  └────┬───┘  └────┬───┘                            │
│       └───────────┼───────────┘                                  │
│                   ▼                                               │
│  PHASE 3: BACKEND (Months 5-6)                                   │
│  ┌────────┐  ┌────────┐  ┌────────┐                            │
│  │Node.js │─>│Database│─>│  REST  │                            │
│  │/Python │  │ SQL/No │  │  APIs  │                            │
│  └────┬───┘  └────┬───┘  └────┬───┘                            │
│       └───────────┼───────────┘                                  │
│                   ▼                                               │
│  PHASE 4: DEVOPS & DEPLOY (Month 7)                              │
│  ┌────────┐  ┌────────┐  ┌────────┐                            │
│  │  Git   │─>│ Docker │─>│ Cloud  │                            │
│  │ CI/CD  │  │  K8s   │  │ Deploy │                            │
│  └────────┘  └────────┘  └────────┘                            │
│                                                                   │
│  TOTAL TIME: ~7 months dedicated study                           │
└──────────────────────────────────────────────────────────────────┘
```

---

## Image Examples

| Prompt | Expected Image Type | Description |
|--------|-------------------|-------------|
| System decomposition | Layered architecture diagram | Color-coded horizontal layers with component boxes and connecting arrows |
| Learning path | Roadmap infographic | Timeline-style path with milestones, skill nodes, and dependency arrows |
| Process breakdown | Hierarchical tree | Top-down decomposition with parent-child relationships |
