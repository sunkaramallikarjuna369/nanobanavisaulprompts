# Infographic Prompts for Gemini Nano Bana

```
╔══════════════════════════════════════════════════════════════╗
║               INFOGRAPHIC PROMPTS                             ║
╚══════════════════════════════════════════════════════════════╝
```

---

## Prompt 1: Technology Comparison Infographic

### Prompt
```
Create an infographic comparing 3 AI model architectures:
- Transformer (GPT, BERT)
- CNN (ResNet, EfficientNet)
- RNN (LSTM, GRU)

For each: show key stats, best use case, year introduced,
number of parameters (typical), and training time comparison.
Use icons and visual hierarchy.
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│  AI ARCHITECTURE COMPARISON INFOGRAPHIC                      │
│                                                               │
│  ┌──────────────────┐                                        │
│  │  TRANSFORMER      │  Year: 2017                           │
│  │  ╔══════════════╗ │  Params: 175B (GPT-3)                │
│  │  ║ Self-Attention║ │  Best for: Text, Code, Multimodal   │
│  │  ║  ↔ ↔ ↔ ↔ ↔  ║ │  Training: ████████████ (Expensive) │
│  │  ╚══════════════╝ │  Parallelizable: ✅ YES              │
│  └──────────────────┘                                        │
│                                                               │
│  ┌──────────────────┐                                        │
│  │  CNN              │  Year: 2012 (AlexNet)                 │
│  │  ┌┐┌┐┌┐          │  Params: 66M (ResNet-152)             │
│  │  │││││├──→ Pool   │  Best for: Images, Video             │
│  │  └┘└┘└┘          │  Training: ██████░░░░░░ (Moderate)    │
│  │  Conv Layers      │  Parallelizable: ✅ YES              │
│  └──────────────────┘                                        │
│                                                               │
│  ┌──────────────────┐                                        │
│  │  RNN/LSTM         │  Year: 1997 (LSTM)                    │
│  │  ●→●→●→●→●       │  Params: 10M (typical)                │
│  │  Sequential       │  Best for: Time series, Speech       │
│  │  Processing       │  Training: ████░░░░░░░░ (Slow/seq)   │
│  │                   │  Parallelizable: ❌ NO               │
│  └──────────────────┘                                        │
└──────────────────────────────────────────────────────────────┘
```

---

## Image Examples

| Prompt | Expected Image Type | Description |
|--------|-------------------|-------------|
| Architecture infographic | Vertical infographic | Three colored sections with architecture diagrams, stats, and comparison bars |
