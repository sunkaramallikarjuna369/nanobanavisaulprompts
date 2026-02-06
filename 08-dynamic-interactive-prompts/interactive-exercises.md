# Interactive Exercise Prompts for Gemini Nano Bana

```
╔══════════════════════════════════════════════════════════════╗
║            INTERACTIVE EXERCISE PROMPTS                       ║
╚══════════════════════════════════════════════════════════════╝
```

---

## Prompt 1: Code Challenge Exercise

### Prompt
```
Create an interactive coding exercise for learning Python lists:
1. Present a problem statement
2. Show starter code with blanks to fill
3. Provide hints (3 levels: gentle, medium, direct)
4. Show the solution with explanation
5. Give a follow-up challenge that builds on it

Topic: Filtering even numbers from a list using list comprehension.
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│  CODING CHALLENGE: List Comprehension                        │
│  Difficulty: ★★☆☆☆ Beginner                                │
│                                                               │
│  PROBLEM: Filter even numbers from [1,2,3,4,5,6,7,8,9,10]  │
│                                                               │
│  STARTER CODE:                                                │
│  numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]                 │
│  evens = [x for x in numbers if ________]                    │
│  print(evens)                                                 │
│                                                               │
│  HINTS:                                                       │
│  💡 Level 1: Even numbers are divisible by 2                │
│  💡 Level 2: Use the modulo operator (%)                    │
│  💡 Level 3: The condition is x % 2 == 0                    │
│                                                               │
│  SOLUTION:                                                    │
│  evens = [x for x in numbers if x % 2 == 0]                 │
│  # Output: [2, 4, 6, 8, 10]                                 │
│                                                               │
│  FOLLOW-UP: Now filter numbers > 5 AND divisible by 3       │
└──────────────────────────────────────────────────────────────┘
```

---

## Prompt 2: Debugging Exercise

### Prompt
```
Create a debugging exercise. Show broken code with 3 bugs hidden
in it. The student must find and fix all bugs. Provide the buggy
code, expected output, actual (wrong) output, and after they
attempt it, reveal each bug with explanation.

Topic: A function that calculates the average of a list.
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│  DEBUG CHALLENGE: Find 3 Bugs                                │
│  Difficulty: ★★★☆☆ Intermediate                            │
│                                                               │
│  BUGGY CODE:                                                  │
│  def calculate_average(numbers):                              │
│      total = 0                                                │
│      for i in range(len(numbers)):  # Bug hint area         │
│          total += numbers                    # 🐛 Bug 1     │
│      average = total / len(numbers) - 1      # 🐛 Bug 2     │
│      return round(average)                   # 🐛 Bug 3     │
│                                                               │
│  Expected: calculate_average([10,20,30]) → 20.0             │
│  Actual:   TypeError / Wrong result                          │
│                                                               │
│  ANSWERS:                                                     │
│  Bug 1: numbers → numbers[i]  (forgot index)                │
│  Bug 2: len(numbers) - 1 → (len(numbers) - 1) needs ()     │
│         Actually: should be len(numbers) without -1          │
│  Bug 3: round(average) → round(average, 1) for decimals     │
└──────────────────────────────────────────────────────────────┘
```

---

## Image Examples

| Prompt | Expected Image Type | Description |
|--------|-------------------|-------------|
| Code challenge | IDE-style card | Dark code editor theme with blanks highlighted in yellow |
| Debug exercise | Split-screen | Left: buggy code with red highlights, Right: fixed code with green highlights |
