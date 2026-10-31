# Universals

A suite of simple, privacy-friendly browser multi-tools that execute simultaneous actions across services in new tabs.

🌐 **Live Website**: [https://vasilisplavos.github.io/universals/](https://vasilisplavos.github.io/universals/)

![Dark Mode](https://img.shields.io/badge/theme-dark-1a1a1a) ![Light Mode](https://img.shields.io/badge/theme-light-f5f5f5) ![Zero Dependencies](https://img.shields.io/badge/dependencies-none-brightgreen)

---

## 🛠️ Included Solutions

### 1. Universal Search (`/search/`)
Search multiple search engines simultaneously with a single query.
- **18 Search Engines**: Google, DuckDuckGo, YouTube, Wikipedia (EN/NL), Startpage, Google Images, Maps, Drive, Wolfram Alpha, Google Translate, etc.
- **Categorized Selection**: General Search, Audiovisual, and Tools.
- **Customizable**: Toggle engines individually or by category.

### 2. Universal Paywalls (`/paywalls/`)
Open any article URL across multiple public web archives, cache services, and bypass/clean reader views in parallel tabs.
- **Supported Providers**:
  - **Archive.ph** (`https://archive.ph/newest/`)
  - **Wayback Machine** (`https://web.archive.org/web/`)
  - **Google Cache** (`https://webcache.googleusercontent.com/search?q=cache:`)
  - **12ft.io** (`https://12ft.io/`)
  - **RemovePaywall.com** (`https://www.removepaywall.com/search?url=`)
  - **smry.ai** (`https://smry.ai/`)
  - **1ft.io** (`https://1ft.io/`)
  - **RemovePaywalls.com** (`https://removepaywalls.com/`)
- **Auto-Formatting**: Automatically handles URLs entered with or without `https://`.
- **Customizable**: Choose which providers you want to query each time.

---

## ✨ Shared Features

- **Hub Navigation**: Central landing page to launch either tool with top-bar navigation between them.
- **Dark & Light Mode**: Seamless theme toggle synced across the hub and all tools via `localStorage`.
- **Preferences Saved**: Your selected engines and providers persist between visits.
- **Zero Dependencies**: Pure HTML, CSS, and vanilla JavaScript. No trackers, no cookies, no frameworks.
- **Staggered Opening**: Smart popup delay to minimize aggressive browser blocking.

---

## 🚀 Usage

### Universal Search
1. Open the [Universal Search](https://vasilisplavos.github.io/universals/search/) page.
2. Select your desired search engines.
3. Enter your search query.
4. Press **Enter** or click **"search in tabs"**.

### Universal Paywalls
1. Open the [Universal Paywalls](https://vasilisplavos.github.io/universals/paywalls/) page.
2. Select which bypass or archive providers you'd like to test.
3. Paste the paywalled article URL (e.g. `https://plavos.com/article`).
4. Press **Enter** or click **"unlock in tabs"**.

---

## 🔗 URL Query Parameters & Quick Launch

You can prefill forms directly through the URL, making it easy to create browser bookmarks, extensions, or Alfred/Raycast shortcuts:

### Pre-fill Universal Paywalls
Pass any article link with `?url=` directly to the paywalls tool:
```text
https://vasilisplavos.github.io/universals/paywalls/?url=https://example.com/article
```

### Pre-fill Universal Search
Pass your search term with `?q=` directly to the search tool:
```text
https://vasilisplavos.github.io/universals/search/?q=my+search+query
```

---

## ⚠️ Browser Permissions (Important)

These tools open multiple tabs at once upon user action. When using for the first time:
- Your browser might show a popup blocked indicator in the address bar.
- Click it and choose **"Always allow popups and redirects from this site"**.

---

## 📁 Repository Structure

```text
universals/
├── index.html          # Hub landing page
├── search/
│   └── index.html      # Universal Search tool
├── paywalls/
│   └── index.html      # Universal Paywalls tool
├── .nojekyll           # GitHub Pages bypass Jekyll
└── README.md
```

---

## 📄 License

MIT
