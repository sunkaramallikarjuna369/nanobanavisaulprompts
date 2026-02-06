# 03 - Few-Shot Prompts for Gemini Nano Bana

```
╔══════════════════════════════════════════════════════════════════╗
║                    FEW-SHOT PROMPTS                               ║
║                                                                  ║
║  Teach the AI by showing examples first!                         ║
║                                                                  ║
║  Example 1 ──┐                                                   ║
║  Example 2 ──┼──> AI learns the pattern ──> Generates new output ║
║  Example 3 ──┘                                                   ║
║                                                                  ║
║  ┌──────────────┐  ┌──────────────┐  ┌──────────────────┐      ║
║  │  One-Shot    │  │  Multi-Shot  │  │    Pattern        │      ║
║  │  Examples    │  │  Examples    │  │    Matching        │      ║
║  └──────────────┘  └──────────────┘  └──────────────────┘      ║
╚══════════════════════════════════════════════════════════════════╝
```

## Types Included

| Type | File | Difficulty | Best For |
|------|------|-----------|----------|
| One-Shot Examples | [one-shot-examples.md](one-shot-examples.md) | Beginner | Simple pattern replication |
| Multi-Shot Examples | [multi-shot-examples.md](multi-shot-examples.md) | Intermediate | Complex pattern learning |
| Pattern Matching | [pattern-matching.md](pattern-matching.md) | Advanced | Format consistency |

## Visual Overview
```
    HOW FEW-SHOT LEARNING WORKS
    ===========================

    ┌──────────────┐
    │  EXAMPLE 1   │  "Paris is to France as Tokyo is to Japan"
    └──────┬───────┘
           ▼
    ┌──────────────┐
    │  EXAMPLE 2   │  "Dog is to puppy as cat is to kitten"
    └──────┬───────┘
           ▼
    ┌──────────────┐
    │  NEW QUERY   │  "Berlin is to Germany as ??? is to ???"
    └──────┬───────┘
           ▼
    ┌──────────────┐
    │  AI OUTPUT   │  "Madrid is to Spain" (learned the pattern!)
    └──────────────┘
```
