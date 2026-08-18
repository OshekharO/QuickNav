# QuickNav - Open Source Directory

![QuickNav Banner](https://img.shields.io/badge/QuickNav-Directory-82a4ea?style=for-the-badge) 
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![GitHub issues](https://img.shields.io/badge/Contributions-Welcome-brightgreen.svg)](https://github.com/OshekharO/QuickNav/issues)
[![GitHub stars](https://img.shields.io/github/stars/OshekharO/QuickNav?style=social)](https://github.com/OshekharO/QuickNav)

A lightning-fast, highly customizable, and privacy-first start page and web directory. QuickNav is designed to replace your browser's default new tab page with a clean, modern interface that organizes your favorite sites and search engines.

[**View Live Demo**](https://stacker.bond)

---

## ✨ Key Features

- **Zero Dependencies:** Built entirely with a single HTML file using vanilla JavaScript, Tailwind CSS (via CDN), and Lucide Icons. No build step required.
- **Privacy First:** No tracking, no analytics, no telemetry. Your data stays entirely local in your browser.
- **Fully Customizable:** 
  - Switch between Light and Dark mode.
  - Toggle between a detailed card layout or a sleek Compact View.
  - Open links in the current or a new tab.
- **Smart Search:** Real-time local site filtering with instant results, plus web search fallback on Enter.
- **Keyboard Shortcuts:** Press `Cmd/Ctrl + K` to instantly focus the search bar.
- **Flawless Drag & Drop:** Reorder your sites effortlessly using SortableJS. Fully responsive and supports touch gestures on mobile devices. Your custom order is saved automatically.
- **Loading Experience:** Smooth skeleton loader while data fetches, with graceful error handling.
- **Smart Icon Resolution:** Automatically fetches the best icon for a site based on its URL (using Google's S2 favicon service) or falls back to a massive library of built-in vector icons.
- **GitHub Actions Integration:** Adding or editing a site through the UI automatically generates a perfectly formatted GitHub Issue, triggering an automated Pull Request workflow to update the directory.
- **Accessibility:** ARIA labels, keyboard navigation, and Escape key support for modals and dropdowns.
- **Responsive:** Optimized for all screen sizes with mobile-first design.

---

## 📂 Directory Categories

QuickNav includes **108 curated sites** across **10 categories**:

- **Common** - Popular and frequently used sites
- **#Resources** - Tools, utilities, job search, and reference materials
- **#Forums** - Discussion communities, developer forums, and boards
- **#Technology** - Tech news, Linux, open-source, and infrastructure
- **#Development** - Coding, documentation, and developer tools
- **#Servers** - Hosting, VPS, and cloud platforms
- **#Ai** - Artificial intelligence tools and assistants
- **#Domains** - Free domains, subdomains, and DNS services
- **#Email** - Encrypted and privacy-focused email providers
- **#Cloud Storage** - File storage and collaboration platforms

---

## 🚀 Getting Started

### Installation

Because QuickNav is a static frontend application, deploying your own instance is incredibly simple.

1. **Fork or Clone the repository:**
    ```bash
    git clone https://github.com/OshekharO/QuickNav.git
    ```

2. **Serve the files:**
    You can serve the directory using any basic web server, or simply open `index.html` in your browser.
    ```bash
    npx serve .
    ```
    *Or deploy instantly to Vercel, Netlify, or GitHub Pages.*

---

## ⚙️ Configuration

All sites, categories, and search engines are powered by a single JSON file located at `public/data.json`.

### Adding a Site
To manually add a site, edit the `sites` array in `public/data.json`:

```json
{
  "id": "1",
  "title": "GitHub",
  "desc": "Platform for hosting and collaborating on software projects.",
  "url": "https://github.com",
  "category": "development",
  "icon": "github"
}
```

*Note: The `icon` field is optional. If omitted, QuickNav will attempt to automatically resolve the site's favicon.*

### Available Icons
QuickNav uses [Lucide Icons](https://lucide.dev/). Any icon name from their library can be used in the `icon` field.

---

## 🛠️ Automated PR Workflow

QuickNav includes a built-in GitHub Actions workflow (`.github/workflows/process-suggestions.yml`). 

When a user submits a site via the frontend UI, it redirects them to open a GitHub Issue. When a repository maintainer adds the `approved` label to that issue, the workflow automatically:
1. Parses the issue body.
2. Updates `public/data.json`.
3. Opens a new Pull Request with the changes.

---

## 🤝 Contribution Guidelines

Contributions are always welcome! Whether it's adding a new feature, fixing a bug, or suggesting a new site for the default directory.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

If you simply want to add a site to the directory, use the **Add New Site** button directly on the live website to generate an issue!

---

## 📝 License

Distributed under the MIT License. See `LICENSE` for more information.

---

## 💬 Support & Contact

If you encounter any issues or have questions, please feel free to [open an issue](https://github.com/OshekharO/QuickNav/issues) on GitHub.
