# Step-by-Step Reasoning Prompts for Gemini Nano Bana

```
╔══════════════════════════════════════════════════════════════╗
║              STEP-BY-STEP REASONING PROMPTS                  ║
║                                                              ║
║  Force the AI to show its work - like showing math steps!    ║
║                                                              ║
║  ┌────┐   ┌────┐   ┌────┐   ┌────┐   ┌──────────┐         ║
║  │ S1 │──>│ S2 │──>│ S3 │──>│ S4 │──>│ ANSWER   │         ║
║  └────┘   └────┘   └────┘   └────┘   └──────────┘         ║
╚══════════════════════════════════════════════════════════════╝
```

---

## Prompt 1: Mathematical Problem Solving

### Prompt
```
Solve this problem step by step, showing all your work:

A store offers a 25% discount on a laptop priced at $1,200.
Then there is an additional 10% student discount on the reduced price.
Finally, 8% sales tax is applied.
What is the final price?

Think through each step carefully before giving the answer.
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│           STEP-BY-STEP PRICE CALCULATION                     │
│                                                               │
│  STEP 1: Original Price                                      │
│  ┌───────────────────────────────┐                           │
│  │  Laptop Price = $1,200.00     │                           │
│  └───────────────┬───────────────┘                           │
│                  ▼                                            │
│  STEP 2: Apply 25% Store Discount                            │
│  ┌───────────────────────────────┐                           │
│  │  Discount = $1,200 x 0.25    │                           │
│  │          = $300.00            │                           │
│  │  New Price = $1,200 - $300    │                           │
│  │           = $900.00           │                           │
│  └───────────────┬───────────────┘                           │
│                  ▼                                            │
│  STEP 3: Apply 10% Student Discount                          │
│  ┌───────────────────────────────┐                           │
│  │  Discount = $900 x 0.10      │                           │
│  │          = $90.00             │                           │
│  │  New Price = $900 - $90       │                           │
│  │           = $810.00           │                           │
│  └───────────────┬───────────────┘                           │
│                  ▼                                            │
│  STEP 4: Apply 8% Sales Tax                                  │
│  ┌───────────────────────────────┐                           │
│  │  Tax = $810 x 0.08           │                           │
│  │     = $64.80                  │                           │
│  │  Final = $810 + $64.80        │                           │
│  │       = $874.80               │                           │
│  └───────────────┬───────────────┘                           │
│                  ▼                                            │
│  ┌─══════════════════════════════┐                           │
│  ║  FINAL ANSWER: $874.80       ║                           │
│  └─══════════════════════════════┘                           │
│                                                               │
│  SAVINGS BREAKDOWN:                                          │
│  ████████████████████ $300.00 (Store Discount)               │
│  ██████ $90.00 (Student Discount)                            │
│  Total Saved: $390.00 (32.5% off original!)                  │
└──────────────────────────────────────────────────────────────┘
```

---

## Prompt 2: Logical Reasoning

