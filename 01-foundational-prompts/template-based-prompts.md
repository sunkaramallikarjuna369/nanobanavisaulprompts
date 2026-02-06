# Template-Based Prompts for Gemini Nano Bana

```
╔══════════════════════════════════════════════════════════════╗
║               TEMPLATE-BASED PROMPTS                         ║
║                                                              ║
║  Pre-structured formats for consistent, repeatable output    ║
║                                                              ║
║  ┌──────────┐    ┌──────────────┐    ┌──────────────────┐   ║
║  │ TEMPLATE │───>│  GEMINI NANO │───>│ FORMATTED OUTPUT │   ║
║  │ + Topic  │    │    BANA      │    │ (Follows your    │   ║
║  │          │    │              │    │  template)       │   ║
║  └──────────┘    └──────────────┘    └──────────────────┘   ║
╚══════════════════════════════════════════════════════════════╝
```

## What Are Template-Based Prompts?

Template prompts provide a **pre-defined structure** that Gemini Nano Bana fills in. This ensures consistent, well-organized output every time.

---

## Prompt Type 1: Structured Report Template

### Prompt
```
Use this template to explain Machine Learning:

**Topic:** [Topic Name]
**Definition:** [2-3 sentence definition]
**Key Concepts:**
  1. [Concept 1] - [Brief explanation]
  2. [Concept 2] - [Brief explanation]
  3. [Concept 3] - [Brief explanation]
**Real-World Applications:**
  - [Application 1]
  - [Application 2]
  - [Application 3]
**Visual Diagram:** [ASCII diagram showing the concept]
**Summary:** [1 paragraph summary]
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│                    MACHINE LEARNING REPORT                    │
│  ┌──────────────────────────────────────────────────────┐    │
│  │ TOPIC: Machine Learning                               │    │
│  ├──────────────────────────────────────────────────────┤    │
│  │ DEFINITION:                                           │    │
│  │ Machine Learning is a subset of AI that enables       │    │
│  │ systems to learn from data without being explicitly   │    │
│  │ programmed.                                           │    │
│  ├──────────────────────────────────────────────────────┤    │
│  │ KEY CONCEPTS:                                         │    │
│  │ ┌───────────────┬───────────────┬───────────────┐    │    │
│  │ │  Supervised   │ Unsupervised  │ Reinforcement │    │    │
│  │ │  Learning     │  Learning     │  Learning     │    │    │
│  │ │ (Labeled      │ (Pattern      │ (Reward-based │    │    │
│  │ │  data)        │  discovery)   │  learning)    │    │    │
│  │ └───────────────┴───────────────┴───────────────┘    │    │
│  ├──────────────────────────────────────────────────────┤    │
│  │ APPLICATIONS:                                         │    │
│  │ [Spam Filter] [Self-Driving] [Medical Diagnosis]     │    │
│  ├──────────────────────────────────────────────────────┤    │
│  │ DIAGRAM:                                              │    │
│  │   Data ──> Training ──> Model ──> Predictions        │    │
│  └──────────────────────────────────────────────────────┘    │
└──────────────────────────────────────────────────────────────┘
```

---

## Prompt Type 2: Lesson Plan Template

