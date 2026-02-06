# Prompts to Generate Dynamic Visual Diagrams with Gemini Nano Bana

```
╔══════════════════════════════════════════════════════════════════════╗
║          HOW TO PROMPT FOR ANIMATED LINKEDIN-STYLE VISUALS          ║
║                                                                      ║
║  The SECRET: Ask for SVG + CSS animations with specific techniques   ║
║                                                                      ║
║  stroke-dasharray ──> Moving lines                                   ║
║  @keyframes ──> Flowing effects                                      ║
║  CSS gradients ──> Color transitions                                 ║
║  transform + transition ──> Hover interactions                       ║
╚══════════════════════════════════════════════════════════════════════╝
```

---

## The Core Techniques That Make Lines Move

### Technique 1: stroke-dasharray + stroke-dashoffset (THE KEY TO FLOWING LINES)

This is the #1 technique used in LinkedIn animated diagrams.

**Prompt:**
```
Generate an SVG with a curved path that has flowing animated dashes.
Use stroke-dasharray to create dashes and animate stroke-dashoffset
with CSS @keyframes to make them flow continuously.
Color: purple to teal gradient. Dark background.
```

**What Gemini Nano Bana generates:**
```html
<svg viewBox="0 0 400 200">
  <defs>
    <linearGradient id="grad1" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#a855f7"/>
      <stop offset="100%" stop-color="#06b6d4"/>
    </linearGradient>
  </defs>
  <path d="M 50,100 C 150,20 250,180 350,100"
        fill="none"
        stroke="url(#grad1)"
        stroke-width="3"
        stroke-dasharray="10, 5"
        class="flowing-path"/>
</svg>

<style>
  .flowing-path {
    animation: flow 2s linear infinite;
  }
  @keyframes flow {
    from { stroke-dashoffset: 0; }
    to { stroke-dashoffset: -15; } /* -(dasharray sum) */
  }
</style>
```

**How it works:**
```
FRAME 1:  ━━━━━━━━━━ ····· ━━━━━━━━━━ ····· ━━━━━━━━━━
FRAME 2:  ···━━━━━━━━━━ ····· ━━━━━━━━━━ ····· ━━━━━━━━
FRAME 3:  ·····━━━━━━━━━━ ····· ━━━━━━━━━━ ····· ━━━━━━
          └──────── The dashes appear to MOVE! ────────┘
```

---

### Technique 2: Pulsing Nodes with radial-gradient + scale animation

**Prompt:**
```
Create SVG circles that pulse with a glowing effect.
Use radial gradient for the glow and CSS animation
to scale between 1.0 and 1.1 with ease-in-out timing.
Add box-shadow glow that expands and fades.
```

**What Gemini Nano Bana generates:**
```html
<svg viewBox="0 0 200 200">
  <defs>
    <radialGradient id="glow">
      <stop offset="0%" stop-color="#a855f7" stop-opacity="0.6"/>
      <stop offset="100%" stop-color="#a855f7" stop-opacity="0"/>
    </radialGradient>
  </defs>
  <!-- Outer glow -->
  <circle cx="100" cy="100" r="40" fill="url(#glow)" class="pulse-glow"/>
  <!-- Inner solid circle -->
  <circle cx="100" cy="100" r="20" fill="#a855f7" class="pulse-node"/>
</svg>

<style>
  .pulse-glow {
    animation: glowPulse 2s ease-in-out infinite;
    transform-origin: center;
  }
  .pulse-node {
    animation: nodePulse 2s ease-in-out infinite;
    transform-origin: center;
  }
  @keyframes glowPulse {
    0%, 100% { opacity: 0.3; transform: scale(1); }
    50% { opacity: 0.8; transform: scale(1.3); }
  }
  @keyframes nodePulse {
    0%, 100% { transform: scale(1); }
    50% { transform: scale(1.1); }
  }
</style>
```

---

### Technique 3: Particle Flow Along a Path

**Prompt:**
```
Create an SVG with small circles that travel along a curved bezier path.
Use CSS animation with translateX or use SVG animateMotion.
3 particles with staggered delays creating a flowing stream effect.
Purple glowing particles on dark background.
```

**What Gemini Nano Bana generates:**
```html
<svg viewBox="0 0 500 200">
  <defs>
    <path id="motionPath" d="M 50,100 C 150,20 350,180 450,100" fill="none"/>
  </defs>
  <!-- Visible path (faint) -->
  <use href="#motionPath" stroke="#a855f7" stroke-width="1" opacity="0.2"/>

  <!-- Particle 1 -->
  <circle r="4" fill="#a855f7" filter="url(#particleGlow)">
    <animateMotion dur="3s" repeatCount="indefinite" begin="0s">
      <mpath href="#motionPath"/>
    </animateMotion>
  </circle>
  <!-- Particle 2 -->
  <circle r="4" fill="#06b6d4">
    <animateMotion dur="3s" repeatCount="indefinite" begin="1s">
      <mpath href="#motionPath"/>
    </animateMotion>
  </circle>
  <!-- Particle 3 -->
  <circle r="4" fill="#f472b6">
    <animateMotion dur="3s" repeatCount="indefinite" begin="2s">
      <mpath href="#motionPath"/>
    </animateMotion>
  </circle>
</svg>
```

---

### Technique 4: Gradient Line that Appears to Flow

