# Table & Data Extraction Prompts for Gemini Nano Bana

```
╔══════════════════════════════════════════════════════════════╗
║            TABLE & DATA EXTRACTION PROMPTS                   ║
╚══════════════════════════════════════════════════════════════╝
```

---

## Prompt 1: Table Extraction & Formatting

### Prompt
```
Extract all tables from this PDF document. For each table:
- Preserve column headers and row structure
- Convert to markdown table format
- Add data types for each column (string, number, date)
- Flag any cells with missing or unclear data
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│  TABLE 1: Quarterly Revenue (Page 4)                         │
│                                                               │
│  | Quarter | Revenue ($M) | Growth (%) | Region   |         │
│  |---------|-------------|------------|----------|          │
│  | Q1 2025 | 12.4        | 8.2        | NA       |         │
│  | Q2 2025 | 14.1        | 13.7       | NA       |         │
│  | Q3 2025 | 13.8        | -2.1       | NA       |         │
│  | Q4 2025 | 16.2        | 17.4       | NA       |         │
│                                                               │
│  Column Types: [string, number, number, string]              │
│  Missing Data: None detected                                 │
│  ─────────────────────────────────────────────               │
│  TABLE 2: Employee Distribution (Page 7)                     │
│                                                               │
│  | Department  | Headcount | Budget ($K) | Status  |        │
│  |------------|-----------|-------------|---------|         │
│  | Engineering | 142       | 8,500       | Active  |        │
│  | Marketing   | 58        | 3,200       | Active  |        │
│  | Sales       | 89        | ⚠ UNCLEAR  | Active  |        │
│                                                               │
│  ⚠ Flag: Row 3, Column 3 - value unclear in source PDF     │
└──────────────────────────────────────────────────────────────┘
```

---

## Prompt 2: Data Comparison from Multiple PDFs

### Prompt
```
I have 3 quarterly report PDFs. Extract the revenue figures from
each and create a comparison table showing:
- Quarter-over-quarter growth
- Year-over-year comparison
- Highlight the best and worst performing quarters
- Calculate averages and totals
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│  CROSS-DOCUMENT COMPARISON                                    │
│                                                               │
│  Revenue Comparison ($M)                                     │
│  ┌─────────┬────────┬────────┬────────┬─────────┐          │
│  │ Quarter │ 2023   │ 2024   │ 2025   │ YoY (%) │          │
│  ├─────────┼────────┼────────┼────────┼─────────┤          │
│  │ Q1      │  8.2   │ 10.1   │ 12.4   │ +22.8   │          │
│  │ Q2      │  9.1   │ 11.3   │ 14.1   │ +24.8 ▲ │          │
│  │ Q3      │  8.8   │ 10.9   │ 13.8   │ +26.6 ▲ │          │
│  │ Q4      │ 10.5   │ 13.2   │ 16.2   │ +22.7   │          │
│  ├─────────┼────────┼────────┼────────┼─────────┤          │
│  │ Total   │ 36.6   │ 45.5   │ 56.5   │ +24.2   │          │
│  │ Average │  9.15  │ 11.38  │ 14.13  │         │          │
│  └─────────┴────────┴────────┴────────┴─────────┘          │
│                                                               │
│  ▲ Best: Q3 2025 (+26.6% YoY)                               │
│  ▼ Worst: Q4 2023 baseline                                   │
└──────────────────────────────────────────────────────────────┘
```

---

## Image Examples

| Prompt | Expected Image Type | Description |
|--------|-------------------|-------------|
| Table extraction | Formatted markdown tables | Clean tables with color-coded data types and warning flags |
| Cross-document comparison | Comparison chart | Side-by-side bar chart with trend arrows and highlights |