### Prompt
```
Fill in this lesson plan template for teaching "Introduction to Python":

**Lesson Title:** ___
**Duration:** ___
**Learning Objectives:**
  - By the end, students will be able to ___
  - By the end, students will be able to ___
  - By the end, students will be able to ___
**Prerequisites:** ___
**Materials Needed:** ___
**Lesson Outline:**
  | Time | Activity | Description |
  |------|----------|-------------|
  | _    | _        | _           |
**Assessment:** ___
**Homework:** ___
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│              LESSON PLAN: INTRO TO PYTHON                    │
│                                                               │
│  ┌─ OBJECTIVES ─────────────────────────────────────────┐    │
│  │ ✦ Write basic Python programs                        │    │
│  │ ✦ Understand variables, data types, operators        │    │
│  │ ✦ Use print() and input() functions                  │    │
│  └──────────────────────────────────────────────────────┘    │
│                                                               │
│  ┌─ TIMELINE ───────────────────────────────────────────┐    │
│  │                                                       │    │
│  │  [0-10min]     [10-25min]    [25-40min]   [40-50min] │    │
│  │  Introduction   Demo &       Hands-on      Q&A &     │    │
│  │  & Setup        Lecture      Practice      Wrap-up   │    │
│  │     │              │            │             │       │    │
│  │     ▼              ▼            ▼             ▼       │    │
│  │  Install       Variables    Write first    Review     │    │
│  │  Python        & Types      program        & Quiz     │    │
│  └──────────────────────────────────────────────────────┘    │
│                                                               │
│  ┌─ ASSESSMENT ─────────────────────────────────────────┐    │
│  │  Quiz: 5 MCQs + 1 coding exercise                    │    │
│  │  Homework: Write a calculator program                 │    │
│  └──────────────────────────────────────────────────────┘    │
└──────────────────────────────────────────────────────────────┘
```

---

## Prompt Type 3: SWOT Analysis Template

### Prompt
```
Perform a SWOT analysis for a startup launching an AI-powered
fitness app. Use this exact format:

┌─────────────────┬─────────────────┐
│   STRENGTHS     │   WEAKNESSES    │
│   (Internal +)  │   (Internal -)  │
│                 │                 │
│   1.            │   1.            │
│   2.            │   2.            │
│   3.            │   3.            │
├─────────────────┼─────────────────┤
│  OPPORTUNITIES  │     THREATS     │
│  (External +)   │  (External -)   │
│                 │                 │
│   1.            │   1.            │
│   2.            │   2.            │
│   3.            │   3.            │
└─────────────────┴─────────────────┘
```

### Expected Visual Output
```
┌────────────────────────────────────────────────────────────┐
│           SWOT ANALYSIS: AI FITNESS APP                     │
│                                                             │
│  ┌──── HELPFUL ──────────┬──── HARMFUL ──────────┐         │
│  │                       │                        │         │
│  │  STRENGTHS            │  WEAKNESSES            │         │
│  │  ┌──────────────────┐ │  ┌──────────────────┐ │         │
│  │  │ 1. Personalized  │ │  │ 1. High dev cost │ │         │
│  │  │    AI workouts   │ │  │ 2. Data privacy  │ │         │
│  │  │ 2. 24/7 avail.   │ │  │    concerns      │ │         │
│  │  │ 3. Data-driven   │ │  │ 3. Limited brand │ │         │
│  │  │    insights      │ │  │    recognition   │ │         │
│  │  └──────────────────┘ │  └──────────────────┘ │         │
│  │                       │                        │         │
│  ├───────────────────────┼────────────────────────┤         │
│  │                       │                        │         │
│  │  OPPORTUNITIES        │  THREATS               │         │
│  │  ┌──────────────────┐ │  ┌──────────────────┐ │         │
│  │  │ 1. Growing       │ │  │ 1. Big tech      │ │         │
│  │  │    health market │ │  │    competitors   │ │         │
│  │  │ 2. Wearable      │ │  │ 2. AI regulation │ │         │
│  │  │    integration   │ │  │ 3. Market        │ │         │
│  │  │ 3. Corporate     │ │  │    saturation    │ │         │
│  │  │    wellness      │ │  │                  │ │         │
│  │  └──────────────────┘ │  └──────────────────┘ │         │
│  └───────────────────────┴────────────────────────┘         │
└────────────────────────────────────────────────────────────┘
```

---

## Prompt Type 4: Technical Documentation Template

