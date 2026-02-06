# Dynamic / Interactive Visual Prompts

Use these prompts with Gemini's Dynamic View to generate interactive UI experiences.

---

## 1. Interactive Professor Whiteboard

```
Using dynamic view, transform this PDF into an interactive professor-style whiteboard dashboard.

Build:
- A main whiteboard canvas with diagrams, arrows, boxes, and short captions
- A left sidebar with clickable bullets for each major section of the PDF
- When I click a bullet, highlight the related region on the whiteboard and show a 2-3 line summary below
- Color highlights to separate definitions, examples, and key formulas

Goal: Make it feel like a live lecture board I can explore.
```

**Example:** Input: Google Cloud PDF → Output: Interactive whiteboard with Compute/Storage/Networking sections, clickable sidebar, highlighted regions on click

---

## 2. Interactive Infographic

```
Using dynamic view, convert this PDF into an interactive infographic interface.

Layout:
- Top hero with title + 3-4 big-number stat cards
- Middle section with an interactive chart (bar/pie/flow)
- Bottom section with collapsible "Details", "Methods", "Limitations" cards

Allow hover/tap on visual elements (bars, segments, icons) to reveal underlying values or short explanations.
```

**Example:** Input: Annual Report PDF → Output: Dashboard with KPI cards, hoverable chart segments, expandable detail cards

---

## 3. Interactive Mind Map

```
Using dynamic view, turn this academic PDF into an interactive concept map.

Requirements:
- Core idea in the center node
- Branch nodes for subtopics around it
- Clicking a node opens a side panel with 2-3 bullet insights and key formulas/definitions
- Color clusters for theory, experiments, results

Designed so I can navigate the paper by clicking nodes instead of reading linearly.
```

**Example:** Input: Research Paper → Output: Central node with clickable branches, side panel with details on click

---

## 4. Interactive Step-by-Step Guide

```
Using dynamic view, convert this PDF into an interactive step-by-step visual guide.

Build:
- Numbered steps across the top (Step 1, Step 2, ...) as clickable chips
- Main panel below showing each step with a diagram/screenshot-style box and arrows
- A progress indicator showing which step I'm on

Goal: Make it easy for a beginner to follow the procedure visually.
```

**Example:** Input: Setup Guide → Output: Clickable step chips, visual main panel, progress bar

---

## 5. Interactive Timeline

```
Using dynamic view, transform this PDF into an interactive timeline.

Features:
- Horizontal or vertical timeline with dates and milestones
- Clicking a milestone opens a card with summary, image/icon, and key data
- Color-code milestones by category (e.g., tech, policy, events)
- Optional zoom controls for focusing on specific time ranges
```

**Example:** Input: History Document → Output: Zoomable timeline with clickable milestone cards

---

## 6. Flowchart Explorer

```
Using dynamic view, convert this process description into an interactive flowchart explorer.

UI:
- Central flowchart canvas with process boxes and decision diamonds
- Scroll/zoom if needed
- Clicking a step highlights it and opens a right-hand panel with "What happens here", "Inputs", "Outputs", and "Common mistakes"
- Success paths in green, error paths in red

Prefer compact labels on the diagram; longer text goes into the side panel.
```

**Example:** Input: Order Processing Text → Output: Clickable flowchart with detail panels per step

---

## 7. System Architecture View

```
Using dynamic view, turn this text into an interactive system architecture view.

Include:
- Boxes for frontend, backend, databases, external services
- Labeled arrows for API calls and data flows
- A toggle or tabs to switch between "Logical View" and "Deployment View"
- On click, each component shows a small card with tech stack, responsibilities, and scaling notes.
```

**Example:** Input: Architecture Description → Output: Toggleable architecture diagram with clickable component cards

---

## 8. Swimlane Process Diagram

```
Using dynamic view, convert this process into a swimlane diagram.

Layout:
- Horizontal lanes for each actor (e.g., Customer, System, Support)
- Process boxes in each lane connected with arrows
- Clicking any box shows an inline popup with a 1-2 sentence description and inputs/outputs
- Color backgrounds or badges per lane to distinguish actors.
```

**Example:** Input: Support Workflow → Output: Color-coded actor lanes with clickable process boxes

---

## 9. Interactive Decision Matrix

```
Using dynamic view, turn this decision-making text into an interactive 2x2 decision matrix.

Features:
- X and Y axes labeled from the text (e.g., Impact vs Effort)
- Each option represented as a clickable bubble in the quadrant
- Hover or tap shows a short explanation and pros/cons
- Optional filter to hide/show specific groups of options.
```

**Example:** Input: Project Prioritization → Output: 2x2 grid with hoverable/filterable option bubbles

