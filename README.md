# 🔍 SEO Head Generator

> AI-powered tool that analyzes your HTML content and auto-generates a fully optimized `<head>` section — titles, meta tags, schema markup, Open Graph, Twitter Cards, and more.

![SEO Head Generator](https://img.shields.io/badge/AI-Groq%20LLaMA%203-00A67E?style=for-the-badge&logo=meta)
![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)
![HTML](https://img.shields.io/badge/Built%20With-HTML%2FJS-orange?style=for-the-badge&logo=html5)
![Free](https://img.shields.io/badge/API-Free%20%F0%9F%86%93-brightgreen?style=for-the-badge)

---

## ✨ Features

- 📄 **Upload or Paste** — Drag & drop HTML files or paste code directly
- 🤖 **AI-Powered** — Uses Groq's LLaMA 3.3 70B model for smart SEO generation
- 🏷️ **10 Tag Types** — Toggle exactly which tags to generate
- 📏 **Description Meter** — Live character count (enforces 150–155 chars)
- 📊 **SEO Metrics** — Shows tag count, keyword count, and description quality
- 📋 **One-Click Copy** — Copy the entire generated head section instantly
- 🌐 **No Server Needed** — Single HTML file, runs entirely in your browser
- 💸 **Free API** — Works with Groq's free tier (no credit card required)

---

## 🚀 Quick Start

### 1. Get a Free API Key
Go to [console.groq.com](https://console.groq.com) → Sign in with Google → **API Keys** → **Create API Key**

Copy the key (starts with `gsk_...`)

### 2. Add Your Key
Open `seo-head-generator.html` in any text editor and find:

```js
const API_KEY = "YOUR_GROQ_API_KEY_HERE";
```

Replace with your key:

```js
const API_KEY = "gsk_xxxxxxxxxxxxxxxxxxxx";
```

### 3. Open & Use
Save the file → Double-click to open in **Chrome** → Done! ✅

---

## 🏷️ Generated Tags

| Tag | Description | SEO Rule |
|-----|-------------|----------|
| `<title>` | Page title | 50–60 characters |
| `<meta name="description">` | Page summary | **150–155 characters exactly** |
| `<meta name="keywords">` | Target keywords | 8–12 comma-separated |
| `<meta name="author">` | Content author | Inferred from content |
| `<meta name="robots">` | Crawler instructions | `index, follow` |
| `<meta name="publisher">` | Publisher/brand | Inferred from content |
| `<link rel="canonical">` | Canonical URL | Use your page URL |
| `<script type="application/ld+json">` | Schema markup | Auto-detects type |
| Open Graph tags | Social sharing (Facebook/LinkedIn) | Full og: set |
| Twitter Card tags | Twitter sharing | `summary_large_image` |

---

## 📸 Screenshot

```
┌─────────────────────────────────────────────────────────────┐
│  S  SEO Head Generator   AI-Powered Meta Tag Optimizer      │
├──────────────────────────┬──────────────────────────────────┤
│  ● INPUT                 │  ● GENERATED OUTPUT              │
│                          │                                  │
│  [ Drop or paste HTML ]  │  Title ✓  Desc ✓  Schema ✓     │
│                          │                                  │
│  [ Textarea ]            │  Tags: 14  Desc: 152  KW: 10    │
│                          │                                  │
│  Canonical URL           │  ████████████████░  152/155     │
│  [________________]      │                                  │
│                          │  <!-- SEO Head Tags -->          │
│  Title        [ON ]      │  <title>Your Page Title</title>  │
│  Description  [ON ]      │  <meta name="description"...     │
│  Keywords     [ON ]      │  <meta name="keywords"...        │
│  ...                     │  ...                             │
│                          │                    [ 📋 Copy ]   │
│  [ ✦ Generate Tags ]     │                                  │
└──────────────────────────┴──────────────────────────────────┘
```

---

## 🛠️ Tech Stack

- **Frontend:** Vanilla HTML, CSS, JavaScript (no frameworks)
- **AI Model:** Groq — LLaMA 3.3 70B Versatile
- **Fonts:** Syne (UI) + JetBrains Mono (code)
- **API:** Groq REST API (OpenAI-compatible format)

---

## 🔑 Supported AI Providers

This project has been built for multiple providers. Switch by editing the API config:

| Provider | Model | Free? | CORS Safe? |
|----------|-------|-------|------------|
| **Groq** ✅ (current) | LLaMA 3.3 70B | ✅ Yes | ✅ Yes |
| Google Gemini | gemini-2.0-flash | ✅ Yes | ✅ Yes |
| OpenAI | gpt-4o | ❌ Paid | ❌ No |
| Anthropic | claude-sonnet | ❌ Paid | ❌ No |

---

## 📁 Project Structure

```
seo-head-generator/
│
└── seo-head-generator.html    # Complete app — single file
```

Everything is in one self-contained HTML file. No dependencies, no build step, no npm.

---

## ⚙️ Configuration

All config is at the top of the `<script>` section:

```js
// 🔑 Your API key
const API_KEY = "YOUR_GROQ_API_KEY_HERE";

// API endpoint
const GROQ_API = "https://api.groq.com/openai/v1/chat/completions";
```

---

## 📄 License

MIT License — free to use, modify, and distribute.

---

## 👨‍💻 Author

Made with ❤️ by **Akash**

---

## 🌟 Support

If this helped you, give it a ⭐ on GitHub!
