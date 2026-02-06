# Direct Instruction Prompts for Gemini Nano Bana

```
╔══════════════════════════════════════════════════════════════╗
║                 DIRECT INSTRUCTION PROMPTS                   ║
║                                                              ║
║  Tell the AI exactly what to do - like giving orders!        ║
║                                                              ║
║  ┌──────────┐    ┌──────────────┐    ┌──────────────────┐   ║
║  │ COMMAND  │───>│  GEMINI NANO │───>│ PRECISE OUTPUT   │   ║
║  │ (Action  │    │    BANA      │    │ (Follows your    │   ║
║  │  Verb)   │    │              │    │  instructions)   │   ║
║  └──────────┘    └──────────────┘    └──────────────────┘   ║
╚══════════════════════════════════════════════════════════════╝
```

## What Are Direct Instruction Prompts?

Direct instruction prompts use **action verbs** (Write, Create, List, Generate, Build, Design) to tell Gemini Nano Bana exactly what task to perform. They are precise and leave little room for ambiguity.

---

## Prompt Type 1: Write Command

### Prompt
```
Write a professional email to a client apologizing for a delayed shipment.
Include: reason for delay, new expected delivery date, and a discount offer.
Tone: Professional yet empathetic.
```

### Expected Output
A formatted email with subject line, greeting, body paragraphs, and closing.

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────┐
│  📧 EMAIL TEMPLATE                                       │
│  ┌──────────────────────────────────────────────────┐    │
│  │ FROM: support@company.com                         │    │
│  │ TO: client@email.com                              │    │
│  │ SUBJECT: Update on Your Order #12345              │    │
│  ├──────────────────────────────────────────────────┤    │
│  │                                                    │    │
│  │ Dear [Client Name],                               │    │
│  │                                                    │    │
│  │ ┌────────────────────────────────────────────┐    │    │
│  │ │ PARAGRAPH 1: Apology + Acknowledgment      │    │    │
│  │ ├────────────────────────────────────────────┤    │    │
│  │ │ PARAGRAPH 2: Reason + New Delivery Date    │    │    │
│  │ ├────────────────────────────────────────────┤    │    │
│  │ │ PARAGRAPH 3: 15% Discount Offer            │    │    │
│  │ ├────────────────────────────────────────────┤    │    │
│  │ │ CLOSING: Warm regards + Contact info       │    │    │
│  │ └────────────────────────────────────────────┘    │    │
│  └──────────────────────────────────────────────────┘    │
└──────────────────────────────────────────────────────────┘
```

---

## Prompt Type 2: Create Command

### Prompt
```
Create a weekly study schedule for a college student taking 5 courses:
- Data Structures (Mon/Wed)
- Calculus II (Tue/Thu)
- Physics (Mon/Wed/Fri)
- English Composition (Tue/Thu)
- Computer Networks (Fri)
Include study time, breaks, and review sessions.
```

### Expected Output
A detailed weekly schedule table with time blocks.

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────────┐
│                    WEEKLY STUDY SCHEDULE                          │
│                                                                   │
│  TIME    │ MON      │ TUE      │ WED      │ THU      │ FRI      │
│  ────────┼──────────┼──────────┼──────────┼──────────┼──────────│
│  8:00 AM │ Physics  │ Calculus │ Physics  │ Calculus │ Physics  │
│  ────────┼──────────┼──────────┼──────────┼──────────┼──────────│
│  10:00AM │ Data     │ English  │ Data     │ English  │ Computer │
│          │ Struct   │ Comp     │ Struct   │ Comp     │ Networks │
│  ────────┼──────────┼──────────┼──────────┼──────────┼──────────│
│  12:00PM │ ☕ LUNCH │ ☕ LUNCH │ ☕ LUNCH │ ☕ LUNCH │ ☕ LUNCH │
│  ────────┼──────────┼──────────┼──────────┼──────────┼──────────│
│  1:00 PM │ Study:   │ Study:   │ Study:   │ Study:   │ Review   │
│          │ Physics  │ Calculus │ Data St. │ English  │ All      │
│  ────────┼──────────┼──────────┼──────────┼──────────┼──────────│
│  3:00 PM │ 🏃 Break│ 🏃 Break│ 🏃 Break│ 🏃 Break│ 🏃 Break│
│  ────────┼──────────┼──────────┼──────────┼──────────┼──────────│
│  4:00 PM │ Review   │ Review   │ Review   │ Review   │ FREE     │
│          │ Session  │ Session  │ Session  │ Session  │ TIME     │
└──────────────────────────────────────────────────────────────────┘
```