### Prompt
```
Think step by step to solve this logic puzzle:

Five friends - Alice, Bob, Carol, Dave, and Eve - sit in a row.
- Alice sits next to Bob
- Carol does not sit next to Dave
- Eve sits at one end
- Bob sits in the middle

What is the seating arrangement? Show your reasoning at each step.
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│              LOGIC PUZZLE: STEP-BY-STEP SOLUTION              │
│                                                               │
│  STEP 1: Place known positions                               │
│  ┌─────┬─────┬─────┬─────┬─────┐                           │
│  │  ?  │  ?  │ BOB │  ?  │  ?  │  (Bob is in middle)       │
│  └─────┴─────┴─────┴─────┴─────┘                           │
│                                                               │
│  STEP 2: Place Eve at one end                                │
│  ┌─────┬─────┬─────┬─────┬─────┐                           │
│  │ EVE │  ?  │ BOB │  ?  │  ?  │  (Eve at left end)        │
│  └─────┴─────┴─────┴─────┴─────┘                           │
│                                                               │
│  STEP 3: Alice must be next to Bob (seat 2 or 4)            │
│  ┌─────┬───────┬─────┬───────┬─────┐                       │
│  │ EVE │ ALICE │ BOB │   ?   │  ?  │  (Alice next to Bob)  │
│  └─────┴───────┴─────┴───────┴─────┘                       │
│                                                               │
│  STEP 4: Carol NOT next to Dave                              │
│  Remaining: Carol, Dave for seats 4 and 5                    │
│  If Dave=4, Carol=5: Dave next to Bob, Carol at end ✓        │
│  Carol is NOT next to Dave ✓                                 │
│                                                               │
│  ┌─────┬───────┬─────┬──────┬───────┐                      │
│  │ EVE │ ALICE │ BOB │ DAVE │ CAROL │                      │
│  └─────┴───────┴─────┴──────┴───────┘                      │
│    1       2      3      4       5                           │
│                                                               │
│  VERIFICATION:                                               │
│  ✓ Alice next to Bob (seats 2,3)                            │
│  ✓ Carol NOT next to Dave (seats 5,4 - wait, they ARE next) │
│                                                               │
│  CORRECTION - Try: Dave=5, Carol=4                           │
│  ┌─────┬───────┬─────┬───────┬──────┐                      │
│  │ EVE │ ALICE │ BOB │ CAROL │ DAVE │                      │
│  └─────┴───────┴─────┴───────┴──────┘                      │
│  ✓ Carol(4) next to Dave(5)? NO - they ARE adjacent!        │
│                                                               │
│  TRY: Alice on other side of Bob                             │
│  ┌─────┬──────┬─────┬───────┬───────┐                      │
│  │ EVE │ CAROL│ BOB │ ALICE │ DAVE  │                      │
│  └─────┴──────┴─────┴───────┴───────┘                      │
│  ✓ Alice next to Bob ✓                                      │
│  ✓ Carol NOT next to Dave ✓                                 │
│  ✓ Eve at end ✓                                             │
│  ✓ Bob in middle ✓                                          │
│                                                               │
│  FINAL ANSWER: Eve, Carol, Bob, Alice, Dave                  │
└──────────────────────────────────────────────────────────────┘
```

---

## Prompt 3: Scientific Analysis

### Prompt
```
Using step-by-step reasoning, explain why ice floats on water.
Start from molecular structure and work up to the observable phenomenon.
Show each logical step in your reasoning chain.
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────────┐
│           WHY DOES ICE FLOAT? (Chain of Reasoning)               │
│                                                                   │
│  STEP 1: Water Molecule Structure                                │
│  ┌─────────────────────────────────────────┐                     │
│  │     H       H                            │                     │
│  │      \     /        Water molecule        │                     │
│  │       O ← →         H₂O has a bent       │                     │
│  │                      shape (104.5°)       │                     │
│  │  Molecules are POLAR (+ and - ends)       │                     │
│  └──────────────────────┬──────────────────┘                     │
│                         ▼                                         │
│  STEP 2: Liquid Water Arrangement                                │
│  ┌─────────────────────────────────────────┐                     │
│  │  Liquid water: molecules move freely     │                     │
│  │  ○ ○ ○ ○ ○                               │                     │
│  │   ○ ○ ○ ○    Close together              │                     │
│  │  ○ ○ ○ ○ ○   Random arrangement          │                     │
│  │   ○ ○ ○ ○    Density: ~1.0 g/cm³        │                     │
│  └──────────────────────┬──────────────────┘                     │
│                         ▼                                         │
│  STEP 3: Ice Crystal Formation                                   │
│  ┌─────────────────────────────────────────┐                     │
│  │  Ice: Hydrogen bonds lock molecules      │                     │
│  │                                           │                     │
│  │   O───H···O───H···O                      │                     │
│  │   │         │         │                   │                     │
│  │   H···O───H···O───H                      │                     │
│  │                                           │                     │
│  │  Hexagonal crystal lattice               │                     │
│  │  MORE SPACE between molecules!            │                     │
│  │  Density: ~0.917 g/cm³                   │                     │
│  └──────────────────────┬──────────────────┘                     │
│                         ▼                                         │
│  STEP 4: Density Comparison                                      │
│  ┌─────────────────────────────────────────┐                     │
│  │  Ice density (0.917) < Water density (1.0)│                    │
│  │                                           │                     │
│  │  ████ Ice:   0.917 g/cm³                 │                     │
│  │  █████ Water: 1.000 g/cm³                │                     │
│  └──────────────────────┬──────────────────┘                     │
│                         ▼                                         │
│  STEP 5: Conclusion                                              │
│  ┌─════════════════════════════════════════─┐                    │
│  │  Less dense objects FLOAT on more dense   │                    │
│  │  liquids. Ice is ~8% less dense than      │                    │
│  │  water, so ICE FLOATS!                    │                    │
│  │                                           │                    │
│  │     ~~~~ICE~~~~                           │                    │
│  │  ~~~~~~~~~~~~~~~~~~  ← Water surface      │                    │
│  │  ~~~ WATER ~~~~~~~~                       │                    │
│  │  ~~~~~~~~~~~~~~~~~~                       │                    │
│  └─════════════════════════════════════════─┘                    │
└──────────────────────────────────────────────────────────────────┘
```

