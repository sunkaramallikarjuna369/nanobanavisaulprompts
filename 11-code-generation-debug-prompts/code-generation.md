# Code Generation Prompts for Gemini Nano Bana

```
╔══════════════════════════════════════════════════════════════╗
║              CODE GENERATION PROMPTS                          ║
╚══════════════════════════════════════════════════════════════╝
```

---

## Prompt 1: Function Generation

### Prompt
```
Write a Python function called `retry_with_backoff` that:
- Takes a callable function and max_retries (default 3)
- Retries the function on exception with exponential backoff
- Backoff formula: 2^attempt seconds (1s, 2s, 4s, 8s...)
- Logs each retry attempt with the error message
- Returns the function result on success
- Raises the last exception after all retries exhausted
Include type hints and a usage example.
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│  GENERATED CODE                                               │
│                                                               │
│  import time                                                  │
│  import logging                                               │
│  from typing import Callable, TypeVar, Any                    │
│                                                               │
│  T = TypeVar('T')                                             │
│                                                               │
│  def retry_with_backoff(                                      │
│      func: Callable[..., T],                                  │
│      max_retries: int = 3,                                    │
│      *args: Any,                                              │
│      **kwargs: Any                                            │
│  ) -> T:                                                      │
│      last_exception = None                                    │
│      for attempt in range(max_retries):                       │
│          try:                                                  │
│              return func(*args, **kwargs)                      │
│          except Exception as e:                                │
│              last_exception = e                                │
│              wait = 2 ** attempt                               │
│              logging.warning(                                  │
│                  f"Attempt {attempt+1} failed: {e}. "         │
│                  f"Retrying in {wait}s..."                     │
│              )                                                 │
│              time.sleep(wait)                                  │
│      raise last_exception                                     │
│                                                               │
│  # Usage:                                                     │
│  result = retry_with_backoff(fetch_api_data, 3,               │
│                               url="https://api.example.com")  │
└──────────────────────────────────────────────────────────────┘
```

---

## Prompt 2: API Endpoint Generation

### Prompt
```
Generate a REST API endpoint using FastAPI for a user registration
system. Include:
- POST /register endpoint
- Pydantic model for request validation (email, password, name)
- Password hashing with bcrypt
- Duplicate email check
- Return user object without password
- Proper HTTP status codes and error responses
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│  API STRUCTURE                                                │
│                                                               │
│  POST /register                                              │
│  ┌────────────────┐    ┌──────────────┐   ┌──────────────┐ │
│  │ Request Body   │ →  │ Validation   │ → │ Hash Password│ │
│  │ {email, pass,  │    │ Pydantic     │   │ bcrypt       │ │
│  │  name}         │    │ checks       │   │              │ │
│  └────────────────┘    └──────────────┘   └──────┬───────┘ │
│                                                    │         │
│                         ┌──────────────┐   ┌──────▼───────┐ │
│                         │ Response 201 │ ← │ Save to DB   │ │
│                         │ {id, email,  │   │ Check dupe   │ │
│                         │  name}       │   │ email first  │ │
│                         └──────────────┘   └──────────────┘ │
│                                                               │
│  Error Responses:                                            │
│  409 → Email already exists                                  │
│  422 → Invalid input (Pydantic validation)                   │
│  500 → Server error                                          │
└──────────────────────────────────────────────────────────────┘
```

---

## Image Examples

| Prompt | Expected Image Type | Description |
|--------|-------------------|-------------|
| Function generation | Code editor screenshot | Dark theme IDE with syntax-highlighted Python code |
| API endpoint | Architecture flow | Request flow diagram with validation and response stages |
