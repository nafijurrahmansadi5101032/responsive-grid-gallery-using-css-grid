# Responsive CSS Grid Gallery

A modern, responsive masonry-style image gallery built using pure CSS Grid with dynamic span placement and dense packing algorithms.

---

## 🌟 Overview

This project showcases the power and flexibility of **CSS Grid Layout** without external frameworks or JavaScript. It dynamically organizes images of varying proportions (standard, vertical, horizontal, and large feature tiles) into a gapless layout using CSS Grid's `grid-auto-flow: dense` property.

---

## ✨ Features

- **Pure CSS Layout:** Built entirely with vanilla HTML5 and CSS3.
- **Adaptive Auto-Placement:** Uses `grid-auto-flow: dense` to automatically backfill empty gaps in the grid.
- **Fluid & Responsive:** Adjusts columns automatically to fit any viewport size using `auto-fit` and `minmax()`.
- **Dynamic Tile Spanning:**
  - **Standard:** Default $1 \times 1$ grid unit.
  - **Vertical:** Spans across 2 rows (`grid-row: span 2`).
  - **Horizontal:** Spans across 2 columns (`grid-column: span 2`).
  - **Big / Feature:** Spans across a $2 \times 2$ block (`grid-column: span 2; grid-row: span 2`).
- **Aspect Ratio Integrity:** Uses `object-fit: cover` to preserve image quality without stretching or distorting aspect ratios.

---

## 🗂 Project Structure

```text
├── index.html         # Gallery semantic markup
├── styles.css         # Grid styling and responsive rules
├── images/            # Image assets
│   ├── normal*.jpg
│   ├── vertical*.jpg
│   ├── horizontal*.jpg
│   └── big*.jpg
└── README.md          # Project documentation
```

---

## 🚀 Getting Started

### Prerequisites

All you need is a modern web browser (Google Chrome, Firefox, Safari, Edge).

### Running Locally

1. **Clone the repository:**
   ```bash
   git clone https://github.com/your-username/responsive-grid-gallery.git
   ```

2. **Navigate to the project folder:**
   ```bash
   cd responsive-grid-gallery
   ```

3. **Open the project:**
   - Double-click `index.html` to open it in your default browser, or
   - Serve it using VS Code's **Live Server** extension.

---

## 🛠 Key CSS Concepts Demonstrated

```css
.container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(100px, 1fr));
  grid-auto-flow: dense;
  gap: 3px;
}
```

* **`repeat(auto-fit, minmax(100px, 1fr))`**: Dynamically computes the maximum number of columns that can fit the viewport width, with each item at least `100px` wide and expanding evenly via fractional units (`1fr`).
* **`grid-auto-flow: dense`**: Fills empty gaps created by larger multi-column or multi-row tiles with smaller subsequent elements.

---

## 📄 License

This project is open-source.
