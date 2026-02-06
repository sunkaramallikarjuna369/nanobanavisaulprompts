# Debugging Prompts for Gemini Nano Bana

```
╔══════════════════════════════════════════════════════════════╗
║                DEBUGGING PROMPTS                              ║
╚══════════════════════════════════════════════════════════════╝
```

---

## Prompt 1: Systematic Bug Analysis

### Prompt
```
I have a bug in my Python web app. When users submit a form with 
special characters (like &, <, >), the data gets corrupted in the
database. Help me debug this systematically:
1. Identify likely causes
2. Show me diagnostic steps
3. Provide the fix
4. Suggest prevention measures
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│  BUG ANALYSIS: Special Character Corruption                  │
│                                                               │
│  1. LIKELY CAUSES                                            │
│  ┌─────────────────────────────────────────┐                 │
│  │ ❌ Missing input sanitization           │ ← Most likely  │
│  │ ❌ HTML encoding before DB insert       │                 │
│  │ ❌ Database charset not UTF-8           │                 │
│  │ ❌ ORM escaping special chars           │                 │
│  └─────────────────────────────────────────┘                 │
│                                                               │
│  2. DIAGNOSTIC STEPS                                         │
│  Step A: Print raw input before DB insert                    │
│  Step B: Check DB column encoding (SHOW CREATE TABLE)        │
│  Step C: Check if ORM has auto-escape enabled                │
│                                                               │
│  3. FIX                                                       │
│  Before:  db.insert(request.form['name'])                    │
│  After:   db.insert(html.unescape(request.form['name']))     │
│  + Set:   charset=utf8mb4 in DB connection                   │
│                                                               │
│  4. PREVENTION                                                │
│  ✅ Use parameterized queries (prevents SQL injection too)   │
│  ✅ Set DB charset to utf8mb4                                │
│  ✅ Add input validation middleware                          │
│  ✅ Add unit tests with special character inputs             │
└──────────────────────────────────────────────────────────────┘
```

---

## Prompt 2: Error Message Decoding

### Prompt
```
Explain this error and fix it:
"FATAL: too many connections for role 'myapp_user'"
Context: PostgreSQL database, Python app using SQLAlchemy,
running on 4 worker processes with gunicorn.
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│  ERROR DECODED                                                │
│                                                               │
│  Error: FATAL: too many connections for role 'myapp_user'    │
│                                                               │
│  WHAT IT MEANS:                                               │
│  Your app opened more DB connections than PostgreSQL allows   │
│  for this user.                                               │
│                                                               │
│  WHY IT HAPPENS:                                              │
│  4 gunicorn workers × 10 SQLAlchemy pool = 40 connections    │
│  PostgreSQL limit for myapp_user = 20 connections            │
│                                                               │
│  Demand (40) > Limit (20) = 💥 CRASH                        │
│                                                               │
│  FIXES (pick one):                                            │
│  ┌──────────────────────────────────────────────┐            │
│  │ Option A: Reduce pool size                    │            │
│  │ engine = create_engine(url, pool_size=3,      │            │
│  │                         max_overflow=2)       │            │
│  │ 4 workers × 5 = 20 connections ✅             │            │
│  ├──────────────────────────────────────────────┤            │
│  │ Option B: Increase PostgreSQL limit           │            │
│  │ ALTER ROLE myapp_user CONNECTION LIMIT 50;    │            │
│  ├──────────────────────────────────────────────┤            │
│  │ Option C: Use PgBouncer connection pooler     │            │
│  │ App → PgBouncer (pool) → PostgreSQL           │            │
│  │ Best for production! ← RECOMMENDED            │            │
│  └──────────────────────────────────────────────┘            │
└──────────────────────────────────────────────────────────────┘
```

---

## Image Examples

| Prompt | Expected Image Type | Description |
|--------|-------------------|-------------|
| Bug analysis | Diagnostic flowchart | Decision tree flowing from symptom to root cause to fix |
| Error decoding | Architecture diagram | Connection flow showing bottleneck with red warning indicators |