---

## Prompt 4: Business Decision Making

### Prompt
```
Walk me through the decision-making process step by step:

A small bakery owner is deciding whether to:
A) Open a second location
B) Expand the current location
C) Start an online delivery service

Current revenue: $500K/year
Available budget: $150K
Staff: 8 employees

Analyze each option with clear reasoning steps.
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────────┐
│            BUSINESS DECISION ANALYSIS                             │
│                                                                   │
│  STEP 1: Define Criteria                                         │
│  ┌──────────────────────────────────────┐                        │
│  │ Cost │ Risk │ Revenue Potential │ Time│                        │
│  └──────────────────────────────────────┘                        │
│                                                                   │
│  STEP 2: Analyze Each Option                                     │
│                                                                   │
│  OPTION A: New Location          OPTION B: Expand Current        │
│  ┌────────────────────┐         ┌────────────────────┐          │
│  │ Cost:    $120-200K  │         │ Cost:    $80-120K   │          │
│  │ Risk:    ★★★★☆ HIGH│         │ Risk:    ★★★☆☆ MED │          │
│  │ Revenue: +$200-350K │         │ Revenue: +$100-200K │          │
│  │ Time:    6-12 months│         │ Time:    3-6 months │          │
│  │ Staff:   +6 needed  │         │ Staff:   +2 needed  │          │
│  └────────────────────┘         └────────────────────┘          │
│                                                                   │
│  OPTION C: Online Delivery                                       │
│  ┌────────────────────┐                                          │
│  │ Cost:    $30-60K    │                                          │
│  │ Risk:    ★★☆☆☆ LOW │                                          │
│  │ Revenue: +$80-150K  │                                          │
│  │ Time:    1-3 months │                                          │
│  │ Staff:   +2 needed  │                                          │
│  └────────────────────┘                                          │
│                                                                   │
│  STEP 3: Score Matrix (1-5)                                      │
│  ┌──────────┬────────┬────────┬────────┐                        │
│  │ Criteria │ Opt A  │ Opt B  │ Opt C  │                        │
│  ├──────────┼────────┼────────┼────────┤                        │
│  │ Budget   │  ★★    │  ★★★   │ ★★★★★ │                        │
│  │ Risk     │  ★★    │  ★★★   │ ★★★★  │                        │
│  │ Revenue  │ ★★★★★  │  ★★★   │  ★★★  │                        │
│  │ Speed    │  ★★    │  ★★★   │ ★★★★★ │                        │
│  ├──────────┼────────┼────────┼────────┤                        │
│  │ TOTAL    │  13    │   15   │   20   │                        │
│  └──────────┴────────┴────────┴────────┘                        │
│                                                                   │
│  STEP 4: Recommendation                                          │
│  ┌─════════════════════════════════════════════════════─┐        │
│  ║  BEST CHOICE: Option C (Online Delivery)             ║        │
│  ║                                                       ║        │
│  ║  WHY: Lowest cost, fastest launch, within budget,    ║        │
│  ║  lowest risk. Can use profits to fund Option B later.║        │
│  ║                                                       ║        │
│  ║  STRATEGY: C now → B in Year 2 → A in Year 3        ║        │
│  └─════════════════════════════════════════════════════─┘        │
└──────────────────────────────────────────────────────────────────┘
```

