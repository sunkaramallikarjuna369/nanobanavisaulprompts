# Knowledge Assessment Prompts for Gemini Nano Bana

```
╔══════════════════════════════════════════════════════════════╗
║            KNOWLEDGE ASSESSMENT PROMPTS                       ║
╚══════════════════════════════════════════════════════════════╝
```

---

## Prompt 1: Skill Level Assessment

### Prompt
```
Assess my knowledge level in Machine Learning. Ask me 5 questions
of increasing difficulty (beginner → advanced). Based on my answers,
rate my skill level and recommend a personalized learning path.

Question types:
1. Definition (beginner)
2. Application (intermediate)
3. Problem-solving (intermediate+)
4. Architecture design (advanced)
5. Research-level (expert)
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│  ML SKILL ASSESSMENT                                          │
│                                                               │
│  Q1 [Beginner]: What is the difference between               │
│  supervised and unsupervised learning?                        │
│  Your answer: ✅ Correct                                     │
│                                                               │
│  Q2 [Intermediate]: When would you use Random Forest         │
│  over Logistic Regression?                                   │
│  Your answer: ✅ Correct                                     │
│                                                               │
│  Q3 [Intermediate+]: How would you handle class              │
│  imbalance in a fraud detection dataset?                     │
│  Your answer: ⚠️ Partially correct                           │
│                                                               │
│  Q4 [Advanced]: Design a recommendation system               │
│  architecture for 10M users.                                 │
│  Your answer: ❌ Needs improvement                           │
│                                                               │
│  Q5 [Expert]: Explain attention mechanisms in                │
│  transformers and their computational complexity.            │
│  Your answer: ❌ Not attempted                               │
│                                                               │
│  ASSESSMENT RESULT:                                           │
│  Level: Intermediate (Score: 2.5/5)                          │
│  ████████████░░░░░░░░ 50%                                    │
│                                                               │
│  LEARNING PATH:                                               │
│  1. Review SMOTE and class imbalance techniques              │
│  2. Study system design for ML at scale                      │
│  3. Deep dive into Transformer architecture                  │
│  4. Practice on Kaggle competitions                          │
└──────────────────────────────────────────────────────────────┘
```

---

## Image Examples

| Prompt | Expected Image Type | Description |
|--------|-------------------|-------------|
| Skill assessment | Progress dashboard | Radar chart of skills with recommended learning path arrows |
