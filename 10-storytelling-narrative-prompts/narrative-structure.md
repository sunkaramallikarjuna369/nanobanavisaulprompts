# Narrative Structure Prompts for Gemini Nano Bana

```
╔══════════════════════════════════════════════════════════════╗
║              NARRATIVE STRUCTURE PROMPTS                      ║
╚══════════════════════════════════════════════════════════════╝
```

---

## Prompt 1: Hero's Journey for Tech Concepts

### Prompt
```
Explain the journey of a data packet traveling across the internet
using the Hero's Journey narrative structure:
- The Call: User clicks a link
- The Departure: Packet leaves the browser
- Trials: DNS lookup, routing through networks, firewalls
- The Ordeal: Packet loss, retransmission
- The Return: Response arrives back at the browser
Make it engaging and educational.
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│  THE HERO'S JOURNEY OF A DATA PACKET                         │
│                                                               │
│  ACT 1: THE CALL                                             │
│  User clicks "Search" → A tiny packet is born               │
│  Packet: {src: 192.168.1.5, dst: 142.250.80.46}            │
│       │                                                       │
│       ▼                                                       │
│  ACT 2: THE DEPARTURE                                        │
│  Packet leaves home (local network) → meets the Router       │
│  Router: "I'll send you to the ISP gateway"                  │
│       │                                                       │
│       ▼                                                       │
│  ACT 3: THE TRIALS                                           │
│  DNS Oracle: "142.250.80.46 = google.com"                    │
│  Firewall Guard: "Papers please... OK, you may pass"        │
│  15 hops across routers → each one closer to destination     │
│       │                                                       │
│       ▼                                                       │
│  ACT 4: THE ORDEAL                                           │
│  Packet #47 gets LOST in a congested router!                 │
│  TCP: "Packet 47 missing! Sending again!"                    │
│  Retransmission succeeds on attempt 2                        │
│       │                                                       │
│       ▼                                                       │
│  ACT 5: THE RETURN                                           │
│  Server responds → 200 OK → page renders                    │
│  Total journey: 47ms across 12,000 kilometers               │
│  User sees: Google search results                            │
└──────────────────────────────────────────────────────────────┘
```

---

## Image Examples

| Prompt | Expected Image Type | Description |
|--------|-------------------|-------------|
| Hero's journey | Illustrated path | Winding path with labeled stages, packet character traveling through network landmarks |
