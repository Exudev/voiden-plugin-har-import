> A community plugin for [Voiden](https://github.com/VoidenHQ) — the developer-first API client.

# Voiden HTTP Archive (HAR) Importer Plugin

Import HTTP Archive (`.har`) files captured from browser Developer Tools or network proxies and automatically convert them into organized, native Voiden `.void` request collections.

[![Release Plugin](https://github.com/Exudev/voiden-plugin-har-import/actions/workflows/release.yml/badge.svg)](https://github.com/Exudev/voiden-plugin-har-import/actions/workflows/release.yml)
[![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)](https://github.com/Exudev/voiden-plugin-har-import/releases)

---

## ✨ Features

- **Browser Network Captures**: Import `.har` and HAR-formatted `.json` files directly into Voiden.
- **Smart Organization**: Automatically creates folders matching page titles or domain hostnames.
- **Full Request Fidelity**:
  - Headers (`headers-table` blocks)
  - Cookies and Authorization details
  - Query parameters (`query-table` blocks)
  - HTTP Methods (GET, POST, PUT, DELETE, PATCH, OPTIONS, HEAD, etc.)
  - Request Bodies:
    - JSON (`json_body` blocks)
    - XML (`xml_body` blocks)
    - Form Data (`multipart-table` blocks)
    - URL-encoded (`urlencoded-table` blocks)
    - Plain Text
- **Static Asset Filtering**: Option to filter out images, CSS stylesheets, JavaScript files, fonts, and media assets during import.
- **Progress Tracking & Cancellation**: Real-time progress bar with one-click cancellation.
- **Safe Batch Creation**: Throttled write pipeline to maintain application responsiveness on large captures.

---

## 📦 Installation

### In Voiden
1. Open **Voiden**.
2. Navigate to **Extensions / Plugins** in the sidebar.
3. Search for **HTTP Archive (HAR) Importer** in the Community tab and click **Install**.

---

## 🚀 Usage

1. In Google Chrome, Firefox, Safari, or Edge DevTools, go to the **Network** tab.
2. Perform your API requests and click **Export HAR** / **Save all as HAR with content**.
3. In Voiden, open the `.har` file or click the **Import HAR Collection** button in the sidebar.
4. (Optional) Check or uncheck **Ignore static assets**.
5. Click **Generate Voiden files**.

---

## 🛠️ Development & Building

```bash
# Install dependencies
npm install

# Run tests
npm test

# Build plugin bundle
npm run build
```

The build output will be generated into `dist/har-import.js` alongside `manifest.json` and `changelog.json`.

---

## 📄 License

MIT © [Exudev](https://github.com/Exudev)
