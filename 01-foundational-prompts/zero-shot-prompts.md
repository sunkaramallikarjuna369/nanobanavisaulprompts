# Zero-Shot Prompts for Gemini Nano Bana

```
╔══════════════════════════════════════════════════════════╗
║                   ZERO-SHOT PROMPTS                      ║
║                                                          ║
║  No examples needed - just ask directly!                 ║
║                                                          ║
║  ┌──────────┐    ┌──────────────┐    ┌──────────────┐   ║
║  │  INPUT   │───>│  GEMINI NANO │───>│   OUTPUT     │   ║
║  │ (Query)  │    │    BANA      │    │  (Answer)    │   ║
║  └──────────┘    └──────────────┘    └──────────────┘   ║
╚══════════════════════════════════════════════════════════╝
```

## What is a Zero-Shot Prompt?

A zero-shot prompt gives the AI a task **without any examples**. You simply describe what you want, and the model uses its training knowledge to respond.

---

## Prompt Type 1: Simple Question

### Prompt
```
What is artificial intelligence and how does it impact daily life?
```

### Expected Output
A clear explanation of AI with real-world examples like virtual assistants, recommendation systems, etc.

### Expected Visual Output
```
┌─────────────────────────────────────────────────┐
│            ARTIFICIAL INTELLIGENCE               │
│                                                  │
│  ┌──────────┐  ┌──────────┐  ┌──────────┐      │
│  │  Virtual  │  │  Self-   │  │  Smart   │      │
│  │Assistants │  │ Driving  │  │  Home    │      │
│  │  (Siri,  │  │  Cars    │  │ Devices  │      │
│  │  Alexa)  │  │          │  │          │      │
│  └────┬─────┘  └────┬─────┘  └────┬─────┘      │
│       │              │              │            │
│       └──────────────┼──────────────┘            │
│                      │                           │
│              ┌───────┴────────┐                  │
│              │  Daily Life    │                  │
│              │  Integration   │                  │
│              └────────────────┘                  │
└─────────────────────────────────────────────────┘
```

---

## Prompt Type 2: Definition Request

### Prompt
```
Define quantum computing in simple terms that a 10-year-old could understand.
```

### Expected Output
A simplified explanation using analogies (e.g., "normal computers use switches that are ON or OFF, quantum computers use switches that can be ON, OFF, or BOTH at the same time").

### Expected Visual Output
```
┌────────────────────────────────────────────────────┐
│          QUANTUM COMPUTING SIMPLIFIED               │
│                                                     │
│  Classical Computer          Quantum Computer       │
│  ┌─────────────┐            ┌─────────────┐        │
│  │  Bit: 0 OR 1│            │Qubit: 0 AND 1│       │
│  │  ┌───┐      │            │  ┌───────┐   │       │
│  │  │ 0 │      │            │  │ 0 + 1 │   │       │
│  │  └───┘      │            │  └───────┘   │       │
│  │     OR      │            │  BOTH AT     │       │
│  │  ┌───┐      │            │  THE SAME    │       │
│  │  │ 1 │      │            │  TIME!       │       │
│  │  └───┘      │            │              │       │
│  └─────────────┘            └─────────────┘        │
│                                                     │
│  Like a coin:               Like a spinning coin:   │
│  Heads OR Tails             Heads AND Tails!        │
└────────────────────────────────────────────────────┘
```

---

## Prompt Type 3: Explanation Request

### Prompt
```
Explain how solar panels convert sunlight into electricity.
```

### Expected Output
Step-by-step explanation of the photovoltaic effect.

### Expected Visual Output
```
┌──────────────────────────────────────────────────────┐
│           SOLAR PANEL ENERGY CONVERSION               │
│                                                       │
│    ☀ SUNLIGHT (Photons)                              │
│        │                                              │
│        ▼                                              │
│   ┌─────────────────┐                                │
│   │  SOLAR PANEL     │                                │
│   │  ┌─────────────┐ │                                │
│   │  │Silicon Cells │ │  Photons hit silicon atoms    │
│   │  │  ⚡ ⚡ ⚡    │ │  Electrons get excited        │
│   │  │  ⚡ ⚡ ⚡    │ │  Electric field pushes them   │
│   │  └──────┬──────┘ │                                │
│   └─────────┼────────┘                                │
│             ▼                                         │
│   ┌──────────────────┐                                │
│   │  DC ELECTRICITY   │                                │
│   └────────┬─────────┘                                │
│            ▼                                          │
│   ┌──────────────────┐                                │
│   │    INVERTER       │  Converts DC to AC            │
│   └────────┬─────────┘                                │
│            ▼                                          │
│   ┌──────────────────┐                                │
│   │  AC ELECTRICITY   │  Powers your home!            │
│   │  🏠 💡 📺 🖥️    │                                │
│   └──────────────────┘                                │
└──────────────────────────────────────────────────────┘
```

