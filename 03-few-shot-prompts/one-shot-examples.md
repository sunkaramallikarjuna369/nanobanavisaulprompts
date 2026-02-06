# One-Shot Example Prompts for Gemini Nano Bana

```
╔══════════════════════════════════════════════════════════════╗
║                 ONE-SHOT EXAMPLE PROMPTS                     ║
║                                                              ║
║  Show ONE example, then ask for a new output!                ║
║                                                              ║
║  ┌──────────┐    ┌──────────────┐    ┌──────────────────┐   ║
║  │ 1 Example│───>│  AI Learns   │───>│  New Output      │   ║
║  │ + Query  │    │  Pattern     │    │  Same Style      │   ║
║  └──────────┘    └──────────────┘    └──────────────────┘   ║
╚══════════════════════════════════════════════════════════════╝
```

---

## Prompt 1: Content Format Replication

### Prompt
```
Here is an example of a tech concept explanation card:

**Concept:** Blockchain
**One-liner:** A decentralized digital ledger that records transactions across many computers.
**Analogy:** Like a shared Google Doc where everyone can see edits but no one can delete history.
**Key Benefit:** Transparency and tamper-proof records.
**Difficulty:** ★★★★☆

Now create the same format for: Machine Learning
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│                  CONCEPT CARD: MACHINE LEARNING               │
│  ┌──────────────────────────────────────────────────────┐    │
│  │  CONCEPT: Machine Learning                            │    │
│  ├──────────────────────────────────────────────────────┤    │
│  │  ONE-LINER:                                           │    │
│  │  A subset of AI where systems learn from data to      │    │
│  │  make predictions without explicit programming.       │    │
│  ├──────────────────────────────────────────────────────┤    │
│  │  ANALOGY:                                             │    │
│  │  Like a child learning to recognize animals by        │    │
│  │  looking at thousands of pictures, not by reading     │    │
│  │  definitions.                                         │    │
│  ├──────────────────────────────────────────────────────┤    │
│  │  KEY BENEFIT:                                         │    │
│  │  Automates pattern discovery in massive datasets.     │    │
│  ├──────────────────────────────────────────────────────┤    │
│  │  DIFFICULTY: ★★★★☆                                   │    │
│  └──────────────────────────────────────────────────────┘    │
└──────────────────────────────────────────────────────────────┘
```

---

## Prompt 2: Visual Diagram Style

### Prompt
```
Example of how I want system architectures explained:

**System:** E-commerce Website
**Diagram:**
  [User Browser] --> [Load Balancer] --> [Web Server]
                                              |
                                         [Database]
**Components:** 4
**Data Flow:** User request → Load balanced → Served → Data retrieved

Now explain the same way for: Social Media Platform
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│          SOCIAL MEDIA PLATFORM ARCHITECTURE                   │
│                                                               │
│  ┌──────────┐    ┌──────────────┐    ┌──────────────┐       │
│  │   User   │───>│    CDN /     │───>│  Web Server  │       │
│  │  Mobile  │    │ Load Balancer│    │  (API Layer) │       │
│  │  App     │    └──────────────┘    └──────┬───────┘       │
│  └──────────┘                               │               │
│                                ┌────────────┼────────────┐  │
│                                ▼            ▼            ▼  │
│                          ┌──────────┐ ┌──────────┐ ┌──────┐│
│                          │  User DB │ │  Media   │ │Cache ││
│                          │(Postgres)│ │ Storage  │ │(Redis)│
│                          └──────────┘ │  (S3)    │ └──────┘│
│                                       └──────────┘          │
│                                                               │
│  COMPONENTS: 6                                               │
│  DATA FLOW: User post → CDN cached → API processes →         │
│             Media stored in S3 → Metadata in Postgres →      │
│             Feed cached in Redis → Delivered to followers     │
└──────────────────────────────────────────────────────────────┘
```

---

## Prompt 3: Code Documentation Style

### Prompt
```
Example documentation format:

Function: `sort_array(arr, order="asc")`
Purpose: Sorts an array in ascending or descending order
Input: arr (list of numbers), order (string: "asc" or "desc")
Output: Sorted list
Example:
  sort_array([3,1,2]) → [1,2,3]
  sort_array([3,1,2], "desc") → [3,2,1]
Complexity: O(n log n)

Now document this function the same way: `merge_dicts(dict1, dict2, strategy="overwrite")`
```

### Expected Visual Output
```
┌──────────────────────────────────────────────────────────────┐
│          FUNCTION DOCUMENTATION                               │
│                                                               │
│  ┌─ merge_dicts(dict1, dict2, strategy="overwrite") ──────┐ │
│  │                                                          │ │
│  │  PURPOSE: Merges two dictionaries into one using the     │ │
│  │  specified conflict resolution strategy                  │ │
│  │                                                          │ │
│  │  INPUT:                                                  │ │
│  │  ┌──────────┬────────┬──────────────────────────┐       │ │
│  │  │ dict1    │ dict   │ First dictionary          │       │ │
│  │  │ dict2    │ dict   │ Second dictionary         │       │ │
│  │  │ strategy │ string │ "overwrite", "keep",      │       │ │
│  │  │          │        │ "merge_lists"             │       │ │
│  │  └──────────┴────────┴──────────────────────────┘       │ │
│  │                                                          │ │
│  │  OUTPUT: Merged dictionary                               │ │
│  │                                                          │ │
│  │  EXAMPLES:                                               │ │
│  │  merge_dicts({"a":1}, {"b":2})                          │ │
│  │    → {"a":1, "b":2}                                     │ │
│  │                                                          │ │
│  │  merge_dicts({"a":1}, {"a":2}, "keep")                  │ │
│  │    → {"a":1}                                            │ │
│  │                                                          │ │
│  │  COMPLEXITY: O(n + m) where n,m = dict sizes            │ │
│  └──────────────────────────────────────────────────────────┘ │
└──────────────────────────────────────────────────────────────┘
```

---

## Image Examples

| Prompt | Expected Image Type | Description |
|--------|-------------------|-------------|
| Concept card | Styled info card | Rounded card with icon, gradient header, sections with dividers |
| Architecture | System diagram | Boxes with service names connected by labeled arrows, cloud icons |
| Code docs | Dark-themed doc card | Syntax-highlighted function signature with parameter table below |