---

## 10. Interactive Data Flow

```
Using dynamic view, convert this process description into an interactive data flow diagram.

Elements:
- External entities as rectangles
- Processes as circles
- Data stores as open-ended rectangles
- Arrows showing data movement

Clicking on any element opens a panel with "Description", "Inputs", "Outputs", and "Risks".
```

**Example:** Input: Payment System → Output: Clickable DFD with detail panels per element

---

## 11. Execution Tracer

```
Using dynamic view, turn this code into an interactive execution tracer.

UI:
- Left pane: code with syntax highlighting
- Right pane: flow diagram or call stack that updates as execution steps change
- Next/Previous buttons to step through execution
- Current line in the code and current node in the diagram highlighted in sync

For recursion, show the call stack as a vertical stack of frames.
```

**Example:** Input: Sorting Algorithm → Output: Synced code + visual execution with step controls

---

## 12. Data Structure Visualizer

```
Using dynamic view, convert this data structure code into an interactive visualizer.

Features:
- Visual representation of nodes (e.g., linked list nodes as boxes with arrows)
- Controls to step through operations (insert, delete, search)
- As I step, animate changes to the structure (e.g., pointer updates)
- Short text panel describing what just happened at each step.
```

**Example:** Input: Binary Tree Code → Output: Animated tree with insert/delete/search step controls

---

## 13. UML Class Explorer

```
Using dynamic view, turn this object-oriented code into an interactive UML class explorer.

Include:
- Class boxes with attributes and methods
- Inheritance and association lines
- Clicking a class opens a side panel with method descriptions, key responsibilities, and example usage
- Filter or search bar to highlight a specific class or relationship.
```

**Example:** Input: OOP Python Code → Output: Searchable UML diagram with clickable class panels

---

## 14. API Sequence Diagram

```
Using dynamic view, convert these API interactions into an interactive sequence diagram.

UI:
- Vertical lifelines for each actor/service (Client, API, DB, etc.)
- Arrows for requests and responses
- Clicking an arrow shows payload examples, status codes, and typical errors
- Zoom or collapse repeated patterns (e.g., polling loops).
```

**Example:** Input: REST API Flow → Output: Sequence diagram with clickable arrows showing payloads

---

## 15. Algorithm Walkthrough

```
Using dynamic view, transform this algorithm into a step-by-step interactive walkthrough.

Elements:
- Pseudocode panel
- Visual panel (e.g., array, graph) updated at each step
- Slider or Next/Prev buttons to move through the algorithm
- At each step, highlight the changed elements and show a one-line explanation.
```

**Example:** Input: Dijkstra's Algorithm → Output: Visual graph with slider stepping through shortest path discovery

---

## 16. KPI Dashboard

```
Using dynamic view, transform this dataset into an interactive KPI dashboard.

Layout:
- Top row: 3-4 KPI cards (total, average, growth rate) with colored trend arrows
- Middle: main chart (line or bar) with filters for date range and category
- Right: filter panel with dropdowns/checkboxes
- Bottom: table that updates to show only data matching current filters

Clicking a chart element (bar/point) should filter the table to related records.
```

**Example:** Input: Sales Data → Output: Filterable dashboard with linked chart and table

---

## 17. Interactive Funnel

```
Using dynamic view, turn this conversion data into an interactive funnel.

Design:
- Funnel stages stacked vertically with widths proportional to counts
- Each stage clickable to show:
  - count
  - conversion % from previous stage
  - short text on typical reasons for drop-off
- Optional toggle to compare two time periods (e.g., last month vs this month) using side-by-side funnels.
```

**Example:** Input: Marketing Funnel Data → Output: Clickable funnel with comparison toggle

---

## 18. Geo Map View

```
Using dynamic view, convert this geo-tagged dataset into an interactive map view.

Features:
- Map with markers or bubbles sized by magnitude (e.g., revenue, users)
- Color code by category/region
- Hover tooltip with key fields (name, value, last updated)
- Filter panel to limit by region, category, or value range.
```

**Example:** Input: Store Locations CSV → Output: Filterable map with sized/colored markers

---

## 19. Correlation Heatmap

```
Using dynamic view, turn this correlation matrix into an interactive heatmap.

UI:
- Grid of cells colored by correlation strength
- Hover on a cell shows the exact value and variable pair
- Option to sort rows/columns by correlation with a selected variable
- Toggle to show only strong positive/negative correlations.
```

**Example:** Input: Feature Correlation Matrix → Output: Sortable, filterable heatmap with tooltips

---

## 20. Time-Series Explorer