---

## Prompt Type 4: List Generation

### Prompt
```
List the top 10 programming languages in 2025 with their primary use cases.
```

### Expected Output
A numbered list with language names and use cases.

### Expected Visual Output
```
┌──────────────────────────────────────────────────┐
│        TOP PROGRAMMING LANGUAGES 2025            │
│                                                   │
│  ┌─────────────┬───────────────────────────┐     │
│  │  Language    │  Primary Use Case         │     │
│  ├─────────────┼───────────────────────────┤     │
│  │ 1. Python   │ AI/ML, Data Science       │     │
│  │ 2. JavaScript│ Web Development          │     │
│  │ 3. TypeScript│ Enterprise Web Apps      │     │
│  │ 4. Rust     │ Systems Programming       │     │
│  │ 5. Go       │ Cloud & DevOps            │     │
│  │ 6. Java     │ Enterprise Applications   │     │
│  │ 7. C++      │ Game Dev, Embedded        │     │
│  │ 8. Kotlin   │ Android Development       │     │
│  │ 9. Swift    │ iOS Development           │     │
│  │10. SQL      │ Database Management       │     │
│  └─────────────┴───────────────────────────┘     │
└──────────────────────────────────────────────────┘
```

---

## Prompt Type 5: Concept Visualization Request

### Prompt
```
Visualize the water cycle as a diagram with all stages labeled.
```

### Expected Output
A text-based diagram showing evaporation, condensation, precipitation, and collection.

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────┐
│                    THE WATER CYCLE                         │
│                                                           │
│         ☁ ☁ ☁ CONDENSATION ☁ ☁ ☁                        │
│        ╱    (Water vapor cools    ╲                       │
│       ╱      and forms clouds)     ╲                      │
│      ╱                              ╲                     │
│  EVAPORATION                    PRECIPITATION             │
│  (Sun heats                     (Rain, snow,              │
│   water)                         sleet, hail)             │
│     ↑                               ↓                     │
│     │    ☀                          │                     │
│     │   ╱╲╱╲                       │                     │
│  ~~~│~~╱~~~~╲~~~~~~~~~~~~~~~~~~~~~~~│~~~                  │
│  ~OCEAN~  ~LAKE~   ←──RUNOFF──←   ~│~                    │
│  ~~~~~~~~  ~~~~~~                  ~│~                    │
│                    ┌────────────────┘                     │
│                    │  COLLECTION                          │
│                    │  (Water gathers in                   │
│                    │   oceans, lakes, rivers)             │
│                    └────────────────                      │
└──────────────────────────────────────────────────────────┘
```

---

## Best Practices for Zero-Shot Prompts

```
┌──────────────────────────────────────────┐
│        ZERO-SHOT BEST PRACTICES          │
│                                          │
│  ✦ Be specific and clear                │
│  ✦ Use simple, direct language           │
│  ✦ State the desired format              │
│  ✦ Mention the audience level            │
│  ✦ One question per prompt works best    │
│                                          │
│  GOOD: "Explain DNA replication in       │
│         3 simple steps"                  │
│                                          │
│  BAD:  "Tell me about DNA"              │
└──────────────────────────────────────────┘
```

---

## Image Examples: What Gemini Nano Bana Would Generate

When using these prompts with visual mode, expect outputs like:

| Prompt | Expected Image Type | Description |
|--------|-------------------|-------------|
| "What is AI?" | Infographic | Colorful diagram showing AI branches (ML, NLP, CV) with icons |
| "Explain the solar system" | Orbital diagram | Planets arranged around the sun with labels and distances |
| "How does WiFi work?" | Signal flow diagram | Router emitting waves to devices with data packet visualization |
| "What is DNA?" | Double helix illustration | Colored base pairs (A-T, G-C) in a twisted ladder structure |
| "Explain gravity" | Force diagram | Objects with arrows showing gravitational pull, Earth-Moon example |
