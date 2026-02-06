# Conversational Flow Prompts for Gemini Nano Bana

```
╔══════════════════════════════════════════════════════════════╗
║            CONVERSATIONAL FLOW PROMPTS                        ║
╚══════════════════════════════════════════════════════════════╝
```

---

## Prompt 1: Multi-Turn Technical Support

### Prompt
```
Act as a technical support chatbot for a cloud platform. Guide 
the user through diagnosing why their deployment failed. Ask one 
question at a time, wait for the response, then proceed to the 
next diagnostic step. Follow this flow:
1. Ask which service they're deploying to
2. Ask for the error message
3. Suggest a diagnostic command
4. Based on output, provide the fix
Keep responses under 3 sentences each.
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│  CONVERSATION FLOW                                            │
│                                                               │
│  Bot: Which service are you deploying to?                    │
│  ┌────────────────────────────────────────────┐              │
│  │ User: AWS Lambda                           │              │
│  └────────────────────────────────────────────┘              │
│          │                                                    │
│          ▼                                                    │
│  Bot: What error message are you seeing?                     │
│  ┌────────────────────────────────────────────┐              │
│  │ User: "Runtime.ImportModuleError"          │              │
│  └────────────────────────────────────────────┘              │
│          │                                                    │
│          ▼                                                    │
│  Bot: Run `pip install -t ./package -r requirements.txt`     │
│       and re-zip your deployment package. This error means   │
│       dependencies aren't bundled with your code.            │
│  ┌────────────────────────────────────────────┐              │
│  │ User: That fixed it! Thanks!               │              │
│  └────────────────────────────────────────────┘              │
│          │                                                    │
│          ▼                                                    │
│  Bot: Glad it's resolved! For future deployments,            │
│       consider using Lambda Layers for shared deps.          │
└──────────────────────────────────────────────────────────────┘
```

---

## Prompt 2: Socratic Teaching Conversation

### Prompt
```
Teach me about recursion using the Socratic method. Don't explain
it directly. Instead, ask guiding questions that lead me to 
understand the concept myself. Start with something I already 
know (like looking up a word in a dictionary), then build toward
the programming concept. Maximum 5 question-answer exchanges.
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│  SOCRATIC DIALOGUE                                            │
│                                                               │
│  Q1: When you look up "happy" in a dictionary and it says    │
│      "see: joyful", what do you do next?                     │
│  A1: I look up "joyful"                                      │
│          │                                                    │
│  Q2: And if "joyful" says "see: glad"?                       │
│  A2: I keep looking up words until I find a real definition  │
│          │                                                    │
│  Q3: What would happen if every word just pointed to another │
│      word, forever?                                          │
│  A3: I'd never find the answer - infinite loop!              │
│          │                                                    │
│  Q4: So what does a dictionary need to work?                 │
│  A4: At least one word must have an actual definition!       │
│          │                                                    │
│  Q5: In programming, a function that calls itself is called  │
│      "recursive". What's the equivalent of that "actual      │
│      definition" that stops the chain?                       │
│  A5: A base case!                                            │
│          │                                                    │
│  ✅ You just discovered recursion!                           │
│     Function calls itself → needs a base case to stop       │
└──────────────────────────────────────────────────────────────┘
```

---

## Image Examples

| Prompt | Expected Image Type | Description |
|--------|-------------------|-------------|
| Tech support flow | Chat bubble sequence | Alternating colored chat bubbles with arrows showing conversation progression |
| Socratic teaching | Question tree | Branching question-answer tree leading to the "aha" moment at the bottom |
