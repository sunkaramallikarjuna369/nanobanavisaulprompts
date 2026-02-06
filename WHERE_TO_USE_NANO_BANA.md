# Where & How to Apply Prompts Using Gemini Nano Bana

```
╔══════════════════════════════════════════════════════════════════════╗
║                                                                      ║
║     WHERE & HOW TO USE GEMINI NANO BANA                              ║
║     Complete Integration Guide                                       ║
║                                                                      ║
║     Chrome DevTools | Android Apps | Web API | Edge AI               ║
║                                                                      ║
╚══════════════════════════════════════════════════════════════════════╝
```

---

## Table of Contents

1. [What is Gemini Nano Bana?](#what-is-gemini-nano-bana)
2. [Where Can You Use It?](#where-can-you-use-it)
3. [Chrome Browser Integration](#1-chrome-browser-integration)
4. [Android App Integration](#2-android-app-integration)
5. [Web API Integration](#3-web-api-integration)
6. [Prompt Application Map](#4-prompt-application-map)
7. [Integration Workflows](#5-integration-workflows)
8. [Code Examples](#6-code-examples)
9. [Best Practices](#7-best-practices)
10. [Troubleshooting](#8-troubleshooting)

---

## What is Gemini Nano Bana?

```
┌──────────────────────────────────────────────────────────────────┐
│                                                                    │
│  Gemini Nano Bana is Google's lightweight on-device AI model      │
│  designed to run directly in Chrome browser and Android devices.  │
│                                                                    │
│  KEY CHARACTERISTICS:                                              │
│  ┌────────────┐  ┌────────────┐  ┌────────────┐  ┌────────────┐ │
│  │  On-Device  │  │  Fast      │  │  Private   │  │  Offline   │ │
│  │  Processing │  │  Response  │  │  Data      │  │  Capable   │ │
│  │  No server  │  │  <100ms    │  │  Stays     │  │  Works     │ │
│  │  needed     │  │  latency   │  │  local     │  │  anywhere  │ │
│  └────────────┘  └────────────┘  └────────────┘  └────────────┘ │
│                                                                    │
│  BEST FOR:                                                         │
│  - Text summarization           - Smart autocomplete              │
│  - Quick Q&A                    - Content suggestions             │
│  - Translation assistance       - Code completion hints           │
│  - On-device text processing    - Form field assistance           │
│                                                                    │
└──────────────────────────────────────────────────────────────────┘
```

---

## Where Can You Use It?

```
PLATFORM MAP:
                    ┌─────────────────┐
                    │  GEMINI NANO    │
                    │     BANA        │
                    └────────┬────────┘
                             │
            ┌────────────────┼────────────────┐
            │                │                │
     ┌──────▼──────┐  ┌─────▼──────┐  ┌──────▼──────┐
     │   CHROME    │  │  ANDROID   │  │   WEB API   │
     │   BROWSER   │  │    APPS    │  │  (Server)   │
     └──────┬──────┘  └─────┬──────┘  └──────┬──────┘
            │               │                │
     ┌──────▼──────┐  ┌─────▼──────┐  ┌──────▼──────┐
     │ DevTools    │  │ AICore     │  │ REST/gRPC   │
     │ Console     │  │ Library    │  │ Endpoints   │
     │ Extensions  │  │ Kotlin/Java│  │ Node/Python │
     │ Web Apps    │  │ On-device  │  │ Cloud-based │
     └─────────────┘  └────────────┘  └─────────────┘
```

---

## 1. Chrome Browser Integration

### How to Access Nano Bana in Chrome

```
STEP-BY-STEP SETUP:
┌─────────────────────────────────────────────────────────────┐
│                                                               │
│  Step 1: Update Chrome to version 127+ (or Canary/Dev)      │
│          chrome://settings/help → Check for updates          │
│                                                               │
│  Step 2: Enable the Prompt API flag                          │
│          Navigate to: chrome://flags                         │
│          Search: "Prompt API for Gemini Nano"                │
│          Set to: ENABLED                                     │
│                                                               │
│  Step 3: Enable the on-device model                          │
│          Navigate to: chrome://flags                         │
│          Search: "Enables optimization guide on device"      │
│          Set to: ENABLED                                     │
│                                                               │
│  Step 4: Restart Chrome                                      │
│          Click "Relaunch" button                             │
│                                                               │
│  Step 5: Wait for model download                             │
│          Navigate to: chrome://components                    │
│          Look for: "Optimization Guide On Device Model"      │
│          Click "Check for update" if needed                  │
│          Status should show: "Up-to-date"                    │
│                                                               │
│  Step 6: Verify in DevTools Console                          │
│          Press F12 → Console tab                             │
│          Type: await ai.languageModel.capabilities()         │
│          Should return: { available: "readily" }             │
│                                                               │
└─────────────────────────────────────────────────────────────┘
```

### Using Nano Bana in Chrome DevTools Console

```javascript
// Check if Nano Bana is available
const capabilities = await ai.languageModel.capabilities();
console.log(capabilities);
// Output: { available: "readily", defaultTopK: 3, maxTopK: 8, defaultTemperature: 1.0 }

// Create a session
const session = await ai.languageModel.create();

// Send a prompt (use ANY prompt from this library!)
const result = await session.prompt("Explain Docker in 3 sentences");
console.log(result);

// Stream response for longer outputs
const stream = await session.promptStreaming("Create a step-by-step guide for Git");
for await (const chunk of stream) {
  console.log(chunk);
}

// Create session with system prompt (Role-Based Prompts!)
const expertSession = await ai.languageModel.create({
  systemPrompt: "You are a senior Python developer. Always include code examples."
});
const answer = await expertSession.prompt("How do I handle exceptions?");

// Destroy session when done
session.destroy();
```

### Chrome Extension Integration

```javascript
// manifest.json for Chrome Extension using Nano Bana
{
  "name": "Nano Bana Assistant",
  "version": "1.0",
  "manifest_version": 3,
  "permissions": ["aiLanguageModelOriginTrial"],
  "content_scripts": [{
    "matches": ["<all_urls>"],
    "js": ["content.js"]
  }]
}

// content.js - Use Nano Bana to summarize selected text
document.addEventListener('mouseup', async () => {
  const selectedText = window.getSelection().toString();
  if (selectedText.length > 50) {
    const session = await ai.languageModel.create();
    const summary = await session.prompt(
      `Summarize this in 2 sentences: ${selectedText}`
    );
    showTooltip(summary);
    session.destroy();
  }
});
```

### Web Application Integration

```html
<!DOCTYPE html>
<html>
<head><title>Nano Bana Web App</title></head>
<body>
  <textarea id="input" placeholder="Enter your question..."></textarea>
  <button onclick="askNanoBana()">Ask Nano Bana</button>
  <div id="output"></div>

  <script>
    async function askNanoBana() {
      const input = document.getElementById('input').value;
      const output = document.getElementById('output');

      // Check availability first
      const { available } = await ai.languageModel.capabilities();
      if (available === 'no') {
        output.textContent = 'Nano Bana not available. Please enable in chrome://flags';
        return;
      }

      output.textContent = 'Thinking...';
      const session = await ai.languageModel.create();

      // Stream the response
      const stream = await session.promptStreaming(input);
      output.textContent = '';
      for await (const chunk of stream) {
        output.textContent = chunk;
      }

      session.destroy();
    }
  </script>
</body>
</html>
```

---

## 2. Android App Integration

### Setup for Android

```
ANDROID INTEGRATION STEPS:
┌─────────────────────────────────────────────────────────────┐
│                                                               │
│  Step 1: Add dependency in build.gradle                      │
│          implementation 'com.google.ai:generativeai:0.x.x'  │
│                                                               │
│  Step 2: Initialize the on-device model                      │
│          Use GenerativeModel with "gemini-nano" config       │
│                                                               │
│  Step 3: Check device compatibility                          │
│          Requires: Android 14+ with Google AI Core           │
│          Minimum: 4GB RAM device                             │
│                                                               │
│  Step 4: Request model download if not cached                │
│          Model downloads in background (~100MB)              │
│                                                               │
│  Step 5: Use in your app activities/fragments                │
│          Prompt the model with any prompt from this library  │
│                                                               │
└─────────────────────────────────────────────────────────────┘
```

### Kotlin Code Example

```kotlin
// build.gradle (app level)
dependencies {
    implementation("com.google.ai.client.generativeai:generativeai:0.7.0")
}

// MainActivity.kt
import com.google.ai.client.generativeai.GenerativeModel
import com.google.ai.client.generativeai.type.generationConfig

class MainActivity : AppCompatActivity() {

    private lateinit var model: GenerativeModel

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)

        // Initialize Gemini Nano (on-device)
        model = GenerativeModel(
            modelName = "gemini-nano",
            generationConfig = generationConfig {
                temperature = 0.7f
                topK = 3
                maxOutputTokens = 1024
            }
        )
    }

    // Use ANY prompt from this library
    suspend fun askQuestion(prompt: String): String {
        return try {
            val response = model.generateContent(prompt)
            response.text ?: "No response"
        } catch (e: Exception) {
            "Error: ${e.message}"
        }
    }

    // Example: Using a Chain-of-Thought prompt
    suspend fun solveWithReasoning(problem: String): String {
        val cotPrompt = """
            Solve this step by step:
            $problem

            Think through each step:
            Step 1: [identify what's given]
            Step 2: [determine the approach]
            Step 3: [execute the solution]
            Final Answer: [state the result]
        """.trimIndent()

        return askQuestion(cotPrompt)
    }

    // Example: Using a Role-Based prompt
    suspend fun getExpertAdvice(topic: String): String {
        val rolePrompt = """
            You are a senior software architect with 15 years of experience.
            Provide expert advice on: $topic
            Include: best practices, common pitfalls, and recommended tools.
        """.trimIndent()

        return askQuestion(rolePrompt)
    }
}
```

### Android Use Cases

```
ON-DEVICE AI USE CASES:
┌──────────────────────┬───────────────────────────────────────┐
│ Use Case             │ Prompt Type to Use                    │
├──────────────────────┼───────────────────────────────────────┤
│ Smart Reply          │ 01-Foundational (Direct Instruction)  │
│ Text Summarization   │ 14-Summarization (Tiered Summary)     │
│ Writing Assistant    │ 15-Creative (Idea Generation)         │
│ Code Helper          │ 11-Code Generation (Quick Snippets)   │
│ Study Aid            │ 12-Assessment (Quiz Generation)       │
│ Translation          │ 04-Role-Based (Translator Role)       │
│ Form Auto-fill       │ 01-Foundational (Template-Based)      │
│ Accessibility        │ 14-Summarization (Key Points)         │
└──────────────────────┴───────────────────────────────────────┘
```

---

## 3. Web API Integration

### Using Gemini API (Server-Side)

For server-side applications where you need more power than the on-device model:

```
API SETUP:
┌─────────────────────────────────────────────────────────────┐
│                                                               │
│  Step 1: Get API key from Google AI Studio                   │
│          https://aistudio.google.com/apikey                  │
│                                                               │
│  Step 2: Install the SDK                                     │
│          npm install @google/generative-ai                   │
│          pip install google-generativeai                      │
│                                                               │
│  Step 3: Initialize with your API key                        │
│          const genAI = new GoogleGenerativeAI(API_KEY);      │
│                                                               │
│  Step 4: Choose the model                                    │
│          "gemini-1.5-flash" for fast responses               │
│          "gemini-1.5-pro" for complex tasks                  │
│                                                               │
└─────────────────────────────────────────────────────────────┘
```

### Node.js Example

```javascript
const { GoogleGenerativeAI } = require("@google/generative-ai");

const genAI = new GoogleGenerativeAI(process.env.GEMINI_API_KEY);
const model = genAI.getGenerativeModel({ model: "gemini-1.5-flash" });

// Use ANY prompt from this library via API
async function generateWithPrompt(promptText) {
  const result = await model.generateContent(promptText);
  return result.response.text();
}

// Example: Few-Shot Prompt (Concept 03)
async function classifySentiment(text) {
  const prompt = `
    Classify the sentiment of the text as Positive, Negative, or Neutral.

    Examples:
    Text: "This product is amazing!" → Sentiment: Positive
    Text: "Terrible experience, never again" → Sentiment: Negative
    Text: "The meeting is at 3pm" → Sentiment: Neutral

    Text: "${text}" → Sentiment:
  `;
  return generateWithPrompt(prompt);
}

// Example: Chain-of-Thought Prompt (Concept 02)
async function solveWithReasoning(problem) {
  const prompt = `
    Solve this problem step by step. Show your reasoning at each step.

    Problem: ${problem}

    Step 1: Understand what is being asked
    Step 2: Identify the relevant information
    Step 3: Apply the appropriate method
    Step 4: Calculate the answer
    Final Answer:
  `;
  return generateWithPrompt(prompt);
}

// Example: Comparative Analysis Prompt (Concept 09)
async function compareTechnologies(tech1, tech2, criteria) {
  const prompt = `
    Compare ${tech1} vs ${tech2} across these criteria: ${criteria.join(', ')}.

    For each criterion, rate both on a 1-10 scale and explain why.
    End with a clear recommendation based on the scores.

    Format as a comparison table.
  `;
  return generateWithPrompt(prompt);
}
```

### Python Example

```python
import google.generativeai as genai
import os

genai.configure(api_key=os.environ['GEMINI_API_KEY'])
model = genai.GenerativeModel('gemini-1.5-flash')

# Use ANY prompt from this library via API
def generate(prompt_text):
    response = model.generate_content(prompt_text)
    return response.text

# Example: Tutorial Generation Prompt (Concept 06)
def generate_tutorial(topic, level="beginner"):
    prompt = f"""
    Create a step-by-step tutorial for: {topic}
    Target audience: {level}

    Include:
    1. Prerequisites
    2. Step-by-step instructions with code examples
    3. Common mistakes to avoid
    4. Practice exercises
    5. Next steps for learning more
    """
    return generate(prompt)

# Example: PDF Analysis Prompt (Concept 07)
def analyze_document(document_text):
    prompt = f"""
    Analyze this document and extract:
    1. Main topic and purpose
    2. Key findings (top 5)
    3. Data points and statistics mentioned
    4. Conclusions and recommendations
    5. One-paragraph executive summary

    Document:
    {document_text}
    """
    return generate(prompt)

# Example: Code Review Prompt (Concept 11)
def review_code(code, language="python"):
    prompt = f"""
    Review this {language} code for:
    1. Security vulnerabilities (SQL injection, XSS, etc.)
    2. Performance issues
    3. Best practice violations
    4. Potential bugs

    Rate severity: Critical / High / Medium / Low
    Provide fixed code for each issue found.

    Code:
    ```{language}
    {code}
    ```
    """
    return generate(prompt)
```

---

## 4. Prompt Application Map

### Which Prompt Type to Use Where

```
APPLICATION MATRIX:
┌────────────────────────────┬──────────┬──────────┬──────────┐
│ Prompt Concept             │ Chrome   │ Android  │ Web API  │
│                            │ On-Device│ On-Device│ Server   │
├────────────────────────────┼──────────┼──────────┼──────────┤
│ 01 Foundational            │ ★★★★★   │ ★★★★★   │ ★★★★★   │
│ 02 Chain-of-Thought        │ ★★★☆☆   │ ★★★☆☆   │ ★★★★★   │
│ 03 Few-Shot                │ ★★★★☆   │ ★★★★☆   │ ★★★★★   │
│ 04 Role-Based              │ ★★★★★   │ ★★★★★   │ ★★★★★   │
│ 05 Visual/Diagram          │ ★★☆☆☆   │ ★★☆☆☆   │ ★★★★★   │
│ 06 Tutorial Generation     │ ★★★☆☆   │ ★★★☆☆   │ ★★★★★   │
│ 07 PDF Analysis            │ ★★☆☆☆   │ ★★★☆☆   │ ★★★★★   │
│ 08 Dynamic Interactive     │ ★★★★☆   │ ★★★★★   │ ★★★★☆   │
│ 09 Comparative Analysis    │ ★★★☆☆   │ ★★★☆☆   │ ★★★★★   │
│ 10 Storytelling            │ ★★★★☆   │ ★★★★☆   │ ★★★★★   │
│ 11 Code Gen & Debug        │ ★★★☆☆   │ ★★★☆☆   │ ★★★★★   │
│ 12 Assessment & Quiz       │ ★★★★☆   │ ★★★★★   │ ★★★★★   │
│ 13 Data Visualization      │ ★★☆☆☆   │ ★★☆☆☆   │ ★★★★★   │
│ 14 Summarization           │ ★★★★★   │ ★★★★★   │ ★★★★★   │
│ 15 Creative Brainstorming  │ ★★★★☆   │ ★★★★☆   │ ★★★★★   │
├────────────────────────────┼──────────┼──────────┼──────────┤
│ ★★★★★ = Excellent fit     │          │          │          │
│ ★★★☆☆ = Works but limited │          │          │          │
│ ★★☆☆☆ = Basic support     │          │          │          │
└────────────────────────────┴──────────┴──────────┴──────────┘

NOTE: On-device (Chrome/Android) is best for short prompts and
quick responses. Complex prompts work better with Web API.
```

---

## 5. Integration Workflows

### Workflow 1: Smart Writing Assistant (Chrome)

```
USER FLOW:
┌──────────┐    ┌──────────────┐    ┌──────────────┐    ┌────────────┐
│ User     │    │ Detect text  │    │ Apply prompt │    │ Show       │
│ types in │───→│ input field  │───→│ template     │───→│ suggestion │
│ textarea │    │ (on focus)   │    │ (Concept 01) │    │ (inline)   │
└──────────┘    └──────────────┘    └──────────────┘    └────────────┘

IMPLEMENTATION:
1. Listen for input events on text areas
2. When user pauses typing (debounce 500ms)
3. Send current text to Nano Bana with autocomplete prompt
4. Display suggestion as ghost text
5. Tab to accept, Esc to dismiss
```

### Workflow 2: Study App (Android)

```
USER FLOW:
┌──────────┐    ┌──────────────┐    ┌──────────────┐    ┌────────────┐
│ Student  │    │ Generate     │    │ Student      │    │ Grade &    │
│ selects  │───→│ quiz using   │───→│ answers      │───→│ explain    │
│ topic    │    │ (Concept 12) │    │ questions    │    │ (Concept 2)│
└──────────┘    └──────────────┘    └──────────────┘    └────────────┘

PROMPT CHAIN:
1. Use Assessment Prompt (12) to generate quiz
2. User answers questions
3. Use Chain-of-Thought (02) to explain correct answers
4. Use Knowledge Assessment to track progress
```

### Workflow 3: Code Review Pipeline (Web API)

```
USER FLOW:
┌──────────┐    ┌──────────────┐    ┌──────────────┐    ┌────────────┐
│ Dev      │    │ Extract code │    │ Run prompts  │    │ Post       │
│ pushes   │───→│ from PR diff │───→│ (Concept 11) │───→│ review     │
│ code     │    │ via webhook  │    │ Security+Perf│    │ comments   │
└──────────┘    └──────────────┘    └──────────────┘    └────────────┘

PROMPT CHAIN:
1. Webhook receives PR event
2. Extract changed files
3. Use Code Review prompt (11) for security scan
4. Use Code Review prompt (11) for performance check
5. Use Summarization prompt (14) to create review summary
6. Post as PR comment via GitHub API
```

---

## 6. Code Examples

### Complete Chrome Extension: Text Summarizer

```javascript
// background.js
chrome.runtime.onInstalled.addListener(() => {
  chrome.contextMenus.create({
    id: "summarize",
    title: "Summarize with Nano Bana",
    contexts: ["selection"]
  });
});

chrome.contextMenus.onClicked.addListener(async (info, tab) => {
  if (info.menuItemId === "summarize") {
    const selectedText = info.selectionText;

    // Use Tiered Summary prompt (Concept 14)
    const session = await ai.languageModel.create({
      systemPrompt: "You are a concise summarizer. Always respond in 2-3 sentences."
    });

    const summary = await session.prompt(
      `Summarize this text in 2-3 key sentences: ${selectedText}`
    );

    // Send summary to content script to display
    chrome.tabs.sendMessage(tab.id, {
      action: "showSummary",
      summary: summary
    });

    session.destroy();
  }
});
```

### Complete Android Widget: Quick Q&A

```kotlin
class QuickAnswerWidget : AppWidgetProvider() {

    override fun onUpdate(context: Context, appWidgetManager: AppWidgetManager,
                          appWidgetIds: IntArray) {
        for (appWidgetId in appWidgetIds) {
            val views = RemoteViews(context.packageName, R.layout.widget_layout)
            views.setOnClickPendingIntent(R.id.askButton,
                getPendingIntent(context, appWidgetId))
            appWidgetManager.updateAppWidget(appWidgetId, views)
        }
    }

    // Uses Foundational Prompt (Concept 01)
    suspend fun getQuickAnswer(question: String): String {
        val model = GenerativeModel(modelName = "gemini-nano")
        val prompt = """
            Answer this question in one concise sentence:
            $question
        """.trimIndent()
        val response = model.generateContent(prompt)
        return response.text ?: "Could not generate answer"
    }
}
```

---

## 7. Best Practices

### On-Device (Chrome & Android) Tips

```
┌──────────────────────────────────────────────────────────────┐
│  ON-DEVICE BEST PRACTICES                                     │
│                                                               │
│  1. KEEP PROMPTS SHORT                                       │
│     On-device models have limited context windows            │
│     Aim for < 500 tokens in prompt + response                │
│                                                               │
│  2. USE SYSTEM PROMPTS FOR ROLE-BASED                        │
│     Set the role in systemPrompt parameter, not in           │
│     the user prompt itself (saves tokens)                    │
│                                                               │
│  3. PREFER FOUNDATIONAL & FEW-SHOT PROMPTS                  │
│     These work best with smaller models                      │
│     Keep few-shot examples to 2-3 max                        │
│                                                               │
│  4. STREAM RESPONSES                                         │
│     Use promptStreaming() for better UX                      │
│     User sees response building in real-time                 │
│                                                               │
│  5. HANDLE AVAILABILITY GRACEFULLY                           │
│     Always check capabilities() first                        │
│     Provide fallback for unsupported devices                 │
│                                                               │
│  6. DESTROY SESSIONS                                         │
│     Call session.destroy() when done                         │
│     Prevents memory leaks on device                          │
│                                                               │
│  7. CACHE REPEATED QUERIES                                   │
│     Store responses for identical prompts                    │
│     Reduces model inference cycles                           │
│                                                               │
└──────────────────────────────────────────────────────────────┘
```

### Web API Tips

```
┌──────────────────────────────────────────────────────────────┐
│  WEB API BEST PRACTICES                                       │
│                                                               │
│  1. USE FULL PROMPT TEMPLATES                                │
│     API models handle complex prompts well                   │
│     Chain-of-Thought and long Few-Shot work great            │
│                                                               │
│  2. SET TEMPERATURE APPROPRIATELY                            │
│     Creative tasks: 0.8-1.0                                  │
│     Factual/code tasks: 0.1-0.3                              │
│     Balanced: 0.5-0.7                                        │
│                                                               │
│  3. IMPLEMENT RETRY LOGIC                                    │
│     API calls can fail; use exponential backoff              │
│     Max 3 retries with 1s, 2s, 4s delays                    │
│                                                               │
│  4. RATE LIMIT YOUR REQUESTS                                 │
│     Free tier: 60 requests/minute                            │
│     Implement request queuing                                │
│                                                               │
│  5. SANITIZE USER INPUT                                      │
│     Never pass raw user input to prompts                     │
│     Escape special characters and limit length               │
│                                                               │
│  6. LOG PROMPTS AND RESPONSES                                │
│     Track which prompts perform best                         │
│     A/B test different prompt variations                     │
│                                                               │
└──────────────────────────────────────────────────────────────┘
```

---

## 8. Troubleshooting

### Common Issues

```
TROUBLESHOOTING GUIDE:
┌──────────────────────┬──────────────────────────────────────┐
│ Issue                │ Solution                             │
├──────────────────────┼──────────────────────────────────────┤
│ "Model not available"│ 1. Check chrome://flags enabled      │
│                      │ 2. Check chrome://components         │
│                      │ 3. Restart Chrome                    │
│                      │ 4. Wait for model download           │
├──────────────────────┼──────────────────────────────────────┤
│ Slow responses       │ 1. Shorten prompt length             │
│                      │ 2. Reduce maxOutputTokens            │
│                      │ 3. Close other heavy tabs            │
│                      │ 4. Check device RAM usage            │
├──────────────────────┼──────────────────────────────────────┤
│ Poor quality output  │ 1. Add more context to prompt        │
│                      │ 2. Use few-shot examples             │
│                      │ 3. Try role-based system prompt      │
│                      │ 4. Adjust temperature setting        │
├──────────────────────┼──────────────────────────────────────┤
│ API quota exceeded   │ 1. Implement caching                 │
│                      │ 2. Batch similar requests            │
│                      │ 3. Use on-device for simple tasks    │
│                      │ 4. Upgrade API plan                  │
├──────────────────────┼──────────────────────────────────────┤
│ Android model crash  │ 1. Check minimum RAM (4GB)           │
│                      │ 2. Update Google AI Core app         │
│                      │ 3. Clear app cache                   │
│                      │ 4. Reduce concurrent sessions        │
└──────────────────────┴──────────────────────────────────────┘
```

---

## Quick Decision Guide

```
WHICH PLATFORM TO USE?
                          START HERE
                              │
                     Is data privacy critical?
                        /              \
                      YES               NO
                      │                  │
               Is internet available?    │
                /           \            │
              YES            NO          │
              │              │           │
        ┌─────▼────┐  ┌─────▼────┐  ┌──▼──────────┐
        │  Chrome   │  │ Android  │  │  Web API    │
        │  On-Device│  │ On-Device│  │  (Server)   │
        │          │  │          │  │             │
        │ Quick Q&A│  │ Offline  │  │ Complex     │
        │ Summary  │  │ capable  │  │ prompts     │
        │ Simple   │  │ Mobile   │  │ Long output │
        │ tasks    │  │ apps     │  │ Multi-step  │
        └──────────┘  └──────────┘  └─────────────┘
```
