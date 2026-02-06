# 02 - Chain-of-Thought Prompts for Gemini Nano Bana

```
╔══════════════════════════════════════════════════════════════════╗
║                CHAIN-OF-THOUGHT PROMPTS                          ║
║                                                                  ║
║  Guide the AI to think step-by-step for deeper reasoning         ║
║                                                                  ║
║  Step 1 ──> Step 2 ──> Step 3 ──> Step 4 ──> ANSWER            ║
║    │          │          │          │           │                 ║
║  Think      Analyze    Connect    Conclude   Deliver             ║
║                                                                  ║
║  ┌──────────────┐  ┌──────────────┐  ┌────────────────────┐    ║
║  │  Step-by-Step│  │  Tree of     │  │    Logical          │    ║
║  │  Reasoning   │  │  Thought     │  │    Decomposition    │    ║
║  └──────────────┘  └──────────────┘  └────────────────────┘    ║
╚══════════════════════════════════════════════════════════════════╝
```

## What Are Chain-of-Thought Prompts?

Chain-of-Thought (CoT) prompts instruct Gemini Nano Bana to **show its reasoning process** step-by-step before arriving at a final answer. This dramatically improves accuracy for complex problems.

## Types Included

| Type | File | Difficulty | Best For |
|------|------|-----------|----------|
| Step-by-Step Reasoning | [step-by-step-reasoning.md](step-by-step-reasoning.md) | Intermediate | Math, logic, analysis |
| Tree of Thought | [tree-of-thought.md](tree-of-thought.md) | Advanced | Complex decisions, multi-path problems |
| Logical Decomposition | [logical-decomposition.md](logical-decomposition.md) | Intermediate | Breaking down complex topics |

## Visual Process

```
    CHAIN-OF-THOUGHT PROCESS
    ========================

    INPUT: "Why is the sky blue?"

    ┌─────────────────────────────────────────┐
    │ STEP 1: Identify the phenomenon          │
    │ - Sunlight enters Earth's atmosphere     │
    ├─────────────────────────────────────────┤
    │ STEP 2: Understand the science           │
    │ - Sunlight contains all colors           │
    │ - Each color has different wavelength     │
    ├─────────────────────────────────────────┤
    │ STEP 3: Apply the mechanism              │
    │ - Rayleigh scattering occurs             │
    │ - Short wavelengths scatter more         │
    ├─────────────────────────────────────────┤
    │ STEP 4: Conclude                         │
    │ - Blue light has short wavelength        │
    │ - It scatters most, making sky look blue │
    └─────────────────────────────────────────┘

    OUTPUT: Complete, reasoned explanation
```