---

## Prompt 5: Debugging Code

### Prompt
```
Debug this Python code step by step. Show your reasoning at each step:

def calculate_average(numbers):
    total = 0
    for i in range(len(numbers)):
        total += numbers[i]
    average = total / len(numbers)
    return average

result = calculate_average([])
print(result)

Walk through the execution line by line and identify the bug.
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│              CODE DEBUGGING: STEP-BY-STEP                    │
│                                                               │
│  STEP 1: Function called with empty list []                  │
│  ┌──────────────────────────────────────┐                    │
│  │  calculate_average([])               │                    │
│  │  numbers = []                         │                    │
│  └──────────────────┬───────────────────┘                    │
│                     ▼                                         │
│  STEP 2: total = 0  ✓ (No issue)                            │
│  ┌──────────────────────────────────────┐                    │
│  │  total = 0                            │                    │
│  └──────────────────┬───────────────────┘                    │
│                     ▼                                         │
│  STEP 3: Loop execution                                      │
│  ┌──────────────────────────────────────┐                    │
│  │  range(len([])) = range(0) = []      │                    │
│  │  Loop body NEVER executes            │                    │
│  │  total remains 0  ✓                  │                    │
│  └──────────────────┬───────────────────┘                    │
│                     ▼                                         │
│  STEP 4: Calculate average  ⚠ BUG FOUND!                    │
│  ┌──────────────────────────────────────┐                    │
│  │  average = total / len(numbers)      │                    │
│  │  average = 0 / len([])               │                    │
│  │  average = 0 / 0                     │                    │
│  │                                       │                    │
│  │  ╔══════════════════════════════╗    │                    │
│  │  ║ ZeroDivisionError:           ║    │                    │
│  │  ║ division by zero             ║    │                    │
│  │  ╚══════════════════════════════╝    │                    │
│  └──────────────────┬───────────────────┘                    │
│                     ▼                                         │
│  FIX:                                                         │
│  ┌──────────────────────────────────────┐                    │
│  │  def calculate_average(numbers):     │                    │
│  │      if not numbers:          # NEW  │                    │
│  │          return 0             # NEW  │                    │
│  │      total = 0                       │                    │
│  │      for i in range(len(numbers)):   │                    │
│  │          total += numbers[i]         │                    │
│  │      average = total / len(numbers)  │                    │
│  │      return average                  │                    │
│  └──────────────────────────────────────┘                    │
└──────────────────────────────────────────────────────────────┘
```

---

## Image Examples: What Gemini Nano Bana Would Generate

| Prompt | Expected Image Type | Description |
|--------|-------------------|-------------|
| Math step-by-step | Calculation flowchart | Vertical flow with each math operation in a box, arrows connecting steps, highlighted final answer |
| Logic puzzle | Grid/seating diagram | Color-coded seats with names, constraint checkmarks on the side |
| Scientific reasoning | Process diagram | Molecular diagrams transitioning through states with labeled arrows |
| Business decision | Decision matrix infographic | Colorful comparison cards with bar charts and a highlighted recommendation |
| Code debugging | Code trace visualization | Dark-themed code with highlighted lines, variable states shown alongside, bug marked in red |
