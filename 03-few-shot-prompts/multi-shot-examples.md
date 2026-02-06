# Multi-Shot Example Prompts for Gemini Nano Bana

```
╔══════════════════════════════════════════════════════════════╗
║               MULTI-SHOT EXAMPLE PROMPTS                     ║
║                                                              ║
║  Show MULTIPLE examples to teach complex patterns!           ║
║                                                              ║
║  Ex 1 ──┐                                                   ║
║  Ex 2 ──┼──> Strong pattern recognition ──> Better output   ║
║  Ex 3 ──┘                                                   ║
╚══════════════════════════════════════════════════════════════╝
```

---

## Prompt 1: Sentiment Analysis Pattern

### Prompt
```
Classify the sentiment of these reviews as Positive, Negative, or Neutral:

Example 1: "This phone is amazing! Best purchase ever!" → Positive
Example 2: "Terrible battery life, broke in 2 weeks." → Negative  
Example 3: "It works fine, nothing special." → Neutral
Example 4: "Love the camera but hate the price." → Mixed
Example 5: "Wouldn't recommend to anyone, total waste." → Negative

Now classify these:
1. "Pretty good for the price, exceeded my expectations!"
2. "Arrived damaged, customer service was unhelpful."
3. "It's okay, does what it's supposed to do."
4. "Best headphones I've owned, incredible sound quality!"
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│              SENTIMENT ANALYSIS RESULTS                       │
│                                                               │
│  TRAINING EXAMPLES (what AI learned):                        │
│  ┌────────────────────────────────────────┐                  │
│  │ 😊 Positive markers: amazing, best,    │                  │
│  │    love, incredible                     │                  │
│  │ 😠 Negative markers: terrible, broke,   │                  │
│  │    waste, wouldn't recommend            │                  │
│  │ 😐 Neutral markers: fine, okay, works   │                  │
│  └────────────────────────────────────────┘                  │
│                                                               │
│  RESULTS:                                                     │
│  ┌──────────────────────────────────────────────────────┐    │
│  │ 1. "Pretty good...exceeded expectations"             │    │
│  │    ████████████████████████ POSITIVE (92%)            │    │
│  │                                                       │    │
│  │ 2. "Arrived damaged...unhelpful"                     │    │
│  │    ████████████████████████ NEGATIVE (96%)            │    │
│  │                                                       │    │
│  │ 3. "It's okay...supposed to do"                      │    │
│  │    ████████████████████████ NEUTRAL  (88%)            │    │
│  │                                                       │    │
│  │ 4. "Best headphones...incredible sound"              │    │
│  │    ████████████████████████ POSITIVE (98%)            │    │
│  └──────────────────────────────────────────────────────┘    │
│                                                               │
│  CONFIDENCE DISTRIBUTION:                                    │
│  Positive ████████████  50%                                  │
│  Negative ██████  25%                                        │
│  Neutral  ██████  25%                                        │
└──────────────────────────────────────────────────────────────┘
```

---

## Prompt 2: Data Transformation Pattern

### Prompt
```
Transform these data entries from raw format to structured JSON:

Raw: "John Smith, 28, New York, Software Engineer, $95000"
JSON: {"name": "John Smith", "age": 28, "city": "New York", "role": "Software Engineer", "salary": 95000}

Raw: "Jane Doe, 34, San Francisco, Product Manager, $120000"
JSON: {"name": "Jane Doe", "age": 34, "city": "San Francisco", "role": "Product Manager", "salary": 120000}

Raw: "Bob Wilson, 45, Chicago, VP Engineering, $180000"
JSON: {"name": "Bob Wilson", "age": 45, "city": "Chicago", "role": "VP Engineering", "salary": 180000}

Now transform these:
1. "Alice Chen, 31, Seattle, Data Scientist, $110000"
2. "Carlos Rivera, 27, Austin, Frontend Developer, $85000"
3. "Sara Khan, 39, Boston, CTO, $200000"
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│           DATA TRANSFORMATION PIPELINE                        │
│                                                               │
│  PATTERN LEARNED:                                            │
│  ┌──────────────────────────────────────────┐                │
│  │  "Name, Age, City, Role, $Salary"        │                │
│  │         │                                 │                │
│  │         ▼                                 │                │
│  │  {                                        │                │
│  │    "name":   → string (First Last)       │                │
│  │    "age":    → integer                   │                │
│  │    "city":   → string                    │                │
│  │    "role":   → string                    │                │
│  │    "salary": → integer (remove $)        │                │
│  │  }                                        │                │
│  └──────────────────────────────────────────┘                │
│                                                               │
│  OUTPUT:                                                      │
│  ┌──────────────────────────────────────────┐                │
│  │  1. {                                     │                │
│  │       "name": "Alice Chen",              │                │
│  │       "age": 31,                          │                │
│  │       "city": "Seattle",                  │                │
│  │       "role": "Data Scientist",           │                │
│  │       "salary": 110000                    │                │
│  │     }                                     │                │
│  ├──────────────────────────────────────────┤                │
│  │  2. {                                     │                │
│  │       "name": "Carlos Rivera",           │                │
│  │       "age": 27,                          │                │
│  │       "city": "Austin",                   │                │
│  │       "role": "Frontend Developer",       │                │
│  │       "salary": 85000                     │                │
│  │     }                                     │                │
│  ├──────────────────────────────────────────┤                │
│  │  3. {                                     │                │
│  │       "name": "Sara Khan",               │                │
│  │       "age": 39,                          │                │
│  │       "city": "Boston",                   │                │
│  │       "role": "CTO",                      │                │
│  │       "salary": 200000                    │                │
│  │     }                                     │                │
│  └──────────────────────────────────────────┘                │
└──────────────────────────────────────────────────────────────┘
```

---

## Image Examples

| Prompt | Expected Image Type | Description |
|--------|-------------------|-------------|
| Sentiment analysis | Dashboard with gauges | Color-coded bars (green/red/gray) showing confidence percentages |
| Data transformation | Pipeline flow diagram | Raw text box → transformation arrows → JSON code blocks |
| Classification | Category grid | Items sorted into labeled columns with percentage confidence |
