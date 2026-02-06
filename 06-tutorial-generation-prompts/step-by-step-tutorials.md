# Step-by-Step Tutorial Prompts for Gemini Nano Bana

```
╔══════════════════════════════════════════════════════════════╗
║             STEP-BY-STEP TUTORIAL PROMPTS                    ║
╚══════════════════════════════════════════════════════════════╝
```

---

## Prompt 1: Technology Setup Tutorial

### Prompt
```
Create a step-by-step tutorial for setting up a Python virtual 
environment and installing TensorFlow on Ubuntu. Include: 
prerequisites, each command with explanation, verification steps,
and common troubleshooting tips. Number each step clearly.
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│  TUTORIAL: TensorFlow Setup on Ubuntu                        │
│                                                               │
│  Prerequisites: Python 3.8+, pip, Ubuntu 20.04+             │
│                                                               │
│  Step 1 ─── Check Python Version                            │
│  ┌────────────────────────────────────────────┐              │
│  │ $ python3 --version                        │              │
│  │ Python 3.10.12                             │              │
│  └────────────────────────────────────────────┘              │
│                                                               │
│  Step 2 ─── Create Virtual Environment                      │
│  ┌────────────────────────────────────────────┐              │
│  │ $ python3 -m venv tf_env                   │              │
│  │ $ source tf_env/bin/activate               │              │
│  │ (tf_env) $                                 │              │
│  └────────────────────────────────────────────┘              │
│                                                               │
│  Step 3 ─── Install TensorFlow                              │
│  ┌────────────────────────────────────────────┐              │
│  │ (tf_env) $ pip install tensorflow          │              │
│  └────────────────────────────────────────────┘              │
│                                                               │
│  Step 4 ─── Verify Installation                             │
│  ┌────────────────────────────────────────────┐              │
│  │ >>> import tensorflow as tf                │              │
│  │ >>> print(tf.__version__)                  │              │
│  │ 2.15.0                                     │              │
│  └────────────────────────────────────────────┘              │
│                                                               │
│  ⚠️ TROUBLESHOOTING:                                        │
│  • "No module named pip" → sudo apt install python3-pip     │
│  • GPU not detected → Install CUDA toolkit first            │
└──────────────────────────────────────────────────────────────┘
```

---

## Prompt 2: Concept Explanation Tutorial

### Prompt
```
Create a tutorial explaining how REST APIs work. Structure it as:
1. What is a REST API? (simple definition)
2. HTTP Methods explained (GET, POST, PUT, DELETE)
3. Status codes cheat sheet
4. Build your first API call with curl
5. Common mistakes to avoid
Include code examples for each section.
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│  TUTORIAL: Understanding REST APIs                           │
│  ═══════════════════════════════════                         │
│                                                               │
│  1. WHAT IS REST?                                            │
│  REST = Representational State Transfer                      │
│  Client ──HTTP Request──> Server ──Response──> Client        │
│                                                               │
│  2. HTTP METHODS                                             │
│  ┌──────────┬─────────────────┬──────────────┐              │
│  │ Method   │ Action          │ Example      │              │
│  ├──────────┼─────────────────┼──────────────┤              │
│  │ GET      │ Read data       │ GET /users   │              │
│  │ POST     │ Create new      │ POST /users  │              │
│  │ PUT      │ Update existing │ PUT /users/1 │              │
│  │ DELETE   │ Remove          │ DELETE /u/1  │              │
│  └──────────┴─────────────────┴──────────────┘              │
│                                                               │
│  3. STATUS CODES                                             │
│  200 ✅ OK    201 ✅ Created   204 ✅ No Content            │
│  400 ❌ Bad   401 🔒 Unauth   404 🔍 Not Found             │
│  500 💥 Server Error                                         │
│                                                               │
│  4. YOUR FIRST API CALL                                      │
│  $ curl https://api.example.com/users                        │
│  Response: [{"id":1,"name":"Alice"},{"id":2,"name":"Bob"}]  │
└──────────────────────────────────────────────────────────────┘
```

---

## Image Examples

| Prompt | Expected Image Type | Description |
|--------|-------------------|-------------|
| Setup tutorial | Terminal screenshots | Dark terminal with numbered commands and colored output |
| REST API tutorial | Infographic | HTTP methods as colored cards with arrows showing request/response flow |
