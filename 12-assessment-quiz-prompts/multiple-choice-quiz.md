# Multiple Choice Quiz Prompts for Gemini Nano Bana

```
╔══════════════════════════════════════════════════════════════╗
║            MULTIPLE CHOICE QUIZ PROMPTS                       ║
╚══════════════════════════════════════════════════════════════╝
```

---

## Prompt 1: Technical Knowledge Quiz

### Prompt
```
Create a 5-question multiple choice quiz on Python data structures.
For each question:
- 4 options (A, B, C, D) with only one correct answer
- Mark the correct answer
- Explain WHY the correct answer is right
- Explain WHY each wrong answer is wrong
Difficulty: Intermediate level.
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│  PYTHON DATA STRUCTURES QUIZ                                  │
│  Difficulty: ★★★☆☆ Intermediate                             │
│                                                               │
│  Q1: What is the time complexity of checking if an           │
│      element exists in a Python set?                         │
│                                                               │
│  A) O(n)     B) O(1)     C) O(log n)     D) O(n²)          │
│                                                               │
│  ✅ Correct: B) O(1)                                         │
│                                                               │
│  Explanation:                                                 │
│  ✅ B: Sets use hash tables → constant-time lookups          │
│  ❌ A: O(n) is for lists (linear search)                     │
│  ❌ C: O(log n) is for binary search on sorted data          │
│  ❌ D: O(n²) would be nested iteration, not lookup           │
│  ─────────────────────────────────────────────────           │
│  Q2: Which data structure preserves insertion order           │
│      in Python 3.7+?                                         │
│                                                               │
│  A) set   B) frozenset   C) dict   D) None of these         │
│                                                               │
│  ✅ Correct: C) dict                                         │
│  Since Python 3.7, dictionaries maintain insertion order.     │
│  Sets do NOT guarantee order.                                │
└──────────────────────────────────────────────────────────────┘
```

---

## Image Examples

| Prompt | Expected Image Type | Description |
|--------|-------------------|-------------|
| MCQ quiz | Quiz card layout | Numbered question cards with highlighted correct answers and color-coded explanations |
