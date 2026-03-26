# CLAUDE.md — Mental Health Resources for Youth Athletes

This file provides context for AI assistants working in this repository.

## Project Overview

A static, single-file web application providing mental health resources specifically for youth athletes. The app includes crisis hotlines, local clinic listings, live facility data from the SAMHSA national database, and a keyword-based chatbot.

**Target audience:** Youth athletes, coaches, parents, and athletic organizations in Oregon.

## Repository Structure

```
/
├── index.html      # Entire application (HTML + CSS + JS in one file)
├── README.md       # Minimal project title
└── CLAUDE.md       # This file
```

There is no build system, package manager, backend, or external dependencies. The entire application is self-contained in `index.html`.

## Tech Stack

- **HTML5** — Semantic markup, single page
- **CSS** — Vanilla, embedded in `<style>` tags in `<head>`
- **JavaScript** — Vanilla ES6, embedded in `<script>` tags at end of `<body>`
- **External API** — SAMHSA National Mental Health Facilities Locator

No frameworks, no bundler, no npm, no build step.

## Running the Application

Open `index.html` directly in a browser — no server required.

For local development with live reload, any static file server works:
```bash
# Python
python3 -m http.server 8000

# Node.js (npx)
npx serve .
```

## Application Sections

### 1. Search Bar (`#searchInput`)
Filters visible `.section` elements by text content match. Controlled by `searchResources()`.

### 2. Crisis & Emergency Support
Static content — hardcoded crisis phone numbers with `tel:` links:
- 988 Suicide & Crisis Lifeline
- YouthLine (877-968-8491)
- Lines for Life Sports & Wellness (800-273-8255)

**Do not remove or alter crisis numbers without verified replacements.**

### 3. Sports Psychology & Therapy Clinics
Static HTML table (`.resource-table`) listing local Oregon clinics with links.

### 4. Live Mental Health Resources (`#apiResources`)
Populated at page load by `fetchMentalHealthResources()`, which calls:
```
https://findtreatment.samhsa.gov/locator/api/1.0/facilities?state=OR&serviceType=MentalHealth
```
Displays the first 5 results. Falls back to an error message if the API is unavailable.

### 5. Resource Navigator Chatbot (`.chatbot`)
Fixed bottom-right widget. Toggled by `toggleChatbot()`. Responds to keywords:
- `anxiety` → anxiety management resource
- `burnout` → burnout prevention resource
- `injury` → injury recovery resource
- `stress` → mindfulness resource
- `help` → directs to 988 crisis line
- *(anything else)* → suggests using the search bar

## Code Conventions

### Naming
| Context | Convention | Example |
|---|---|---|
| HTML IDs | camelCase | `searchInput`, `chatbotBody`, `apiResources` |
| CSS classes | kebab-case | `chatbot-header`, `resource-table` |
| JS functions | camelCase | `sendChat()`, `toggleChatbot()` |

### File Organization (within `index.html`)
1. `<head>` — meta tags, title, all `<style>` rules
2. `<body>` — semantic HTML structure
3. Chatbot UI (fixed overlay, outside `<main>`)
4. Chatbot toggle button
5. `<script>` blocks at bottom of body, each labeled with an HTML comment:
   - `<!-- Search Script -->`
   - `<!-- Chatbot Script -->`
   - API fetch script (unlabeled)
   - Toggle script (unlabeled)

### Styling
- Primary color: `#004080` (dark blue) — used for headers, table headers, chatbot header
- Background: `#f9f9f9`
- Card background: `white` with `box-shadow: 0 2px 4px rgba(0,0,0,0.1)`
- Max content width: `900px`, centered
- Font: `Arial, sans-serif`

## Key Constraints

1. **No dependencies** — Do not introduce npm packages, CDN imports, or build tools without explicit project direction.
2. **Single file** — Unless restructuring is explicitly requested, keep all code in `index.html`.
3. **No backend** — This is a purely client-side app with no server-side logic.
4. **Crisis content is sensitive** — Any edits to crisis hotline numbers, labels, or links must be verified against current, accurate contact information.
5. **SAMHSA API is unauthenticated** — The API endpoint requires no key. Do not add authentication headers.

## Common Tasks

### Add a new clinic to the table
Edit the `<table class="resource-table">` block in the "Sports Psychology & Therapy Clinics" section. Follow the existing `<tr>` pattern: Clinic Name | Location | Specialty | Contact link.

### Add a new chatbot keyword
Extend the `if/else if` chain inside `getChatbotResponse()` in the Chatbot Script block.

### Change the SAMHSA API query (e.g., different state)
Update the `apiUrl` string inside `fetchMentalHealthResources()`. The API supports `state=XX` and `serviceType=` parameters.

### Add a new resource section
1. Add a `<div class="section">` block inside `<main>`.
2. The search functionality (`searchResources()`) will automatically include it since it queries all `.section` elements.

## Git Workflow

- **Main branch:** `main` (on remote `origin`)
- **Development:** Feature branches off `main`
- Commit messages follow the pattern: `Update index.html` (descriptive messages preferred)
- No CI/CD pipeline configured; deployment is manual static file hosting

## Deployment

The app can be hosted on any static file host (GitHub Pages, Netlify, Vercel, S3, etc.) by uploading `index.html`. No build step required.

For GitHub Pages: push to the `main` branch and enable Pages from the repository settings.
