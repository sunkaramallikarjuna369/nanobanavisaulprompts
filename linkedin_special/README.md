# LinkedIn Special: Animated Dynamic Visual Diagrams

```
╔══════════════════════════════════════════════════════════════════════╗
║              LINKEDIN SPECIAL DYNAMIC VISUALS                        ║
║                                                                      ║
║  Animated flowing diagrams like the ones you see on LinkedIn!        ║
║  Open any .html file in your browser to see the animation live.      ║
║                                                                      ║
║  ~~~~~ Lines that MOVE ~~~~~ Nodes that PULSE ~~~~~                  ║
║  ~~~~~ Gradients that FLOW ~~~~~ Paths that ANIMATE ~~~~~            ║
╚══════════════════════════════════════════════════════════════════════╝
```

## How LinkedIn Animated Diagrams Work

Those beautiful flowing line diagrams on LinkedIn are built using:

1. **SVG (Scalable Vector Graphics)** - Draws the shapes and paths
2. **CSS Animations** - Makes the lines move using `stroke-dasharray` and `stroke-dashoffset`
3. **CSS Gradients** - Creates the purple/teal color flows
4. **Keyframe Animations** - Controls timing and movement

## Files in This Folder

| File | What It Creates | How to Use |
|------|----------------|------------|
| [01-flowing-roadmap.html](01-flowing-roadmap.html) | AI Systems Roadmap with flowing animated lines | Open in browser |
| [02-animated-mindmap.html](02-animated-mindmap.html) | Mind Map with pulsing nodes and flowing connections | Open in browser |
| [03-tech-stack-flow.html](03-tech-stack-flow.html) | Technology stack with animated data flow paths | Open in browser |
| [04-process-pipeline.html](04-process-pipeline.html) | ML Pipeline with animated flowing gradient lines | Open in browser |
| [05-network-visualization.html](05-network-visualization.html) | Neural network with animated signal propagation | Open in browser |
| [06-timeline-flow.html](06-timeline-flow.html) | Career/Project timeline with animated milestones | Open in browser |
| [prompts-for-dynamic-visuals.md](prompts-for-dynamic-visuals.md) | Prompts to ask Gemini Nano Bana to generate these | Read guide |

## Quick Start

1. Download any `.html` file
2. Open it in Chrome/Firefox/Edge
3. Watch the animated flowing lines!
4. View source code to learn how it works
5. Use the prompts in `prompts-for-dynamic-visuals.md` to generate similar visuals

## The Secret: How Moving Lines Work

```css
/* This is the magic CSS that makes lines flow on LinkedIn diagrams */

/* Step 1: Define the path with dashes */
.flowing-line {
    stroke-dasharray: 10, 5;     /* 10px dash, 5px gap */
    animation: flow 2s linear infinite;
}

/* Step 2: Animate the dash offset to create movement */
@keyframes flow {
    from { stroke-dashoffset: 0; }
    to   { stroke-dashoffset: -15; }  /* dash + gap = 15 */
}

/* Step 3: Add gradient for color flow effect */
.gradient-line {
    stroke: url(#purpleToTealGradient);
}
```
