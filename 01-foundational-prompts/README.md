# 01 - Foundational Prompts for Gemini Nano Bana

```
+----------------------------------------------------------+
|                  FOUNDATIONAL PROMPTS                     |
|                                                          |
|   The building blocks of all prompt engineering.         |
|   Master these first before advancing to complex types.  |
|                                                          |
|   +------------+  +------------+  +----------------+     |
|   | Zero-Shot  |  |  Direct    |  |   Template     |     |
|   |  Prompts   |->| Instruction|->|    Based       |     |
|   +------------+  +------------+  +----------------+     |
|         |               |               |                |
|         v               v               v                |
|   [ Simple Q&A ]  [ Task-Based ]  [ Structured ]         |
+----------------------------------------------------------+
```

## What Are Foundational Prompts?

Foundational prompts are the simplest and most direct way to interact with Gemini Nano Bana. They form the base layer upon which all advanced prompting techniques are built.

## Types Included

| Type | File | Difficulty | Best For |
|------|------|-----------|----------|
| Zero-Shot Prompts | [zero-shot-prompts.md](zero-shot-prompts.md) | Beginner | Quick answers, simple tasks |
| Direct Instruction Prompts | [direct-instruction-prompts.md](direct-instruction-prompts.md) | Beginner | Clear task execution |
| Template-Based Prompts | [template-based-prompts.md](template-based-prompts.md) | Beginner-Intermediate | Consistent output formatting |

## Visual Overview

```
    FOUNDATIONAL PROMPTS HIERARCHY
    ==============================

    Level 1: Zero-Shot (No examples needed)
    ┌─────────────────────────────────┐
    │  "What is machine learning?"    │
    │  "Explain photosynthesis"       │
    │  "Define blockchain"            │
    └─────────────┬───────────────────┘
                  │
    Level 2: Direct Instruction (Clear commands)
    ┌─────────────┴───────────────────┐
    │  "List 5 benefits of yoga"      │
    │  "Write a haiku about rain"     │
    │  "Calculate the area of..."     │
    └─────────────┬───────────────────┘
                  │
    Level 3: Template-Based (Structured format)
    ┌─────────────┴───────────────────┐
    │  "Using this format: [Title]    │
    │   [Summary] [Key Points]        │
    │   explain quantum computing"    │
    └─────────────────────────────────┘
```

## When to Use

- Starting a new topic exploration
- Need quick, direct answers
- Building blocks for more complex prompts
- Teaching beginners prompt engineering
