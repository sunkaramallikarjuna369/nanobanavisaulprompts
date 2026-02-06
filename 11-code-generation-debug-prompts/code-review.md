# Code Review Prompts for Gemini Nano Bana

```
╔══════════════════════════════════════════════════════════════╗
║                CODE REVIEW PROMPTS                            ║
╚══════════════════════════════════════════════════════════════╝
```

---

## Prompt 1: Security-Focused Review

### Prompt
```
Review this Python Flask code for security vulnerabilities:

@app.route('/search')
def search():
    query = request.args.get('q')
    results = db.execute(f"SELECT * FROM products WHERE name LIKE '%{query}%'")
    return render_template_string(f"<h1>Results for {query}</h1>")

List each vulnerability, severity (Critical/High/Medium/Low),
and the fixed code.
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│  SECURITY REVIEW REPORT                                       │
│                                                               │
│  Vulnerability 1: SQL Injection          Severity: CRITICAL  │
│  ─────────────────────────────────────────────────────────   │
│  Line: db.execute(f"SELECT * FROM products...")              │
│  Risk: Attacker can read/modify/delete entire database       │
│  Fix:  db.execute("SELECT * FROM products WHERE             │
│         name LIKE ?", (f"%{query}%",))                       │
│                                                               │
│  Vulnerability 2: XSS (Cross-Site Scripting)  Severity: HIGH│
│  ─────────────────────────────────────────────────────────   │
│  Line: render_template_string(f"<h1>Results for {query}")    │
│  Risk: Attacker injects malicious JavaScript                 │
│  Fix:  render_template("search.html", query=query)           │
│                                                               │
│  Vulnerability 3: No Input Validation    Severity: MEDIUM    │
│  ─────────────────────────────────────────────────────────   │
│  Line: query = request.args.get('q')                         │
│  Risk: No length limit, no sanitization                      │
│  Fix:  query = request.args.get('q', '')[:100].strip()       │
│                                                               │
│  SCORE: 2/10 ← Needs immediate fixes before deployment      │
└──────────────────────────────────────────────────────────────┘
```

---

## Prompt 2: Performance Review

### Prompt
```
Review this code for performance issues and suggest optimizations:

def find_duplicates(items):
    duplicates = []
    for i in range(len(items)):
        for j in range(len(items)):
            if i != j and items[i] == items[j]:
                if items[i] not in duplicates:
                    duplicates.append(items[i])
    return duplicates
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│  PERFORMANCE REVIEW                                           │
│                                                               │
│  Current Complexity: O(n³) ← Very slow!                     │
│  (nested loop O(n²) × linear search in duplicates O(n))     │
│                                                               │
│  Issue 1: Nested loops → O(n²) comparisons                  │
│  Issue 2: `not in duplicates` → O(n) linear search          │
│  Issue 3: Checking items[i]==items[j] both directions        │
│                                                               │
│  OPTIMIZED VERSION: O(n) ← 1000x faster for large lists     │
│  ┌──────────────────────────────────────────────┐            │
│  │ from collections import Counter              │            │
│  │                                              │            │
│  │ def find_duplicates(items):                  │            │
│  │     counts = Counter(items)                  │            │
│  │     return [x for x, c in counts.items()     │            │
│  │             if c > 1]                        │            │
│  └──────────────────────────────────────────────┘            │
│                                                               │
│  Benchmark (10,000 items):                                   │
│  Original:  45.2 seconds                                     │
│  Optimized:  0.003 seconds                                   │
└──────────────────────────────────────────────────────────────┘
```

---

## Image Examples

| Prompt | Expected Image Type | Description |
|--------|-------------------|-------------|
| Security review | Severity dashboard | Color-coded cards (red=critical, orange=high) with vulnerability details |
| Performance review | Before/after benchmark | Side-by-side with O(n³) vs O(n) complexity graph |
