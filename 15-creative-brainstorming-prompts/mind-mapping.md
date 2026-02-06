# Mind Mapping Prompts for Gemini Nano Bana

```
╔══════════════════════════════════════════════════════════════╗
║               MIND MAPPING PROMPTS                            ║
╚══════════════════════════════════════════════════════════════╝
```

---

## Prompt 1: Topic Exploration Mind Map

### Prompt
```
Create a mind map for the topic "Cloud Computing".
Start from the center concept and branch into:
- 4 main branches (major subtopics)
- 3 sub-branches per main branch
- 2 leaf nodes per sub-branch
Use visual hierarchy to show depth levels.
Include connections between related leaf nodes across branches.
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│                        MIND MAP                               │
│                                                               │
│                    ┌─ AWS                                     │
│              ┌─ Providers ─┤─ Azure                          │
│              │     └─ GCP                                     │
│              │                                                │
│        ┌─ IaaS ─┤─ Compute ─┬─ VMs                          │
│        │     │  └─ Storage ─┼─ Block                         │
│        │     │              └─ Object ·····→(links to        │
│        │     │                               Data Lakes)     │
│  CLOUD │                                                      │
│COMPUTING┤     ┌─ Containers ─┬─ Docker                       │
│        │     │              └─ Kubernetes                     │
│        ├─ PaaS ─┤─ Serverless ─┬─ Lambda                    │
│        │     │               └─ Functions                    │
│        │     └─ Databases ─┬─ Managed SQL                    │
│        │                   └─ NoSQL                           │
│        │                                                      │
│        │     ┌─ Email ─┬─ Gmail API                          │
│        ├─ SaaS ─┤─ CRM ─┴─ Salesforce                       │
│        │     └─ Collab ─┬─ Slack                             │
│        │                └─ Teams                              │
│        │                                                      │
│        │     ┌─ Encryption ─┬─ At rest                       │
│        └─ Security ─┤─ IAM ─┴─ RBAC                         │
│              └─ Compliance ─┬─ GDPR                          │
│                             └─ SOC2                           │
└──────────────────────────────────────────────────────────────┘
```

---

## Prompt 2: Problem Decomposition Map

### Prompt
```
Break down this complex problem into a mind map:
"Why is our web application slow?"

Create branches for each possible cause category.
For each leaf node, add a diagnostic action.
Mark the most likely causes with priority indicators.
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│                  WHY IS THE APP SLOW?                         │
│                                                               │
│  ┌─ Frontend ──┬─ Large bundle size → Run webpack-analyzer  │
│  │             ├─ No lazy loading → Audit route splits       │
│  │             └─ Render blocking → Check Lighthouse  [!!]  │
│  │                                                            │
│  ├─ Backend ───┬─ N+1 queries → Enable query logging  [!!] │
│  │             ├─ No caching → Add Redis layer              │
│  │             └─ Sync operations → Profile with APM        │
│  │                                                            │
│  ├─ Database ──┬─ Missing indexes → Run EXPLAIN  [!!!]     │
│  │             ├─ Full table scans → Check slow query log   │
│  │             └─ Connection pool → Monitor pool usage      │
│  │                                                            │
│  ├─ Network ───┬─ No CDN → Check TTFB by region            │
│  │             ├─ Large payloads → Enable compression       │
│  │             └─ DNS latency → Measure DNS resolution      │
│  │                                                            │
│  └─ Infra ─────┬─ Undersized servers → Check CPU/RAM       │
│                ├─ No auto-scaling → Review scaling rules    │
│                └─ Region distance → Add edge locations      │
│                                                               │
│  [!!!] = Most likely cause   [!!] = Probable   [!] = Check  │
└──────────────────────────────────────────────────────────────┘
```

---

## Image Examples

| Prompt | Expected Image Type | Description |
|--------|-------------------|-------------|
| Topic mind map | Radial diagram | Central node with color-coded branches radiating outward with decreasing node sizes |
| Problem decomposition | Tree diagram | Root cause tree with priority heat coloring (red=likely, yellow=possible) |
