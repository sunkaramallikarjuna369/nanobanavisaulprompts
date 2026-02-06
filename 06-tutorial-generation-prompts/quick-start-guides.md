# Quick Start Guide Prompts for Gemini Nano Bana

```
╔══════════════════════════════════════════════════════════════╗
║               QUICK START GUIDE PROMPTS                      ║
╚══════════════════════════════════════════════════════════════╝
```

---

## Prompt 1: Framework Quick Start

### Prompt
```
Create a 5-minute quick start guide for FastAPI. Include only the
essential steps: install, create a minimal app, run it, and test
one endpoint. No extras - just the fastest path to "Hello World".
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│  FastAPI in 5 Minutes                                        │
│  ━━━━━━━━━━━━━━━━━━━                                        │
│                                                               │
│  1. Install          $ pip install fastapi uvicorn           │
│                                                               │
│  2. Create app.py    from fastapi import FastAPI             │
│                       app = FastAPI()                         │
│                       @app.get("/")                           │
│                       def read_root():                        │
│                           return {"message": "Hello World"}  │
│                                                               │
│  3. Run              $ uvicorn app:app --reload              │
│                                                               │
│  4. Test             Open http://localhost:8000               │
│                       Docs at http://localhost:8000/docs      │
│                                                               │
│  ✅ Done! You have a running API in under 5 minutes.        │
└──────────────────────────────────────────────────────────────┘
```

---

## Prompt 2: Tool Quick Start

### Prompt
```
Create a quick start guide for Docker. Cover: install Docker,
pull an image, run a container, and verify it's working.
Maximum 4 steps, each with one command.
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│  Docker Quick Start                                          │
│                                                               │
│  Step 1 ──▶ Install                                         │
│  $ curl -fsSL https://get.docker.com | sh                    │
│                                                               │
│  Step 2 ──▶ Pull Image                                      │
│  $ docker pull nginx:latest                                  │
│                                                               │
│  Step 3 ──▶ Run Container                                   │
│  $ docker run -d -p 8080:80 nginx                            │
│                                                               │
│  Step 4 ──▶ Verify                                          │
│  $ curl http://localhost:8080                                 │
│  → Welcome to nginx!                                         │
└──────────────────────────────────────────────────────────────┘
```

---

## Image Examples

| Prompt | Expected Image Type | Description |
|--------|-------------------|-------------|
| FastAPI quick start | Terminal + browser split | Left: terminal with commands, Right: browser showing JSON response |
| Docker quick start | Sequential command cards | Numbered cards with terminal commands and expected outputs |