```
Using dynamic view, convert this time-series data into an interactive timeline explorer.

Features:
- Main line chart with pan/zoom on the x-axis
- Brush control or mini-chart below for selecting a time window
- Hover tooltips with values and annotations for key events
- Filter to toggle different series on/off (e.g., revenue, users, churn).
```

**Example:** Input: Monthly Metrics → Output: Zoomable chart with series toggles and event annotations

---

## 21. Study Board

```
Using dynamic view, convert these notes into an interactive study board.

Columns:
- Definitions
- Examples
- Pitfalls
- Practice Questions

Each item should be a card that expands on click. Include a "Mark as learned" toggle per card and a progress bar at the top showing % learned.
```

**Example:** Input: Biology Notes → Output: 4-column board with expandable cards and progress tracking

---

## 22. Interactive Cheat Sheet

```
Using dynamic view, turn these notes into an interactive visual cheat sheet.

Layout:
- Sections for "Formulas", "Key Ideas", "Common Mistakes"
- Within each section, small cards with:
  - formula or concept
  - 1-2 line explanation
  - tiny example
- Hover over any formula to highlight where it's commonly used (e.g., tag badges like 'probability', 'geometry').
```

**Example:** Input: Statistics Formulas → Output: Sectioned cheat sheet with hoverable formula cards

---

## 23. Flashcard Carousel

```
Using dynamic view, transform these notes into an interactive flashcard carousel.

Features:
- Card view with question on front, answer on back (flip on click)
- Buttons for "I know this" / "I don't know this"
- Simple spaced-repetition style: show unknown cards more frequently in the session
- Progress indicator for cards reviewed in this session.
```

**Example:** Input: Vocabulary List → Output: Flippable cards with "know/don't know" buttons and progress bar

---

## 24. Concept Relationship Map

```
Using dynamic view, convert these notes into an interactive concept relationship map.

UI:
- Nodes for key terms
- Labeled edges for relationships (e.g., "causes", "is a type of")
- Clicking a node shows its definition and 1-2 examples
- Optional search box to jump to a specific concept.
```

**Example:** Input: Chemistry Concepts → Output: Searchable node graph with clickable definitions

---

## 25. Exam Prep Grid

```
Using dynamic view, turn these notes into an exam prep grid.

Grid columns:
- Topic
- Difficulty (stars or 1-5)
- Importance (Low/Med/High)
- Status (Not Started / In Progress / Mastered)

Allow clicking a topic to open a panel with summary, key formulas, and 1-2 practice questions.
```

**Example:** Input: Final Exam Topics → Output: Interactive grid with expandable topic panels

---

## 26. Strategy Workspace

```
Using dynamic view, transform this business plan into an interactive strategy workspace.

Tabs:
- Business Model Canvas (9 blocks)
- SWOT matrix
- Roadmap timeline

Each block/quadrant/timeline item is clickable and expands to show detailed bullets. Use consistent colors across tabs for the same themes (e.g., "customers", "product", "risks").
```

**Example:** Input: Business Plan → Output: Tabbed workspace with Canvas, SWOT, and Roadmap views

---

## 27. Kanban from Meeting Notes

```
Using dynamic view, convert these meeting notes into an interactive Kanban-style board.

Columns:
- To Do
- In Progress
- Blocked
- Done

Each action item becomes a card with title, owner, due date, and priority badge. Clicking a card reveals additional context from the meeting notes.
```

**Example:** Input: Sprint Planning Notes → Output: Kanban board with expandable action item cards

---

## 28. Interactive RACI Matrix

```
Using dynamic view, turn this project discussion into an interactive RACI matrix.

Grid:
- Rows: key tasks
- Columns: team members
- Cells: R, A, C, or I labels

Let me hover over a cell to see a short explanation of that person's role in that task, pulled from the notes.
```

**Example:** Input: Project Kickoff Notes → Output: Hoverable RACI grid with role explanations

---

## 29. Interactive Risk Register

```
Using dynamic view, convert these project notes into an interactive risk register.

Features:
- Table or card view for risks with fields: description, likelihood, impact, mitigation, owner
- Color coding for risk level (e.g., red/amber/green)
- Filter by owner, status, or severity
- Clicking a risk opens a detailed view with context and history.
```

**Example:** Input: Risk Assessment Notes → Output: Filterable, color-coded risk cards with detail views

---

## 30. Quarterly Gantt View

```
Using dynamic view, turn this planning discussion into an interactive Gantt-style timeline.

UI:
- Timeline on the x-axis (weeks or months)
- Bars for initiatives/projects
- Milestones as markers on the bars
- Hover shows summary, owner, and key dates
- Ability to filter or highlight items by team or priority.
```

**Example:** Input: Q1 Planning Notes → Output: Filterable Gantt chart with hoverable project bars
