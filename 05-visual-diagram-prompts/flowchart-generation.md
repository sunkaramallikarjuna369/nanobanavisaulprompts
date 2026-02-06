# Flowchart Generation Prompts for Gemini Nano Bana

```
╔══════════════════════════════════════════════════════════════╗
║              FLOWCHART GENERATION PROMPTS                     ║
║                                                              ║
║  Transform processes into visual flowcharts!                 ║
╚══════════════════════════════════════════════════════════════╝
```

---

## Prompt 1: Decision Flowchart

### Prompt
```
Create a flowchart for debugging a web application that's returning 
a 500 Internal Server Error. Include decision diamonds for: 
checking logs, database connectivity, API dependencies, memory 
usage, and recent deployments. Use standard flowchart symbols.
```

### Expected Visual Output
```
                    ┌─────────────────┐
                    │  500 Error      │
                    │  Detected       │
                    └────────┬────────┘
                             ▼
                    ┌─────────────────┐
                    │ Check Server    │
                    │ Logs            │
                    └────────┬────────┘
                             ▼
                  ┌──────────────────────┐
                 ╱  Error message found?  ╲
                ╱                          ╲
               ▼ YES                    NO ▼
    ┌────────────────┐          ┌────────────────┐
    │ Fix the        │          │ Check DB       │
    │ specific error │          │ Connection     │
    └────────────────┘          └───────┬────────┘
                                        ▼
                              ┌──────────────────┐
                             ╱  DB responding?    ╲
                            ╱                      ╲
                           ▼ YES                NO ▼
                ┌──────────────┐       ┌──────────────┐
                │ Check API    │       │ Restart DB   │
                │ Dependencies │       │ Service      │
                └──────┬───────┘       └──────────────┘
                       ▼
             ┌──────────────────┐
            ╱  APIs healthy?     ╲
           ╱                      ╲
          ▼ YES                NO ▼
  ┌──────────────┐     ┌──────────────────┐
  │ Check Memory │     │ Contact API      │
  │ & CPU Usage  │     │ Provider         │
  └──────┬───────┘     └──────────────────┘
         ▼
  ┌──────────────┐
  │ Check Recent │
  │ Deployments  │──→ Rollback if needed
  └──────────────┘
```

---

## Prompt 2: User Registration Flow

### Prompt
```
Generate a flowchart for a user registration process with email 
verification. Include: form validation, duplicate check, email 
sending, verification link click, and account activation. Show 
error paths for each step.
```

### Expected Visual Output
```
  ┌──────────┐     ┌──────────────┐     ┌──────────────────┐
  │  START   │────>│ Fill Form    │────>│ Validate Fields  │
  └──────────┘     └──────────────┘     └────────┬─────────┘
                                                  ▼
                                        ┌──────────────────┐
                                       ╱  All valid?        ╲
                                      ╱                      ╲
                                  YES ▼                   NO ▼
                          ┌──────────────┐       ┌──────────────┐
                          │ Check if     │       │ Show Error   │
                          │ email exists │       │ Messages     │──┐
                          └──────┬───────┘       └──────────────┘  │
                                 ▼                                  │
                       ┌──────────────────┐                        │
                      ╱  Already exists?   ╲               ┌───────┘
                     ╱                      ╲              ▼
                  NO ▼                   YES ▼      Back to Form
          ┌──────────────┐       ┌──────────────┐
          │ Create User  │       │ Show "Email  │
          │ (inactive)   │       │ taken" error │
          └──────┬───────┘       └──────────────┘
                 ▼
          ┌──────────────┐     ┌──────────────────┐
          │ Send Verify  │────>│ User Clicks      │
          │ Email        │     │ Verify Link       │
          └──────────────┘     └────────┬──────────┘
                                        ▼
                               ┌──────────────────┐
                              ╱  Token valid?       ╲
                             ╱                       ╲
                          YES ▼                   NO ▼
                  ┌──────────────┐       ┌──────────────┐
                  │ Activate     │       │ "Link        │
                  │ Account ✅   │       │  expired"    │
                  └──────────────┘       └──────────────┘
```

---

## Prompt 3: Mermaid Flowchart Generation

### Prompt
```
Generate a Mermaid.js flowchart for a CI/CD pipeline that includes:
build, test, security scan, staging deploy, integration tests,
approval gate, and production deploy. Use Mermaid syntax.
```

### Expected Visual Output
```
  Mermaid Code Output:
  ┌─────────────────────────────────────────────────┐
  │ ```mermaid                                       │
  │ graph TD                                         │
  │     A[Push Code] --> B[Build]                    │
  │     B --> C[Unit Tests]                          │
  │     C --> D{Tests Pass?}                         │
  │     D -->|Yes| E[Security Scan]                  │
  │     D -->|No| F[Fix & Retry]                     │
  │     F --> A                                       │
  │     E --> G{Vulnerabilities?}                    │
  │     G -->|No| H[Deploy Staging]                  │
  │     G -->|Yes| I[Fix Security]                   │
  │     I --> A                                       │
  │     H --> J[Integration Tests]                   │
  │     J --> K{All Pass?}                           │
  │     K -->|Yes| L[Request Approval]               │
  │     K -->|No| F                                   │
  │     L --> M{Approved?}                           │
  │     M -->|Yes| N[Deploy Production]              │
  │     M -->|No| O[Review Changes]                  │
  │     N --> P[Monitor & Alert]                     │
  │ ```                                               │
  └─────────────────────────────────────────────────┘
```

---

## Image Examples

| Prompt | Expected Image Type | Description |
|--------|-------------------|-------------|
| Debug flowchart | Decision tree | Diamond-shaped decisions with branching YES/NO paths, color-coded severity |
| Registration flow | Process diagram | Sequential boxes with error paths shown in red, success in green |
| Mermaid CI/CD | Rendered flowchart | Auto-generated from Mermaid syntax with styled nodes and edges |
