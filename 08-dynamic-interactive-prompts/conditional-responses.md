# Conditional Response Prompts for Gemini Nano Bana

```
╔══════════════════════════════════════════════════════════════╗
║            CONDITIONAL RESPONSE PROMPTS                       ║
╚══════════════════════════════════════════════════════════════╝
```

---

## Prompt 1: Branching Decision Helper

### Prompt
```
I want to choose a database for my project. Ask me these questions
and recommend based on my answers:
- Is your data structured or unstructured?
- Do you need real-time queries or batch processing?
- Expected data volume: small (<1GB), medium (1-100GB), large (100GB+)?
- Budget: free tier preferred or enterprise OK?

For each combination, suggest a specific database with reasoning.
```

### Expected Visual Output
```
  DATABASE DECISION TREE
  ━━━━━━━━━━━━━━━━━━━━━

  Data Type?
  ├── Structured
  │   ├── Real-time + Small → SQLite
  │   ├── Real-time + Medium → PostgreSQL
  │   ├── Real-time + Large → CockroachDB
  │   ├── Batch + Small → SQLite
  │   ├── Batch + Medium → MySQL
  │   └── Batch + Large → BigQuery
  │
  └── Unstructured
      ├── Real-time + Small → MongoDB
      ├── Real-time + Medium → MongoDB Atlas
      ├── Real-time + Large → Cassandra
      ├── Batch + Small → Firebase
      ├── Batch + Medium → DynamoDB
      └── Batch + Large → Apache HBase
```

---

## Prompt 2: Error-Based Response Routing

### Prompt
```
I'm getting an error in my Python code. Based on the error type,
provide a targeted fix:
- If TypeError → check variable types and type casting
- If ImportError → check package installation and paths
- If KeyError → check dictionary keys and .get() usage
- If IndexError → check list bounds and iteration
Give me the fix for: "TypeError: can't multiply sequence by non-int"
```

### Expected Visual Output
```
  ERROR ROUTING
  ━━━━━━━━━━━━━

  Input Error: TypeError: can't multiply sequence by non-int

  Route: TypeError detected → Type Casting Fix

  DIAGNOSIS:
  You're trying to multiply a string by a float.
  Example: "hello" * 2.5  ← This fails

  FIX:
  ┌─────────────────────────────────────────────┐
  │ # Before (broken)                           │
  │ result = user_input * price    # str * float│
  │                                             │
  │ # After (fixed)                             │
  │ result = int(user_input) * price            │
  └─────────────────────────────────────────────┘
```

---

## Image Examples

| Prompt | Expected Image Type | Description |
|--------|-------------------|-------------|
| Decision helper | Decision tree diagram | Color-coded branching tree with database icons at leaf nodes |
| Error routing | Flowchart | Error type detection flowing to specific fix recommendations |