### Prompt
```
Document the following function using this template:

**Function Name:** `calculateCompoundInterest()`
**Purpose:** ___
**Parameters:**
  | Name | Type | Required | Description |
  |------|------|----------|-------------|
  | _    | _    | _        | _           |
**Return Value:** ___
**Example Usage:**
  ```
  [code example]
  ```
**Edge Cases:** ___
**Related Functions:** ___
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│         FUNCTION DOCUMENTATION                                │
│  ┌──────────────────────────────────────────────────────┐    │
│  │  calculateCompoundInterest()                          │    │
│  ├──────────────────────────────────────────────────────┤    │
│  │  PURPOSE: Calculate compound interest over time       │    │
│  ├──────────────────────────────────────────────────────┤    │
│  │  PARAMETERS:                                          │    │
│  │  ┌──────────┬────────┬──────┬──────────────────┐     │    │
│  │  │ Name     │ Type   │ Req? │ Description      │     │    │
│  │  ├──────────┼────────┼──────┼──────────────────┤     │    │
│  │  │principal │ number │  Y   │ Initial amount   │     │    │
│  │  │rate      │ number │  Y   │ Annual rate (%)  │     │    │
│  │  │time      │ number │  Y   │ Years            │     │    │
│  │  │frequency │ number │  N   │ Times/year (12)  │     │    │
│  │  └──────────┴────────┴──────┴──────────────────┘     │    │
│  ├──────────────────────────────────────────────────────┤    │
│  │  RETURNS: number (final amount with interest)         │    │
│  ├──────────────────────────────────────────────────────┤    │
│  │  EXAMPLE:                                             │    │
│  │  calculateCompoundInterest(1000, 5, 10, 12)          │    │
│  │  // Returns: 1647.01                                  │    │
│  └──────────────────────────────────────────────────────┘    │
└──────────────────────────────────────────────────────────────┘
```

---

## Prompt Type 5: Product Comparison Template

### Prompt
```
Compare iPhone 16 Pro vs Samsung Galaxy S25 Ultra using this template:

**Product Comparison: [Product A] vs [Product B]**

| Feature        | [Product A]  | [Product B]  | Winner |
|---------------|-------------|-------------|--------|
| Display       |             |             |        |
| Camera        |             |             |        |
| Battery       |             |             |        |
| Performance   |             |             |        |
| Price         |             |             |        |
| Storage       |             |             |        |

**Overall Winner:** ___
**Best For:** ___
**Verdict:** ___
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│        iPHONE 16 PRO vs GALAXY S25 ULTRA                     │
│                                                               │
│    ┌─────────┐          VS          ┌─────────┐             │
│    │ ┌─────┐ │                      │ ┌─────┐ │             │
│    │ │     │ │                      │ │     │ │             │
│    │ │ iOS │ │                      │ │ AND │ │             │
│    │ │     │ │                      │ │     │ │             │
│    │ └─────┘ │                      │ └─────┘ │             │
│    │ iPhone  │                      │ Galaxy  │             │
│    └─────────┘                      └─────────┘             │
│                                                               │
│  Display  ████████████ 6.3"  vs  ████████████████ 6.9"      │
│  Camera   ████████████████ 48MP vs ██████████████████ 200MP  │
│  Battery  ████████████ 3274  vs  ██████████████████ 5000     │
│  Price    $$$$$$ $1099       vs  $$$$$$$ $1299               │
│                                                               │
│  VERDICT: Galaxy wins specs, iPhone wins ecosystem           │
└──────────────────────────────────────────────────────────────┘
```

---

## Image Examples: What Gemini Nano Bana Would Generate

| Prompt Template | Expected Image Type | Description |
|----------------|-------------------|-------------|
| Report Template | Structured document | Clean, sectioned report with headers, bullet points, and highlighted key data |
| SWOT Analysis | 2x2 color-coded grid | Four quadrants (green/red/blue/orange) with icons and text |
| Lesson Plan | Timeline infographic | Horizontal timeline with activity icons, durations, and milestones |
| API Documentation | Code-style card | Dark-themed card with syntax highlighting and parameter tables |
| Product Comparison | Side-by-side infographic | Two product images with comparison bars and checkmark indicators |
