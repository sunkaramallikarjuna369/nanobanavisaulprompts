# Tree of Thought Prompts for Gemini Nano Bana

```
╔══════════════════════════════════════════════════════════════╗
║                  TREE OF THOUGHT PROMPTS                     ║
║                                                              ║
║  Explore MULTIPLE reasoning paths simultaneously!            ║
║                                                              ║
║              ┌── Path A ──> Result A                        ║
║             /                                                ║
║  Problem ──┼── Path B ──> Result B  ──> BEST ANSWER         ║
║             \                                                ║
║              └── Path C ──> Result C                        ║
╚══════════════════════════════════════════════════════════════╝
```

---

## Prompt 1: Multi-Path Problem Solving

### Prompt
```
I want you to use Tree of Thought reasoning to solve this:

"How should a small city reduce traffic congestion?"

Explore at least 3 different solution paths. For each path:
1. Describe the approach
2. List pros and cons
3. Estimate effectiveness (1-10)
4. Identify potential issues

Then compare all paths and recommend the best combination.
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────────┐
│              TREE OF THOUGHT: TRAFFIC CONGESTION                  │
│                                                                   │
│                    ┌─ PROBLEM ─┐                                 │
│                    │  Traffic   │                                 │
│                    │ Congestion │                                 │
│                    └─────┬─────┘                                 │
│               ┌──────────┼──────────┐                            │
│               ▼          ▼          ▼                             │
│         ┌──────────┐┌──────────┐┌──────────┐                    │
│   PATH A│  Public  ││ Smart    ││ Urban    │                    │
│         │ Transit  ││ Traffic  ││ Planning │                    │
│         │ Expansion││ Systems  ││ Changes  │                    │
│         └────┬─────┘└────┬─────┘└────┬─────┘                    │
│              ▼           ▼           ▼                            │
│         ┌──────────┐┌──────────┐┌──────────┐                    │
│   PROS  │+Eco-     ││+AI-      ││+Long-term│                    │
│         │ friendly ││ optimized││ solution │                    │
│         │+High     ││+Quick    ││+Quality  │                    │
│         │ capacity ││ deploy   ││ of life  │                    │
│         └──────────┘└──────────┘└──────────┘                    │
│         ┌──────────┐┌──────────┐┌──────────┐                    │
│   CONS  │-Expensive││-Tech     ││-Very slow│                    │
│         │-Slow to  ││ dependent││-Political│                    │
│         │ build    ││-Maintenance│-Expensive│                   │
│         └──────────┘└──────────┘└──────────┘                    │
│                                                                   │
│   Score:    7/10        8/10        6/10                         │
│                                                                   │
│   ┌─════════════════════════════════════════════════════─┐       │
│   ║  BEST: Combine B (Smart Traffic) + A (Transit)       ║       │
│   ║  Quick wins from AI + long-term transit expansion    ║       │
│   └─════════════════════════════════════════════════════─┘       │
└──────────────────────────────────────────────────────────────────┘
```

---

## Prompt 2: Creative Design Decision

### Prompt
```
Use Tree of Thought to design a mobile app landing page.

Consider 3 different design philosophies:
- Path A: Minimalist design
- Path B: Feature-rich showcase  
- Path C: Story-driven narrative

For each, describe the layout, key elements, color scheme,
and expected user engagement. Rate each approach and pick the best.
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────────┐
│           TREE OF THOUGHT: APP LANDING PAGE DESIGN               │
│                                                                   │
│  PATH A: MINIMALIST       PATH B: FEATURE-RICH   PATH C: STORY  │
│  ┌────────────────┐      ┌────────────────┐     ┌────────────┐  │
│  │  ┌──────────┐  │      │ ┌────┐ ┌────┐  │     │ ╔════════╗ │  │
│  │  │   LOGO   │  │      │ │Feat│ │Feat│  │     │ ║ HERO   ║ │  │
│  │  └──────────┘  │      │ │ 1  │ │ 2  │  │     │ ║ IMAGE  ║ │  │
│  │                │      │ └────┘ └────┘  │     │ ╚════════╝ │  │
│  │  One powerful  │      │ ┌────┐ ┌────┐  │     │            │  │
│  │   headline     │      │ │Feat│ │Feat│  │     │  Chapter 1 │  │
│  │                │      │ │ 3  │ │ 4  │  │     │  The Problem│ │
│  │  [ CTA BTN ]  │      │ └────┘ └────┘  │     │            │  │
│  │                │      │ ┌──────────┐   │     │  Chapter 2 │  │
│  │  3 small icons │      │ │ PRICING  │   │     │  Solution  │  │
│  └────────────────┘      │ └──────────┘   │     │            │  │
│                          │ [ SIGN UP ]    │     │  [JOIN US] │  │
│  Colors: B&W +           └────────────────┘     └────────────┘  │
│  1 accent color                                                   │
│  Engagement: ★★★★☆      Colors: Vibrant       Colors: Warm      │
│  Conversion: HIGH        multi-color            earth tones      │
│                          Engagement: ★★★☆☆     Engagement:★★★★★ │
│                          Conversion: MEDIUM     Conversion: HIGH  │
│                                                                   │
│  WINNER: Path A for B2B SaaS, Path C for consumer apps          │
└──────────────────────────────────────────────────────────────────┘
```

---

## Image Examples

| Prompt | Expected Image Type | Description |
|--------|-------------------|-------------|
| Multi-path problem | Branching tree diagram | Root problem branching into colored paths, each with pros/cons cards |
| Design decision | Side-by-side mockups | Three UI wireframes with rating stars and comparison metrics below |
| Strategy planning | Decision tree | Corporate-styled tree with cost/benefit nodes at each branch |
