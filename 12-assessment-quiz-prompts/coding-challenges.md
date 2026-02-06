# Coding Challenge Prompts for Gemini Nano Bana

```
╔══════════════════════════════════════════════════════════════╗
║              CODING CHALLENGE PROMPTS                         ║
╚══════════════════════════════════════════════════════════════╝
```

---

## Prompt 1: Algorithm Challenge

### Prompt
```
Create a coding challenge: "Two Sum Problem"
Include:
- Problem statement with constraints
- 3 test cases (basic, edge case, large input)
- Brute force solution with complexity analysis
- Optimal solution with complexity analysis
- Step-by-step walkthrough of the optimal approach
Difficulty: Easy
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│  CHALLENGE: Two Sum                                          │
│  Difficulty: ★★☆☆☆ Easy                                    │
│                                                               │
│  PROBLEM: Given an array of integers and a target sum,       │
│  return indices of two numbers that add up to the target.    │
│                                                               │
│  TEST CASES:                                                  │
│  Input: [2,7,11,15], target=9  → Output: [0,1]  (2+7=9)    │
│  Input: [3,3], target=6        → Output: [0,1]  (edge)      │
│  Input: [1..10000], target=3   → Output: [0,1]  (large)     │
│                                                               │
│  BRUTE FORCE: O(n²) time, O(1) space                        │
│  for i in range(len(nums)):                                   │
│      for j in range(i+1, len(nums)):                          │
│          if nums[i] + nums[j] == target:                      │
│              return [i, j]                                     │
│                                                               │
│  OPTIMAL: O(n) time, O(n) space                              │
│  seen = {}                                                     │
│  for i, num in enumerate(nums):                               │
│      complement = target - num                                 │
│      if complement in seen:                                    │
│          return [seen[complement], i]                          │
│      seen[num] = i                                             │
│                                                               │
│  WALKTHROUGH: [2,7,11,15], target=9                          │
│  Step 1: num=2, need 7, seen={2:0}                           │
│  Step 2: num=7, need 2, 2 in seen! → return [0,1]           │
└──────────────────────────────────────────────────────────────┘
```

---

## Image Examples

| Prompt | Expected Image Type | Description |
|--------|-------------------|-------------|
| Algorithm challenge | Dual-panel code view | Left: brute force (red border), Right: optimal (green border) with complexity badges |
