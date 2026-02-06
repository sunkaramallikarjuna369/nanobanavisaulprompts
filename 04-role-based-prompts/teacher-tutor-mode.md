# Teacher/Tutor Mode Prompts for Gemini Nano Bana

```
╔══════════════════════════════════════════════════════════════╗
║               TEACHER / TUTOR MODE PROMPTS                   ║
║                                                              ║
║  "Explain [TOPIC] as if I'm a [LEVEL] student"              ║
║                                                              ║
║  ┌─────────┐   ┌──────────────┐   ┌─────────────────────┐  ║
║  │ Student │──>│  AI Teacher  │──>│ Adaptive Lesson     │  ║
║  │ Level   │   │  Persona     │   │ with examples       │  ║
║  └─────────┘   └──────────────┘   └─────────────────────┘  ║
╚══════════════════════════════════════════════════════════════╝
```

---

## Prompt 1: Beginner-Friendly Explanation

### Prompt
```
You are a patient, encouraging computer science teacher for beginners.
Explain how APIs work to a 10-year-old using a fun real-world analogy.
Use simple words, no jargon. Include a step-by-step example they can
relate to, like ordering food at a restaurant.
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│  HOW APIs WORK (Restaurant Analogy)                          │
│                                                               │
│  👤 YOU                    📋 WAITER              👨‍🍳 KITCHEN  │
│  (App/User)               (API)                 (Server)     │
│                                                               │
│  Step 1: You look at      Step 2: Waiter        Step 3:      │
│  the MENU and decide      takes your ORDER      Kitchen      │
│  what you want            to the kitchen        MAKES food   │
│       │                        │                     │       │
│       ▼                        ▼                     ▼       │
│  ┌─────────┐             ┌──────────┐          ┌─────────┐  │
│  │ "I want │────────────>│ Carries  │─────────>│ Prepares│  │
│  │  pizza" │             │ request  │          │  pizza  │  │
│  └─────────┘             └──────────┘          └────┬────┘  │
│                                                      │       │
│  Step 5: You             Step 4: Waiter              │       │
│  EAT and enjoy!          brings food BACK            │       │
│       ▲                        ▲                     │       │
│  ┌─────────┐             ┌──────────┐               │       │
│  │  Yummy! │<────────────│ Delivers │<──────────────┘       │
│  │  🍕     │             │ response │                        │
│  └─────────┘             └──────────┘                        │
│                                                               │
│  API = The waiter who carries your request and brings back   │
│  the response. You never go to the kitchen yourself!         │
└──────────────────────────────────────────────────────────────┘
```

---

## Prompt 2: Progressive Difficulty Lesson

### Prompt
```
You are a university professor teaching Machine Learning.
Create a 3-level explanation of Neural Networks:
- Level 1 (Beginner): Simple analogy, no math
- Level 2 (Intermediate): Key concepts with basic formulas
- Level 3 (Advanced): Full architecture with backpropagation details
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│  NEURAL NETWORKS: 3-LEVEL EXPLANATION                         │
│                                                               │
│  ┌─ LEVEL 1: BEGINNER ─────────────────────────────────────┐│
│  │  Think of a neural network like a team of decision-      ││
│  │  makers. Each person looks at the data and votes.        ││
│  │  The majority vote wins!                                  ││
│  │                                                           ││
│  │  Input → [Vote] [Vote] [Vote] → Majority = Answer       ││
│  └──────────────────────────────────────────────────────────┘│
│                                                               │
│  ┌─ LEVEL 2: INTERMEDIATE ─────────────────────────────────┐│
│  │  Layers of neurons connected by weighted edges:          ││
│  │  output = activation(Σ(weight × input) + bias)          ││
│  │                                                           ││
│  │  [x1]─w1─┐                                               ││
│  │  [x2]─w2─┼─[Σ + b]─→ σ(z) ─→ output                   ││
│  │  [x3]─w3─┘                                               ││
│  └──────────────────────────────────────────────────────────┘│
│                                                               │
│  ┌─ LEVEL 3: ADVANCED ─────────────────────────────────────┐│
│  │  Forward: z = Wx + b, a = σ(z)                          ││
│  │  Loss: L = -Σ[y·log(ŷ) + (1-y)·log(1-ŷ)]             ││
│  │  Backward: ∂L/∂W = ∂L/∂a · ∂a/∂z · ∂z/∂W             ││
│  │  Update: W = W - α · ∂L/∂W                             ││
│  │                                                           ││
│  │  [Input]→[Dense(128,ReLU)]→[Dense(64,ReLU)]→[Softmax]  ││
│  └──────────────────────────────────────────────────────────┘│
└──────────────────────────────────────────────────────────────┘
```

---

## Prompt 3: Interactive Quiz Teacher

### Prompt
```
You are a friendly quiz master teaching Python programming.
Create a mini-lesson about Python lists followed by 3 quiz
questions of increasing difficulty. For each question, provide
the answer hidden behind a "Think about it first!" hint.
After the quiz, give a score guide and next steps.
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│  PYTHON LISTS: MINI-LESSON + QUIZ                            │
│                                                               │
│  📚 LESSON: Lists are ordered collections                    │
│  fruits = ["apple", "banana", "cherry"]                      │
│  fruits[0] → "apple"     fruits[-1] → "cherry"              │
│  fruits.append("date")   len(fruits) → 4                    │
│                                                               │
│  ═══════════════════════════════════════                      │
│                                                               │
│  ❓ Q1 (Easy): What does fruits[1] return?                   │
│  💡 Hint: Indexing starts at 0!                              │
│  ✅ Answer: "banana"                                         │
│                                                               │
│  ❓ Q2 (Medium): What is fruits[1:3]?                        │
│  💡 Hint: Slicing is [start:end) - end is excluded!         │
│  ✅ Answer: ["banana", "cherry"]                             │
│                                                               │
│  ❓ Q3 (Hard): What does fruits[::-1] do?                    │
│  💡 Hint: Step of -1 means...                               │
│  ✅ Answer: ["cherry", "banana", "apple"] (reversed!)        │
│                                                               │
│  SCORE GUIDE:                                                │
│  3/3: ⭐ Python List Master! Try dictionaries next           │
│  2/3: 👍 Almost there! Review slicing                       │
│  1/3: 📖 Re-read the lesson, practice in a REPL            │
└──────────────────────────────────────────────────────────────┘
```

---

## Image Examples

| Prompt | Expected Image Type | Description |
|--------|-------------------|-------------|
| API analogy | Illustrated flow | Cartoon-style restaurant scene with labeled characters as API components |
| Neural network levels | Layered diagram | 3 panels stacked showing increasing complexity from analogy to math |
| Quiz teacher | Interactive card | Question cards with expandable hint/answer sections, progress indicator |
