# 📖 SEO Head Generator — Full Documentation

> Complete usage guide, API reference, and technical documentation.  
> Made with ❤️ by **Akash**

---

## 📌 Table of Contents

1. [Overview](#overview)
2. [Installation & Setup](#installation--setup)
3. [Getting a Free API Key](#getting-a-free-api-key)
4. [Using the Tool](#using-the-tool)
5. [Toggle Options Explained](#toggle-options-explained)
6. [Understanding the Output](#understanding-the-output)
7. [SEO Tag Reference](#seo-tag-reference)
8. [API Configuration](#api-configuration)
9. [Switching AI Providers](#switching-ai-providers)
10. [Troubleshooting](#troubleshooting)
11. [FAQ](#faq)

---

## 📋 Overview

**SEO Head Generator** is a browser-based tool that uses AI to analyze your webpage content and automatically generate a fully SEO-optimized `<head>` section.

### What It Solves
Writing SEO meta tags manually is tedious and error-prone. This tool:
- Reads your HTML content and understands what your page is about
- Generates all necessary SEO tags in seconds
- Enforces Google's recommended character limits (especially 150–155 chars for description)
- Creates structured data (Schema.org JSON-LD) automatically
- Generates Open Graph + Twitter Card tags for social sharing

### How It Works
```
Your HTML Content
       ↓
  AI Analysis (Groq LLaMA 3)
       ↓
  SEO Rules Applied
       ↓
  Generated <head> Tags
       ↓
  Copy & Paste into your site
```

---

## 🚀 Installation & Setup

### Requirements
- Any modern web browser (Chrome recommended)
- A free Groq API key
- A text editor (Notepad, VS Code, etc.)

### Steps

**Step 1 — Download the file**

Download `seo-head-generator.html` to your computer.

**Step 2 — Add your API key**

Open the file in a text editor. Find this section near the bottom inside `<script>`:

```js
// 🔑 PASTE YOUR GROQ API KEY BELOW
const API_KEY = "YOUR_GROQ_API_KEY_HERE";
```

Replace `YOUR_GROQ_API_KEY_HERE` with your actual Groq API key.

**Step 3 — Save and open**

Save the file. Double-click it to open in your browser.

That's it — no installation, no server, no npm required.

---

## 🔑 Getting a Free API Key

### Groq (Recommended — 100% Free)

1. Go to **[console.groq.com](https://console.groq.com)**
2. Click **"Sign in with Google"** (or create an account)
3. In the left sidebar, click **"API Keys"**
4. Click **"Create API Key"**
5. Give it a name (e.g., "SEO Tool")
6. Copy the key — it starts with `gsk_`

**Free tier limits:**
| Limit | Amount |
|-------|--------|
| Requests per minute | 30 |
| Requests per day | 14,400 |
| Tokens per minute | 6,000 |
| Credit card required | ❌ Never |

### Google Gemini (Alternative Free Option)

1. Go to **[aistudio.google.com](https://aistudio.google.com)**
2. Sign in with your Google account
3. Click **"Get API Key"** → **"Create API key in new project"**
4. Copy the key — it starts with `AIza`

> ⚠️ Note: Gemini free tier may not be available in all regions. If you get quota errors, use Groq instead.

---

## 🖥️ Using the Tool

### Step 1 — Add Your Content

**Option A: Upload a file**
- Click the upload area or drag & drop your HTML file
- Supported formats: `.html`, `.htm`, `.php`, `.txt`, `.jsx`, `.vue`
- The file contents will appear in the text area

**Option B: Paste code**
- Click inside the text area
- Paste your HTML content directly (`Ctrl+V`)

> 💡 Tip: You don't need to paste the entire page. Even pasting just the main content (headings, paragraphs) is enough for the AI to generate accurate tags.

### Step 2 — Add Canonical URL (Optional but Recommended)

In the **"Canonical URL"** field, enter the full URL of the page:
```
https://yourwebsite.com/your-page-slug
```

This tells search engines the definitive URL for this page and prevents duplicate content issues.

### Step 3 — Choose Which Tags to Generate

Use the toggle switches to turn specific tag types on or off. See [Toggle Options Explained](#toggle-options-explained) below.

### Step 4 — Generate

Click the **"✦ Generate SEO Head Tags"** button.

The AI will analyze your content and generate optimized tags in 2–5 seconds.

### Step 5 — Copy and Use

Click the **"📋 Copy"** button to copy all generated tags.

Paste them inside the `<head>...</head>` section of your HTML file, replacing or updating existing tags.

---

## 🎛️ Toggle Options Explained

| Toggle | Tag Generated | Purpose |
|--------|--------------|---------|
| **Title** | `<title>` | The clickable headline shown in Google search results. 50–60 chars. |
| **Description** | `<meta name="description">` | The text snippet shown under your title in search results. 150–155 chars. |
| **Keywords** | `<meta name="keywords">` | Comma-separated keywords. Less important for Google, still used by Bing. |
| **Author** | `<meta name="author">` | Name of the content author. Inferred from content or set to "Editorial Team". |
| **Canonical** | `<link rel="canonical">` | The preferred URL for this page. Prevents duplicate content penalties. |
| **Robots** | `<meta name="robots">` | Tells crawlers how to index the page. Default: `index, follow`. |
| **Publisher** | `<meta name="publisher">` | The brand or organization that published the content. |
| **Schema JSON-LD** | `<script type="application/ld+json">` | Structured data markup. AI auto-detects type (Article, WebPage, Product, etc.) |
| **OG Tags** | `<meta property="og:*">` | Open Graph tags for Facebook, LinkedIn, WhatsApp link previews. |
| **Twitter Card** | `<meta name="twitter:*">` | Twitter/X card for rich link previews when shared on Twitter. |

---

## 📊 Understanding the Output

### Metrics Bar (3 Cards)

After generation, three metric cards appear:

- **Tags Added** — Total number of HTML tags generated
- **Desc Length** — Character count of the meta description
- **Keywords** — Number of keywords in the keywords tag

### Description Length Meter

A progress bar shows how close your description is to the ideal length:

| Color | Meaning |
|-------|---------|
| 🟩 Teal/Green | Perfect! 150–155 characters |
| 🟨 Yellow | Too short (under 150 characters) |
| 🟥 Red | Too long (over 155 characters) |

> Google truncates descriptions over ~155 characters in search results. The AI is instructed to hit exactly 150–155 chars.

### Tag Status Chips

Colored pill badges confirm which tags were successfully generated:
- **Green chips** — Tag generated and verified (e.g., `Title ✓`, `Desc ✓`, `Schema`)
- **Purple chips** — Tag generated (e.g., `Canonical`, `Robots`, `Twitter`)
- **Yellow chips** — Tag generated but has a warning (e.g., description length off)

### Generated Code Box

The output box shows your complete, ready-to-use HTML head tags with:
- Proper HTML formatting
- Comments for organization
- Copy button (top-right corner)

---

## 🏷️ SEO Tag Reference

### Title Tag
```html
<title>Your Page Title Here — Brand Name</title>
```
- **Ideal length:** 50–60 characters
- **Best practice:** Primary keyword near the beginning
- **Avoid:** All caps, keyword stuffing, duplicate titles across pages

### Meta Description
```html
<meta name="description" content="Your page description here. Should be compelling, include the primary keyword, and be between 150 and 155 characters total.">
```
- **Ideal length:** 150–155 characters (including spaces)
- **Best practice:** Treat it as an ad — make it click-worthy
- **Avoid:** Duplicate descriptions, keyword stuffing, going over 155 chars

### Meta Keywords
```html
<meta name="keywords" content="keyword one, keyword two, keyword three">
```
- **Ideal count:** 8–12 keywords
- **Note:** Google ignores this tag, but Bing and some other engines still use it

### Robots Tag
```html
<meta name="robots" content="index, follow">
```
Common values:
| Value | Meaning |
|-------|---------|
| `index, follow` | Index page + follow all links (default) |
| `noindex, follow` | Don't index, but follow links |
| `index, nofollow` | Index page, don't follow links |
| `noindex, nofollow` | Don't index, don't follow links |

### Canonical Tag
```html
<link rel="canonical" href="https://yoursite.com/exact-page-url/">
```
- Always use the full URL including `https://`
- Should match exactly one version of the URL (with or without trailing slash — be consistent)

### Schema JSON-LD
```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Article",
  "headline": "Your Article Title",
  "author": { "@type": "Person", "name": "Author Name" },
  "datePublished": "2026-03-14",
  "description": "Article description here"
}
</script>
```
The AI auto-detects the correct schema type:
- `Article` — Blog posts, news articles
- `WebPage` — General pages
- `Product` — E-commerce product pages
- `Organization` — About/company pages
- `FAQPage` — FAQ pages

### Open Graph Tags
```html
<meta property="og:title" content="Page Title">
<meta property="og:description" content="Page description for social sharing">
<meta property="og:type" content="article">
<meta property="og:url" content="https://yoursite.com/page">
<meta property="og:image" content="https://yoursite.com/image.jpg">
```

### Twitter Card Tags
```html
<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:title" content="Page Title">
<meta name="twitter:description" content="Page description">
<meta name="twitter:image" content="https://yoursite.com/image.jpg">
```

---

## ⚙️ API Configuration

The API configuration is at the top of the `<script>` section in the HTML file:

```js
// ── Groq API Configuration ──────────────────────────────────
// 🔑 PASTE YOUR GROQ API KEY BELOW
const API_KEY = "YOUR_GROQ_API_KEY_HERE";

// Groq API endpoint — OpenAI-compatible format
const GROQ_API = "https://api.groq.com/openai/v1/chat/completions";
```

### Changing the Model

To use a different Groq model, find this line in the fetch block:

```js
model: 'llama-3.3-70b-versatile',
```

Available Groq models:
| Model | Speed | Quality | Best For |
|-------|-------|---------|----------|
| `llama-3.3-70b-versatile` | Fast | ⭐⭐⭐⭐⭐ | Best quality (default) |
| `llama-3.1-8b-instant` | ⚡ Fastest | ⭐⭐⭐ | Quick generations |
| `mixtral-8x7b-32768` | Fast | ⭐⭐⭐⭐ | Good alternative |

---

## 🔄 Switching AI Providers

### Switch to Google Gemini

Change the config block to:

```js
const API_KEY = "YOUR_GEMINI_KEY_HERE"; // from aistudio.google.com
```

Change the fetch block to use:

```js
const geminiUrl = `https://generativelanguage.googleapis.com/v1beta/models/gemini-2.0-flash:generateContent?key=${API_KEY}`;

const response = await fetch(geminiUrl, {
  method: 'POST',
  headers: { 'Content-Type': 'application/json' },
  body: JSON.stringify({
    contents: [{ parts: [{ text: systemPrompt + '\n\n' + prompt }] }],
    generationConfig: { maxOutputTokens: 1000, temperature: 0.7 }
  })
});

const output = data.candidates?.[0]?.content?.parts?.[0]?.text || '';
```

---

## 🔧 Troubleshooting

### ✕ "Generation failed: Failed to fetch"
**Cause:** The AI provider's API blocks browser-side requests (CORS).  
**Fix:** Switch to Groq — it fully supports browser calls.

### ✕ "You exceeded your current quota"
**Cause:** Your API key's free quota is exhausted.  
**Fix:** 
1. Wait 24 hours for quota to reset
2. Create a new API key in a new project
3. Switch to Groq (more generous free limits)

### ✕ "Invalid API Key" / 401 Unauthorized
**Cause:** The API key is wrong or has expired.  
**Fix:** Double-check you copied the full key including the `gsk_` prefix. Generate a new key if needed.

### ✕ Description length is wrong
**Cause:** The AI occasionally miscounts characters.  
**Fix:** The generation prompt strictly instructs 150–155 chars. If it's off, click Generate again — the result varies slightly each time.

### Page looks broken / unstyled
**Cause:** Google Fonts may be blocked on your network.  
**Fix:** Open the file in Chrome with an internet connection. The fonts load from Google's CDN.

### File upload not working
**Cause:** Browser security restrictions on local files.  
**Fix:** Open the file via a local server OR use the paste method instead. In VS Code, use the Live Server extension.

---

## ❓ FAQ

**Q: Does this tool need an internet connection?**  
A: Yes — it needs to connect to the Groq API to generate tags. The UI itself works offline.

**Q: Is my content sent to third parties?**  
A: Your content is sent to Groq's API for processing. Do not use this tool with confidential or sensitive content.

**Q: Can I use this for multiple pages?**  
A: Yes! Just paste new content and click Generate again for each page.

**Q: Why is my description sometimes 148 or 157 characters?**  
A: AI models don't count characters exactly. The prompt enforces 150–155 chars, but there may be slight variation. Re-generate if needed or manually trim/expand the output.

**Q: Does it work with React / Vue / non-HTML content?**  
A: Yes! Paste any content — the AI reads the text and understands what the page is about regardless of format.

**Q: Can I host this on a website?**  
A: Yes, but never expose your API key publicly. For a hosted version, you'd need a backend proxy to keep the key secure.

**Q: Which browsers are supported?**  
A: Chrome, Edge, Firefox, Safari (latest versions). Chrome is recommended for best compatibility.

---

## 📜 Changelog

| Version | Changes |
|---------|---------|
| 1.0 | Initial release with Anthropic Claude |
| 1.1 | Added footer & code comments |
| 1.2 | Switched to OpenAI GPT-4o |
| 1.3 | Switched to Google Gemini 2.0 Flash |
| 1.4 | Switched to Groq LLaMA 3.3 (current) |

---

Made with ❤️ by **Akash**
