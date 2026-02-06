# Pattern Matching Prompts for Gemini Nano Bana

```
╔══════════════════════════════════════════════════════════════╗
║                PATTERN MATCHING PROMPTS                       ║
║                                                              ║
║  Teach the AI to recognize and replicate complex patterns!   ║
║                                                              ║
║  Pattern: A→B, C→D, E→?  Answer: F                         ║
╚══════════════════════════════════════════════════════════════╝
```

---

## Prompt 1: Email Classification Pattern

### Prompt
```
Learn this email classification pattern:

Subject: "Your order has shipped!" → Category: Transactional
Subject: "50% off everything today!" → Category: Promotional
Subject: "Meeting at 3pm tomorrow" → Category: Calendar
Subject: "Please review the Q3 report" → Category: Action Required
Subject: "Welcome to our newsletter!" → Category: Onboarding

Now classify:
1. "Your password has been reset"
2. "Flash sale: Buy 1 Get 1 Free!"
3. "Sprint planning moved to Monday"
4. "Approve the budget proposal by Friday"
5. "Thanks for signing up! Here's your guide"
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│           EMAIL CLASSIFICATION RESULTS                        │
│                                                               │
│  PATTERN LEARNED:                                            │
│  ┌───────────────────┬─────────────────────┐                │
│  │ Keywords          │ Category            │                │
│  ├───────────────────┼─────────────────────┤                │
│  │ order, shipped    │ Transactional       │                │
│  │ off, sale, deal   │ Promotional         │                │
│  │ meeting, schedule │ Calendar            │                │
│  │ review, approve   │ Action Required     │                │
│  │ welcome, signup   │ Onboarding          │                │
│  └───────────────────┴─────────────────────┘                │
│                                                               │
│  CLASSIFICATIONS:                                            │
│  ┌─────────────────────────────────────────────────────┐    │
│  │ 1. "Password reset"     → [TRANSACTIONAL]    ████  │    │
│  │ 2. "Flash sale BOGO"    → [PROMOTIONAL]      ████  │    │
│  │ 3. "Planning moved"     → [CALENDAR]         ████  │    │
│  │ 4. "Approve budget"     → [ACTION REQUIRED]  ████  │    │
│  │ 5. "Thanks for signup"  → [ONBOARDING]       ████  │    │
│  └─────────────────────────────────────────────────────┘    │
└──────────────────────────────────────────────────────────────┘
```

---

## Prompt 2: Writing Style Pattern

### Prompt
```
Match these writing style transformations:

Formal: "We would like to inform you that the meeting has been rescheduled."
Casual: "Hey! Just a heads up - the meeting's been moved."

Formal: "Please find attached the quarterly financial report for your review."
Casual: "Here's the Q3 report - take a look when you get a chance!"

Formal: "We regret to inform you that your application has been unsuccessful."
Casual: ???

Transform the last formal sentence to casual style following the pattern.
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│           STYLE TRANSFORMATION PATTERN                        │
│                                                               │
│  PATTERN RULES DETECTED:                                     │
│  ┌──────────────────┬──────────────────────────┐            │
│  │ FORMAL           │ CASUAL                    │            │
│  ├──────────────────┼──────────────────────────┤            │
│  │ "We would like"  │ "Hey!" / "Just"          │            │
│  │ "Please find"    │ "Here's"                 │            │
│  │ "has been"       │ "'s been" / contractions │            │
│  │ "for your review"│ "take a look"            │            │
│  │ Long sentences   │ Short, punchy            │            │
│  └──────────────────┴──────────────────────────┘            │
│                                                               │
│  TRANSFORMATION:                                             │
│  ┌──────────────────────────────────────────────┐           │
│  │  FORMAL:                                      │           │
│  │  "We regret to inform you that your           │           │
│  │   application has been unsuccessful."          │           │
│  │           │                                    │           │
│  │           ▼  [TRANSFORM]                      │           │
│  │                                                │           │
│  │  CASUAL:                                       │           │
│  │  "Sorry, but your application didn't make     │           │
│  │   it this time. Better luck next round!"       │           │
│  └──────────────────────────────────────────────┘           │
└──────────────────────────────────────────────────────────────┘
```

---

## Image Examples

| Prompt | Expected Image Type | Description |
|--------|-------------------|-------------|
| Email classification | Category dashboard | Color-coded email icons sorted into labeled bins with confidence bars |
| Style transformation | Before/after comparison | Split panel showing formal text transforming into casual with highlighted changes |
| Data pattern | Scatter plot with clusters | Points grouped by pattern with labeled cluster boundaries |
