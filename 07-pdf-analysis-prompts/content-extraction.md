# Content Extraction Prompts for Gemini Nano Bana

```
╔══════════════════════════════════════════════════════════════╗
║              PDF CONTENT EXTRACTION PROMPTS                   ║
╚══════════════════════════════════════════════════════════════╝
```

---

## Prompt 1: Structured Data Extraction

### Prompt
```
I have a PDF research paper. Extract the following in structured format:
- Title
- Authors (as a list)
- Abstract (full text)
- Key findings (bullet points)
- Methodology (brief summary)
- Conclusion (2-3 sentences)
- References count

Format the output as a JSON object.
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│  EXTRACTED DOCUMENT STRUCTURE                                │
│                                                               │
│  {                                                            │
│    "title": "Attention Is All You Need",                     │
│    "authors": [                                               │
│      "Vaswani, A.", "Shazeer, N.", "Parmar, N."             │
│    ],                                                         │
│    "abstract": "The dominant sequence transduction...",      │
│    "key_findings": [                                          │
│      "Transformer outperforms RNNs on translation",          │
│      "Self-attention enables parallelization",                │
│      "Achieves 28.4 BLEU on EN-DE translation"              │
│    ],                                                         │
│    "methodology": "Multi-head self-attention with...",       │
│    "conclusion": "We presented the Transformer...",          │
│    "references_count": 42                                     │
│  }                                                            │
│                                                               │
│  ┌──────────┐  ┌──────────┐  ┌──────────┐  ┌──────────┐   │
│  │ Title    │→ │ Authors  │→ │ Abstract │→ │ Findings │   │
│  │ ✅       │  │ ✅       │  │ ✅       │  │ ✅       │   │
│  └──────────┘  └──────────┘  └──────────┘  └──────────┘   │
└──────────────────────────────────────────────────────────────┘
```

---

## Prompt 2: Invoice/Receipt Extraction

### Prompt
```
Extract all financial data from this invoice PDF:
- Vendor name and address
- Invoice number and date
- Line items (description, quantity, unit price, total)
- Subtotal, tax, and grand total
- Payment terms

Present as a formatted table.
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│  INVOICE EXTRACTION RESULT                                    │
│                                                               │
│  Vendor: TechCorp Solutions                                  │
│  Invoice #: INV-2025-0042    Date: 2025-01-15               │
│                                                               │
│  ┌──────────────────┬─────┬──────────┬───────────┐          │
│  │ Description      │ Qty │ Unit ($) │ Total ($) │          │
│  ├──────────────────┼─────┼──────────┼───────────┤          │
│  │ Cloud Hosting    │  12 │   99.00  │  1,188.00 │          │
│  │ API Calls (10K)  │   5 │   25.00  │    125.00 │          │
│  │ Support Plan     │   1 │  200.00  │    200.00 │          │
│  ├──────────────────┼─────┼──────────┼───────────┤          │
│  │ Subtotal         │     │          │  1,513.00 │          │
│  │ Tax (8%)         │     │          │    121.04 │          │
│  │ TOTAL            │     │          │  1,634.04 │          │
│  └──────────────────┴─────┴──────────┴───────────┘          │
│                                                               │
│  Payment Terms: Net 30 days                                  │
└──────────────────────────────────────────────────────────────┘
```

---

## Image Examples

| Prompt | Expected Image Type | Description |
|--------|-------------------|-------------|
| Research paper extraction | Structured JSON card | Color-coded fields extracted from document with confidence indicators |
| Invoice extraction | Formatted table | Clean invoice replica with highlighted extracted fields |