**Prompt:**
```
Create a horizontal line where the gradient color appears to shift
and flow from left to right continuously. Use CSS background-position
animation on a linear-gradient with background-size: 200%.
```

**What Gemini Nano Bana generates:**
```html
<div class="flowing-gradient-line"></div>

<style>
  .flowing-gradient-line {
    width: 100%;
    height: 4px;
    border-radius: 2px;
    background: linear-gradient(90deg,
      #a855f7, #06b6d4, #10b981, #a855f7);
    background-size: 200% 100%;
    animation: gradientFlow 3s linear infinite;
  }
  @keyframes gradientFlow {
    0% { background-position: 0% 50%; }
    100% { background-position: 200% 50%; }
  }
</style>
```

---

### Technique 5: Branching Tree with Animated Reveal

**Prompt:**
```
Create an SVG tree diagram where branches draw themselves
from the trunk outward. Use stroke-dasharray equal to the
path length and animate stroke-dashoffset from path-length
to 0. Stagger each branch's animation-delay.
```

**What Gemini Nano Bana generates:**
```html
<svg viewBox="0 0 600 400">
  <style>
    .branch {
      fill: none;
      stroke-width: 2.5;
      stroke-linecap: round;
      stroke-dasharray: 200;
      stroke-dashoffset: 200;
      animation: drawBranch 1.5s ease-out forwards;
    }
    .branch:nth-child(1) { animation-delay: 0s; }
    .branch:nth-child(2) { animation-delay: 0.3s; }
    .branch:nth-child(3) { animation-delay: 0.6s; }
    .branch:nth-child(4) { animation-delay: 0.9s; }
    .branch:nth-child(5) { animation-delay: 1.2s; }

    @keyframes drawBranch {
      to { stroke-dashoffset: 0; }
    }
  </style>

  <!-- Trunk -->
  <path class="branch" d="M 300,380 L 300,200" stroke="#a855f7"/>
  <!-- Branch left -->
  <path class="branch" d="M 300,250 C 250,230 180,200 120,160" stroke="#06b6d4"/>
  <!-- Branch right -->
  <path class="branch" d="M 300,250 C 350,230 420,200 480,160" stroke="#06b6d4"/>
  <!-- Sub-branch left -->
  <path class="branch" d="M 300,200 C 230,180 160,120 100,80" stroke="#f472b6"/>
  <!-- Sub-branch right -->
  <path class="branch" d="M 300,200 C 370,180 440,120 500,80" stroke="#f472b6"/>
</svg>
```

---

## Complete Prompt Templates for LinkedIn-Style Visuals

### Template 1: Roadmap with Flowing Lines
```
Generate a complete HTML file with an animated roadmap for [TOPIC].
Requirements:
- Dark background (#0a0a1a)
- Left side: main category nodes as rounded rectangles with gradient fills
- Right side: sub-topics as text with dot indicators
- Curved bezier paths connecting nodes to sub-topics
- ALL lines must have stroke-dasharray animation creating flowing movement
- Purple-to-teal color scheme with gradients
- Vertical progress bar on the left edge
- Hover effects on nodes (scale, glow)
- Responsive SVG viewBox
- No JavaScript required, CSS-only animations
```

### Template 2: Mind Map with Pulsing Branches
```
Generate a complete HTML file with an animated mind map for [TOPIC].
Requirements:
- Center node: large circle with pulse animation and glow filter
- 6 branches radiating outward using curved bezier paths
- Each branch: different gradient color
- Leaf nodes at branch ends
- All connections use stroke-dasharray flowing animation
- Nodes float with gentle translateY animation
- Dark radial gradient background
- SVG with viewBox for responsive scaling
```

### Template 3: Process Pipeline with Particle Flow
```
Generate a complete HTML file showing a [NUMBER]-stage pipeline for [TOPIC].
Requirements:
- Horizontal layout with circle icons for each stage
- Between stages: animated connector lines
- Flowing gradient light effect on connectors
- 3 glowing particles travel along each connector with staggered timing
- Stage icons pulse with scale animation
- Metric cards below the pipeline
- Dark background, gradient text
- Hover interactions on stages
```

### Template 4: Timeline with Animated Milestones
```
Generate a complete HTML file with an animated timeline for [TOPIC].
Requirements:
- Vertical center line with multi-color gradient
- Flowing light animation on the center line
- Milestone cards alternating left and right
- Each card slides in with staggered animation delays
- Pulsing dot connectors at junction points
- Unique color theme per milestone
- Technology/skill tags on each card
- Hover: scale up with glow effect
- Responsive layout
```

---

## Key CSS Properties Cheat Sheet

| Property | Effect | Example |
|----------|--------|---------|
| `stroke-dasharray` | Creates dashes in SVG lines | `stroke-dasharray: 10, 5` |
| `stroke-dashoffset` | Shifts dash position (animate this!) | `animation: flow 2s linear infinite` |
| `animation` | Applies keyframe animation | `animation: pulse 2s ease-in-out infinite` |
| `transform: scale()` | Pulsing/growing effect | `transform: scale(1.1)` |
| `filter: drop-shadow()` | Glow effect on SVG elements | `filter: drop-shadow(0 0 10px #a855f7)` |
| `opacity` | Fading in/out | `animation: fadeIn 0.5s forwards` |
| `background-size: 200%` | Enables gradient flow on HTML elements | With `background-position` animation |
| `clip-path` | Reveal animations | Animate polygon points |
