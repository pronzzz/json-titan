# JSON-Titan 🚀

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Version](https://img.shields.io/badge/version-1.0.0-green.svg)
![Status](https://img.shields.io/badge/status-active-success.svg)
![Platform](https://img.shields.io/badge/platform-web-orange.svg)

**JSON-Titan** is a high-performance, browser-based JSON viewer and analyzer designed to handle **massive JSON files** (up to gigabytes) with ease. Built with modern web technologies, it runs entirely in your browser, ensuring your data never leaves your device.

## ✨ Key Features

*   **⚡ Massive File Support**: specific optimizations (chunking, web workers, virtual scrolling) allow loading and navigating multi-gigabyte JSON files without crashing the browser.
*   **🔍 Advanced Search**: Integrated **JQ** support allows for powerful filtering, transforming, and querying of your JSON data.
*   **🆚 Diff View**: Compare two JSON files side-by-side with a synchronized, visual diff tool that highlights additions, deletions, and modifications.
*   **📊 Data Visualization**: Instantly generate charts and graphs from array data within your JSON structure.
*   **🔒 Privacy First**: Zero server-side processing. All analysis happens locally on your machine.
*   **🎨 Polished UI**: A modern, responsive interface with Dark/Light mode support, easy navigation, and keyboard shortcuts.

## 🚀 Getting Started

### Installation
JSON-Titan is designed as a **single-file application** for maximum portability.

1.  **Clone the repository**:
    ```bash
    git clone https://github.com/pronzzz/json-titan.git
    ```
2.  **Open `index.html`**:
    Simply double-click `index.html` to open it in your modern web browser (Chrome, Firefox, Edge, Safari).

### Usage

1.  **Load Data**: Drag and drop a JSON file onto the landing zone, or click to browse your local files.
2.  **Navigate**: Use the tree view to expand/collapse nodes. Use `Arrow Keys` to navigate the list efficiently.
3.  **Search**: Use the global search bar to filter keys and values instantly.
4.  **JQ Console**: Open the console drawer (bottom) to run complex JQ queries on your data.
    *   *Example*: `.users[] | select(.age > 25)`
5.  **Diff Mode**: Click the "Diff Mode" button in the header, then drag/drop two files to see the differences.
6.  **Export**: Export your filtered view or modified data back to a file.

## 🛠️ Technology Stack

*   **Core**: Vanilla JavaScript (ES6+), HTML5, CSS3
*   **Styling**: Tailwind CSS (via CDN)
*   **Processing**: Web Workers for non-blocking parsing and diffing
*   **Query Engine**: jq-web (WASM)
*   **Visualization**: Chart.js

## 📂 Project Structure

```
json-titan/
├── index.html        # Main application file (bundled logic)
├── LICENSE           # MIT License
├── CONTRIBUTING.md   # Contribution Guidelines
└── README.md         # Documentation
```

## 🤝 Contributing

Contributions are welcome! Please check out [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines on how to get started.

## 📄 License

This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details.

---
*Built with ❤️ by Pranav Dwivedi*
