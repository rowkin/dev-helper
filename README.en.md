# DevHelper - Developer Toolbox

> A Chrome extension customized for developers, integrating 17 essential tools including JSON formatting, encoding/decoding, API testing, code formatting, and more. Features built-in **AI Interpretation** and a standalone **AI Assistant** to boost development efficiency.

[![Chrome Extension](https://img.shields.io/badge/Chrome-Extension-blue?logo=googlechrome)](https://github.com/rowkin/dev-helper)
[![Manifest V3](https://img.shields.io/badge/Manifest-V3-green)](https://developer.chrome.com/docs/extensions/mv3/)

---

## ✨ Features

### 🛠️ Developer Tools (17 Tools)

| Tool | Description | AI Integration |
| :--- | :--- | :--- |
| **JSON Formatter** | Beautify, compress, validate, and escape JSON | ✅ AI Structure analysis |
| **Encode/Decode** | URL / Base64 / Unicode / HTML Entities | ✅ AI Auto-recognition |
| **JWT Parser** | Three-section split, expiration detection, payload analysis | ✅ AI Security analysis |
| **Timestamp** | Real-time clock, bidirectional conversion, world timezones | ✅ AI Interpretation |
| **API Tester** | Lightweight API client supporting Headers/Body/Params | ✅ AI Response analysis |
| **Code Beautifier** | Formatter for JS, CSS, HTML, JSON, SQL | ✅ AI Code reading |
| **Regex Tester** | Real-time matching, flags, common regex cheatsheet | ✅ AI Explanation |
| **UUID Generator** | UUID v4 / NanoID / Snowflake ID batch generation | ✅ AI explanation |
| **Password Generator** | Secure password generator, strength evaluation | ✅ AI Safety suggestions |
| **Hash Calculator** | MD5 / SHA-1 / SHA-256 / SHA-512 | ✅ AI Interpretation |
| **Color Converter** | HEX / RGB / HSL / HSV conversion, high precision native EyeDropper screen & tab color picker | — |
| **QR Code** | Generate and decode QR codes with custom styles | — |
| **JSON Diff** | Visualize differences between two JSON objects | ✅ AI Diff analysis |
| **Radix Converter** | Conversions between 2 and 36 bases | — |
| **Image Base64** | Bidirectional conversion between images and Base64 | — |
| **Markdown Editor** | GFM syntax, Mermaid diagram rendering, side-by-side preview | ✅ AI Writing assistant |
| **Page Performance Monitor** | Web Vitals scoring, network timing waterfall charts, local diagnostic tips | ✅ AI Expert diagnostics |

### 🤖 AI Assistant & Split-screen Architecture

- **Beautiful Dual-column Home**: The overview navigation dashboard is split into a 70/30 golden ratio, featuring tools on the left and a resident **AI Assistant** chat panel on the right.
- **Model Switching**: Easily switch between `🤖 Chrome Built-in AI` (Gemini Nano) and `🌐 Custom API` from the dropdown in the chat header.
- **Auto Environment Check & Download Polling**:
  - Automatically guides the configuration of Chrome Flags if Built-in AI is not enabled or the model is still downloading.
  - Automatically copies component names to the clipboard and polls Chrome components status every 2.5s until ready.
- **Markdown Rendering in Chat**: Full support for code highlighting, headings, and lists during streaming.

---

## 🚀 Installation & Usage

### Method 1: Chrome Web Store (Recommended 🌟)

Install directly from the store to enable automatic updates and configuration sync:
👉 [**Get DevHelper on Chrome Web Store**](https://chromewebstore.google.com/detail/dobgahhmdodeeondedoikibehhmnalie)

### Method 2: Manual Installation (Developer/Offline Mode)

1. Download the latest release zip file from [dev-helper/releases](https://github.com/rowkin/dev-helper/releases) and unzip it.
2. Open Chrome and go to `chrome://extensions`.
3. Enable **"Developer mode"** in the top right corner.
4. Click **"Load unpacked"** in the top left corner.
5. Select the unzipped folder.

### Method 3: Build from Source

1. Clone the repository:
   ```bash
   git clone https://github.com/rowkin/DevHelper.git
   ```
2. Run build script under the project root:
   ```bash
   npm run build
   ```
3. The build output will be stored in `dist/` (e.g., `dev-helper-v1.2.0.zip`).
4. Load the unpacked zip or directory in Chrome.

### 💡 Shortcuts

Press `Alt+Shift+D` (or `Option+Shift+D` on macOS) to quickly toggle the DevHelper popup.

---

## ⚙️ AI Configuration

Click the **"AI Settings"** button in the header of any tool page to configure:

### Chrome Built-in AI (Gemini Nano)

- Requires Chrome version 127 or newer.
- Might require downloading the model component on first use.
- Runs entirely locally on your machine, no API key needed.

### Custom OpenAI Compatible Endpoint

```text
API URL: https://api.openai.com/v1/chat/completions
API Key: sk-xxxx
Model Name: gpt-4o-mini
```

Supports any standard OpenAI Compatible API (e.g., standard API proxy, self-hosted LLM endpoints).

---

## 📁 Project Structure

```text
DevHelper/
├── manifest.json          # Chrome extension MV3 manifest
├── popup.html             # Popup popup page
├── background.js          # Service Worker background script
├── README.md              # Chinese README
├── README.en.md           # English README
├── CHANGELOG.md           # Change log
│
├── styles/
│   ├── popup.css          # Popup style
│   └── common.css         # Shared styles for tools
│
├── js/
│   ├── popup.js           # Popup routing and management
│   ├── ai-service.js      # Unified AI agent service
│   └── common.js          # Shared methods (Navbar, AI Panel)
│
├── pages/
│   ├── ai-assistant.html  # Standalone AI assistant page
│   ├── page-timing.html   # Page Performance Monitor
│   └── ... (Other tools)
│
└── icons/                 # Icons in various sizes
```

---

## 🔒 Permissions

| Permission | Purpose |
| :--- | :--- |
| `tabs` | Open tools in new tabs |
| `storage` | Save AI configurations, favorites, and usage histories |
| `activeTab` | Get current active page information for API client / tab detection |
| `scripting` | Inject content scripts for performance evaluation |
| `clipboardWrite` | Enable quick copy buttons |

No unnecessary tracking or telemetry. Network permissions are only used for your configured LLM API calls and active API tester calls.

---

## 📄 License

© 2026 79team. Built for internal developers and open-source contributors.