---

## Prompt Type 3: List Command

### Prompt
```
List 8 effective strategies for improving memory retention while studying.
For each strategy, provide:
- Name of the technique
- How it works (1 sentence)
- Difficulty level (Easy/Medium/Hard)
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│            MEMORY RETENTION STRATEGIES                        │
│                                                               │
│  ┌─── EASY ────────────────────────────────────────────┐     │
│  │ 1. Spaced Repetition                                 │     │
│  │    Review material at increasing intervals            │     │
│  │ 2. Active Recall                                      │     │
│  │    Test yourself instead of re-reading                │     │
│  │ 3. Chunking                                           │     │
│  │    Break information into smaller groups              │     │
│  └──────────────────────────────────────────────────────┘     │
│                                                               │
│  ┌─── MEDIUM ──────────────────────────────────────────┐     │
│  │ 4. Mind Mapping                                       │     │
│  │    Create visual connections between concepts         │     │
│  │ 5. Feynman Technique                                  │     │
│  │    Explain concepts in simple terms                   │     │
│  │ 6. Interleaving                                       │     │
│  │    Mix different topics in one study session          │     │
│  └──────────────────────────────────────────────────────┘     │
│                                                               │
│  ┌─── HARD ────────────────────────────────────────────┐     │
│  │ 7. Method of Loci                                     │     │
│  │    Associate info with physical locations             │     │
│  │ 8. Elaborative Interrogation                          │     │
│  │    Ask "why" and "how" for every fact                 │     │
│  └──────────────────────────────────────────────────────┘     │
└──────────────────────────────────────────────────────────────┘
```

---

## Prompt Type 4: Generate Command

### Prompt
```
Generate a comparison table between REST API and GraphQL.
Include: architecture, data fetching, caching, learning curve,
performance, and best use cases.
Format as a structured table.
```

### Expected Visual Output
```
┌────────────────────────────────────────────────────────────────┐
│              REST API vs GraphQL COMPARISON                     │
│                                                                 │
│  ┌──────────────┬─────────────────┬─────────────────┐          │
│  │   Feature    │    REST API     │    GraphQL      │          │
│  ├──────────────┼─────────────────┼─────────────────┤          │
│  │ Architecture │ Multiple        │ Single          │          │
│  │              │ endpoints       │ endpoint        │          │
│  ├──────────────┼─────────────────┼─────────────────┤          │
│  │ Data Fetch   │ Over/Under      │ Exact data      │          │
│  │              │ fetching        │ requested       │          │
│  ├──────────────┼─────────────────┼─────────────────┤          │
│  │ Caching      │ HTTP caching    │ Complex,        │          │
│  │              │ built-in        │ needs setup     │          │
│  ├──────────────┼─────────────────┼─────────────────┤          │
│  │ Learning     │ ★★☆☆☆ Easy     │ ★★★★☆ Moderate │          │
│  │ Curve        │                 │                 │          │
│  ├──────────────┼─────────────────┼─────────────────┤          │
│  │ Performance  │ Multiple round  │ Single request  │          │
│  │              │ trips possible  │ for all data    │          │
│  ├──────────────┼─────────────────┼─────────────────┤          │
│  │ Best For     │ Simple CRUD     │ Complex, nested │          │
│  │              │ applications    │ data needs      │          │
│  └──────────────┴─────────────────┴─────────────────┘          │
└────────────────────────────────────────────────────────────────┘
```

---

## Prompt Type 5: Design Command

