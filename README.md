[Leer en espanol](README.es.md)

# InnovateStart

A static Single-Page Application (SPA) portal for an entrepreneurship and innovation ecosystem. Built with vanilla HTML5, CSS3, and JavaScript, this project serves as an informational landing site for a startup accelerator program called InnovateStart.

---

## Features

- **Single-Page Application** — Hash-based routing loads page content dynamically without full reloads. Navigation feels smooth and fast.
- **5 Themed Pages:**
  - **Home** — Hero banner, feature cards (mentoring, networking, funding, training, legal advice, digital marketing), and stats section.
  - **Information** — Detailed explanations of Lean Startup, Design Thinking, and Agile Scaling methodologies.
  - **Gallery** — Image gallery with captions and an embedded YouTube video.
  - **Pricing** — Comparison table with four plans: Basic (free), Pro ($49), Enterprise ($199), and Premium ($499).
  - **Contact** — Validated contact form with real-time feedback and character counter.
- **Reusable Components** — Header (navbar) and footer are loaded dynamically from separate HTML files via JavaScript.
- **Responsive Design** — Custom CSS with three breakpoints ensures usability on mobile, tablet, and desktop.
- **Client-side Form Validation** — Real-time validation with visual feedback (Bootstrap `is-invalid` class) and a success alert on submission.
- **Accessibility** — Semantic HTML5 elements (`<section>`, `<article>`, `<aside>`, `<figure>`, `<figcaption>`), `aria-label` attributes, and visually-hidden text for screen readers.

---

## Tech Stack

| Technology | Purpose |
|---|---|
| **HTML5** | Semantic page structure |
| **CSS3** | Custom styling, animations, responsive layout |
| **JavaScript (ES6+)** | SPA routing, dynamic component loading, form validation |
| **Bootstrap 5.3** | UI components, grid system, utility classes (loaded via CDN) |
| **Font Awesome 6.4** | Icons (loaded via CDN) |

---

## Project Structure

```
innovate-start/
├── components/
│   ├── header.html          # Shared navigation bar
│   └── footer.html          # Shared footer with links and copyright
├── css/
│   └── style.css            # Custom styles (variables, typography, responsive)
├── img/                     # Image assets
│   ├── 1.png
│   ├── 2.jpg
│   ├── 3.webp
│   ├── 4.jpg
│   ├── 5.png
│   └── 6.jpg
├── js/
│   ├── script.js            # SPA router, form validation, page title updates
│   └── components.js        # Loads header and footer HTML dynamically
├── pages/
│   ├── home.html            # Landing page content
│   ├── informacion.html     # Methodologies information page
│   ├── galeria.html         # Image gallery page
│   ├── tabla.html           # Pricing comparison table page
│   └── contacto.html        # Contact form page
├── index.html               # Main entry point (SPA shell)
├── README.md                # This file
└── README.es.md             # Spanish version of this README
```

---

## Getting Started

### Prerequisites

You need a local HTTP server to run this project. The JavaScript `fetch()` API does not work with the `file://` protocol, so opening `index.html` directly in a browser will not load the content.

### Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/EmaConor/-mi-portal.git
   cd -mi-portal
   ```

2. **Start a local server** using one of these methods:

   **Option A — Python (recommended):**

   ```bash
   python -m http.server 8000
   ```

   **Option B — VS Code Live Server:**

   Install the "Live Server" extension, right-click `index.html`, and select "Open with Live Server".

   **Option C — Node.js (npx):**

   ```bash
   npx serve .
   ```

3. **Open in your browser:**

   ```
   http://localhost:8000
   ```

---

## Usage

### Navigation

The application uses hash-based routing (e.g., `http://localhost:8000/#/informacion`). Click any navigation link in the header to switch pages without a full reload.

### Routes

| Hash Route | Page |
|---|---|
| `#/` | Home |
| `#/informacion` | Information |
| `#/galeria` | Gallery |
| `#/tabla` | Pricing |
| `#/contacto` | Contact |

### Contact Form

Fill in the required fields (name, email, interest, message, and terms agreement). The form validates input in real time. On successful submission, a green alert confirms the message was sent.


