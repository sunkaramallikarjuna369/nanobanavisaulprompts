# Dynamic / Interactive Visual Prompts

Transform content into interactive UI experiences using Gemini's Dynamic View / Generative UI.

These prompts use the "dynamic view" prefix to generate interactive, clickable, hoverable visual interfaces instead of static images.

| # | Prompt Type | Output Style |
|---|------------|-------------|
| 1 | [Interactive Whiteboard](prompts.md#1-interactive-professor-whiteboard) | Clickable sidebar + whiteboard canvas |
| 2 | [Interactive Infographic](prompts.md#2-interactive-infographic) | Stat cards + expandable charts |
| 3 | [Interactive Mind Map](prompts.md#3-interactive-mind-map) | Clickable nodes with side panels |
| 4 | [Step-by-Step Guide](prompts.md#4-interactive-step-by-step-guide) | Progress indicator + step panels |
| 5 | [Interactive Timeline](prompts.md#5-interactive-timeline) | Clickable milestones with cards |
| 6 | [Flowchart Explorer](prompts.md#6-flowchart-explorer) | Clickable steps with detail panels |
| 7 | [System Architecture View](prompts.md#7-system-architecture-view) | Toggleable logical/deployment views |
| 8 | [Swimlane Diagram](prompts.md#8-swimlane-process-diagram) | Actor lanes with inline popups |
| 9 | [Decision Matrix](prompts.md#9-interactive-decision-matrix) | Clickable bubbles with pros/cons |
| 10 | [Data Flow Diagram](prompts.md#10-interactive-data-flow) | Clickable elements with detail panels |
| 11 | [Execution Tracer](prompts.md#11-execution-tracer) | Code + flow diagram in sync |
| 12 | [Data Structure Visualizer](prompts.md#12-data-structure-visualizer) | Animated step-through operations |
| 13 | [UML Class Explorer](prompts.md#13-uml-class-explorer) | Searchable class diagram |
| 14 | [API Sequence Diagram](prompts.md#14-api-sequence-diagram) | Clickable arrows with payloads |
| 15 | [Algorithm Walkthrough](prompts.md#15-algorithm-walkthrough) | Slider + visual panel |
| 16 | [KPI Dashboard](prompts.md#16-kpi-dashboard) | Filterable charts + linked table |
| 17 | [Interactive Funnel](prompts.md#17-interactive-funnel) | Clickable stages with drop-off data |
| 18 | [Geo Map View](prompts.md#18-geo-map-view) | Map markers with filter panel |
| 19 | [Correlation Heatmap](prompts.md#19-correlation-heatmap) | Hoverable cells with sorting |
| 20 | [Time-Series Explorer](prompts.md#20-time-series-explorer) | Pan/zoom chart with brush control |
| 21 | [Study Board](prompts.md#21-study-board) | Card columns with progress tracking |
| 22 | [Visual Cheat Sheet](prompts.md#22-interactive-cheat-sheet) | Hoverable formulas with tags |
| 23 | [Flashcard Carousel](prompts.md#23-flashcard-carousel) | Flip cards with spaced repetition |
| 24 | [Concept Relationship Map](prompts.md#24-concept-relationship-map) | Clickable nodes with definitions |
| 25 | [Exam Prep Grid](prompts.md#25-exam-prep-grid) | Expandable topics with practice Qs |
| 26 | [Strategy Workspace](prompts.md#26-strategy-workspace) | Tabbed canvas, SWOT, roadmap |
| 27 | [Kanban Board](prompts.md#27-kanban-from-meeting-notes) | Draggable cards with context |
| 28 | [RACI Matrix](prompts.md#28-interactive-raci-matrix) | Hoverable cells with role details |
| 29 | [Risk Register](prompts.md#29-interactive-risk-register) | Filterable, color-coded risk cards |
| 30 | [Quarterly Gantt](prompts.md#30-quarterly-gantt-view) | Timeline with hover details |

### Generic Dynamic-View Wrapper

Append this to any static prompt to make it interactive:

```
Use Dynamic View / generative UI instead of plain text or a single static image.

Requirements:
- Build a single interactive interface with components like cards, charts, tabs, timelines, or side panels
- Prefer clickable/hoverable elements over long paragraphs
- Use clear headings, icons, and color-coded sections
- Design it like a mini web app for exploring and learning this content.
```