### Prompt
```
Design a database schema for an online bookstore application.
Include tables for: Users, Books, Orders, Reviews, and Categories.
Show relationships between tables.
```

### Expected Visual Output
```
┌────────────────────────────────────────────────────────────────┐
│              ONLINE BOOKSTORE DATABASE SCHEMA                   │
│                                                                 │
│  ┌──────────────┐     ┌──────────────┐     ┌──────────────┐   │
│  │    USERS     │     │    ORDERS    │     │   REVIEWS    │   │
│  ├──────────────┤     ├──────────────┤     ├──────────────┤   │
│  │ *user_id  PK │──┐  │ *order_id PK │  ┌──│ *review_id PK│   │
│  │  name        │  ├──│  user_id  FK │  │  │  user_id  FK │   │
│  │  email       │  │  │  book_id  FK │──┤  │  book_id  FK │   │
│  │  password    │  │  │  quantity    │  │  │  rating      │   │
│  │  address     │  │  │  total_price │  │  │  comment     │   │
│  │  created_at  │  │  │  order_date  │  │  │  created_at  │   │
│  └──────────────┘  │  └──────────────┘  │  └──────────────┘   │
│                    │                     │                      │
│                    │  ┌──────────────┐   │  ┌──────────────┐   │
│                    │  │    BOOKS     │   │  │  CATEGORIES  │   │
│                    │  ├──────────────┤   │  ├──────────────┤   │
│                    └──│ *book_id  PK │───┘  │ *cat_id   PK │   │
│                       │  title       │──────│  name        │   │
│                       │  author      │      │  description │   │
│                       │  price       │      │  parent_id   │   │
│                       │  isbn        │      └──────────────┘   │
│                       │  category_id │                          │
│                       └──────────────┘                          │
│                                                                 │
│  RELATIONSHIPS:                                                 │
│  Users ──1:N──> Orders    (One user, many orders)              │
│  Books ──1:N──> Orders    (One book in many orders)            │
│  Users ──1:N──> Reviews   (One user, many reviews)             │
│  Books ──1:N──> Reviews   (One book, many reviews)             │
│  Categories ──1:N──> Books (One category, many books)          │
└────────────────────────────────────────────────────────────────┘
```

---

## Action Verbs Cheat Sheet

```
┌───────────────────────────────────────────────────────┐
│          DIRECT INSTRUCTION ACTION VERBS               │
│                                                        │
│  ┌─────────┐  ┌─────────┐  ┌──────────┐  ┌────────┐ │
│  │  Write  │  │ Create  │  │   List   │  │ Build  │ │
│  └────┬────┘  └────┬────┘  └────┬─────┘  └───┬────┘ │
│       │            │            │             │       │
│  ┌─────────┐  ┌─────────┐  ┌──────────┐  ┌────────┐ │
│  │Generate │  │ Design  │  │ Explain  │  │Analyze │ │
│  └────┬────┘  └────┬────┘  └────┬─────┘  └───┬────┘ │
│       │            │            │             │       │
│  ┌─────────┐  ┌─────────┐  ┌──────────┐  ┌────────┐ │
│  │Compare  │  │Translate│  │Summarize │  │Convert │ │
│  └─────────┘  └─────────┘  └──────────┘  └────────┘ │
│                                                        │
│  TIP: Start every prompt with a strong action verb!    │
└───────────────────────────────────────────────────────┘
```

---

## Image Examples: What Gemini Nano Bana Would Generate

| Prompt | Expected Image Type | Description |
|--------|-------------------|-------------|
| "Design a logo for..." | Brand mockup | Clean vector-style logo with color palette and variations |
| "Create a schedule..." | Calendar/Grid | Color-coded weekly grid with time blocks and activities |
| "Generate a flowchart..." | Process diagram | Boxes and arrows showing sequential steps with decision points |
| "Build a wireframe..." | UI mockup | Grayscale layout showing page structure, buttons, and content areas |
| "Write a report on..." | Document layout | Formatted document with headers, sections, charts embedded |
