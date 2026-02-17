# Week 2 – Configuration-Driven Website System

## 1. Overview

In Week 2, I implemented a configuration-driven website system.  
The goal was to create a webpage that dynamically reads settings from a JSON file and applies them using JavaScript.

Instead of hardcoding layout, navigation, and colors directly in HTML, the website structure is controlled by external configuration files.

---

## 2. Project Structure

The project is organized as follows:

project/
├── config/
│ ├── site-config.json
│ ├── site-config-blog.json
│ ├── site-config-portfolio.json
│ └── site-config-business.json
│
├── frontend/
│ ├── index.html
│ ├── styles/main.css
│ └── scripts/config-loader.js
│
└── docs/
└── week2/
└── config-system.md


- The **config folder** contains all JSON configuration files.
- The **frontend folder** contains HTML, CSS, and JavaScript files.
- The **docs folder** contains documentation for Week 2.

---

## 3. How the Configuration System Works

1. When the page loads, `config-loader.js` fetches a JSON configuration file.
2. The JSON file contains:
   - Site name
   - Layout type (single-column or two-column)
   - Sidebar position
   - Navigation menu items
   - Color settings
3. JavaScript dynamically:
   - Sets the page title
   - Builds the navigation menu
   - Applies layout classes
   - Applies color themes

This allows the same HTML template to generate multiple different website styles.

---

## 4. Different Configurations Created

To demonstrate configurability, I created three additional configuration files:

### 1. Blog Configuration
- Single-column layout
- Blog-related navigation items
- Different color scheme

### 2. Portfolio Configuration
- Two-column layout
- Sidebar on the right
- Portfolio-related navigation items
- Unique color theme

### 3. Business Configuration
- Two-column layout
- Sidebar on the left
- Business-related menu items
- Professional color scheme

Each configuration file transforms the website without modifying the HTML structure.

---

## 5. Screenshots

(Screenshots of each configuration applied should be added here.)

Example:

### Blog Layout
![Blog Layout](screenshots/blog-layout.png)

### Portfolio Layout
![Portfolio Layout](screenshots/portfolio-layout.png)

### Business Layout
![Business Layout](screenshots/business-layout.png)

---

## 6. Challenges Faced

- Handling correct file paths when using fetch()
- Debugging "Cannot GET" errors in Live Server
- Managing folder structure correctly
- Understanding DOM manipulation

---

## 7. Key Learnings

- How to use fetch() to load JSON files
- How to dynamically manipulate the DOM using JavaScript
- The importance of separating structure from configuration
- How real-world content management systems (CMS) use configuration-based approaches

---

## 8. Conclusion

This week helped me understand how a single template can generate multiple website layouts using configuration files.  
The system improves scalability, maintainability, and reusability of code.
