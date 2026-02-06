# Dashboard Design Prompts for Gemini Nano Bana

```
╔══════════════════════════════════════════════════════════════╗
║              DASHBOARD DESIGN PROMPTS                         ║
╚══════════════════════════════════════════════════════════════╝
```

---

## Prompt 1: KPI Dashboard Layout

### Prompt
```
Design a real-time monitoring dashboard for a SaaS application.
Include these KPI sections:
- Active users (current count + 24h trend)
- API response time (p50, p95, p99)
- Error rate (% with color coding)
- Revenue today vs target
- Server health (CPU, memory, disk)
Show the dashboard layout with widget positions.
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│  SaaS MONITORING DASHBOARD                                    │
│                                                               │
│  ┌──────────────┐ ┌──────────────┐ ┌──────────────┐         │
│  │ ACTIVE USERS │ │ ERROR RATE   │ │ REVENUE      │         │
│  │   12,847     │ │   0.12%      │ │  $8,420      │         │
│  │   ▲ +12%     │ │   🟢 Normal  │ │  Target:$10K │         │
│  │   ▁▂▃▄▅▆▇█  │ │   ▁▁▁▂▁▁▁▁  │ │  ████████░░  │         │
│  └──────────────┘ └──────────────┘ └──────────────┘         │
│                                                               │
│  ┌─────────────────────────────────────────────────┐         │
│  │ API RESPONSE TIME (ms)                          │         │
│  │ p50: 45ms  │  p95: 120ms  │  p99: 380ms       │         │
│  │ ▂▂▃▂▂▃▂▂▂▃▄▃▂▂▂▃▂▂▂▂▃▂▂▂▃▂▂▂▂▃▂▂▂▃▂▂▂▂▂▂▂  │         │
│  └─────────────────────────────────────────────────┘         │
│                                                               │
│  ┌──────────────┐ ┌──────────────┐ ┌──────────────┐         │
│  │ CPU          │ │ MEMORY       │ │ DISK         │         │
│  │   42%        │ │   68%        │ │   31%        │         │
│  │ ████░░░░░░░░ │ │ ████████░░░░ │ │ ████░░░░░░░░ │         │
│  │ 🟢 Healthy   │ │ 🟡 Watch     │ │ 🟢 Healthy   │         │
│  └──────────────┘ └──────────────┘ └──────────────┘         │
└──────────────────────────────────────────────────────────────┘
```

---

## Image Examples

| Prompt | Expected Image Type | Description |
|--------|-------------------|-------------|
| KPI dashboard | Dark-themed dashboard | Grafana-style dashboard with real-time charts, gauges, and sparklines |
