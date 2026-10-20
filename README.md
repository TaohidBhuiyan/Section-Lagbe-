<div align="center">

# ⚡ Section Lagbe?
### *Smart, Conflict-Free Course Routine Planner for UIU Students*

[![Live Demo](https://img.shields.io/badge/Live%20App-sectionlagbe.netlify.app-22c55e?style=for-the-badge&logo=netlify&logoColor=white)](https://sectionlagbe.netlify.app/)
[![UIU Semester](https://img.shields.io/badge/UIU-Fall%202026-10b981?style=for-the-badge)](https://sectionlagbe.netlify.app/)
[![Department](https://img.shields.io/badge/Dept-BSCSE%20%7C%20BSDS-38bdf8?style=for-the-badge)](https://sectionlagbe.netlify.app/)
[![Zero Dependencies](https://img.shields.io/badge/Dependencies-Zero%20(Pure%20JS)-f59e0b?style=for-the-badge)](https://sectionlagbe.netlify.app/)
[![License](https://img.shields.io/badge/License-MIT-purple?style=for-the-badge)](LICENSE)

<br/>

**Section Lagbe?** is an ultra-fast, intuitive web app designed to eliminate advising stress. Instead of juggling dozens of course codes, section clashes, and faculty initials on paper or spreadsheets, Section Lagbe calculates all mathematically possible conflict-free schedules in seconds.

[**Explore Live App »**](https://sectionlagbe.netlify.app/) · [Report Bug](https://github.com/TaohidBhuiyan/Section-Lagbe-/issues) · [Request Feature](https://github.com/TaohidBhuiyan/Section-Lagbe-/issues)

</div>

---

## ✨ Key Features

| Feature | Description |
| :--- | :--- |
| ⚡ **Preloaded Schedule** | Bundled with official **UIU Fall 2026** course offering (790+ sections across **BSCSE** and **BSDS**). |
| 🎯 **Instant Conflict Resolution** | Real-time combinatorial search engine tests thousands of permutations to find clash-free routine options. |
| 🧬 **BSDS & BSCSE Separation** | Data Science courses and specialized sections (`BA`, `BB`, etc.) are clearly tagged and segregated from CSE sections. |
| 🔒 **Faculty Preference, Lock & Avoid** | Prefer (✓), must-have lock (🔒), or completely avoid/exclude (🚫) unwanted faculty sections from routines. |
| ⏳ **Personalized Routine Preferences** | Specify max days per week, early morning vs afternoon classes, gap minimization, and blocked slots (prayer/break times). |
| 📊 **18-Credit Limit Guard** | Real-time credit summation based on verified course catalog values to avoid over/under advising. |
| 📱 **Responsive & Themed** | Fluid mobile and desktop layout with modern Light and Dark Forest themes. |
| 📤 **One-Click Export** | Download your finalized routine as an image/PDF or copy a shareable link. |

---

## 🚀 How It Works

```
   ┌──────────────────┐       ┌──────────────────┐       ┌──────────────────┐
   │  1. Pick Courses │ ───>  │ 2. Set Criteria  │ ───>  │  3. Get Routine  │
   │  Preloaded / CSV │       │  Locks & Limits  │       │  Compare & Save  │
   └──────────────────┘       └──────────────────┘       └──────────────────┘
```

1. **Load Schedule**: Jump straight in with preloaded **UIU Fall 2026** data, upload your own `.csv`/`.xlsx` file, or input sections manually.
2. **Select Courses**: Check off the theory and lab courses you plan to take. Expand cards to filter by faculty or pin preferred sections.
3. **Configure Preferences**: Choose preferred days, maximum classes per day, or block unwanted time slots.
4. **Generate & Compare**: Flip through conflict-free schedule combinations, review weekly timetable grids, and save the routine that fits your lifestyle.

---

## 💻 Quick Start / Local Development

Section Lagbe is built with vanilla web technologies — **no Node.js build step, no compiler, and zero dependencies required.**

### 1. Clone the repository
```bash
git clone https://github.com/TaohidBhuiyan/Section-Lagbe-.git
cd Section-Lagbe-
```

### 2. Run locally
You can open `index.html` directly in your browser, or launch a lightweight local server:

```bash
# Python 3
python -m http.server 8000

# or Node.js (npx)
npx serve .
```

Open `http://localhost:8000` in your browser.

---

## 🛠️ Schedule Maintenance (`preloaded-data.js`)

When a new semester starts or the university updates section offerings, you can update the bundled dataset without touching `index.html`.

### Record Structure
Each section inside `window.SECTION_LAGBE_PRELOADED_DATA` is an object:

```javascript
{
  "id": 0,
  "type": "Theory",                   // "Theory" or "Lab"
  "course_code": "CSE 1111",          // Course Code
  "course_name": "Structured Programming Language", // Append (BSDS) for Data Science courses
  "section": "A",                     // Section name (e.g., A, B, BA, BB)
  "faculty": "Faculty Full Name",     // "TBA" if unassigned
  "day": "Sat,Tue",                   // Comma-separated: "Sat,Tue", "Sun,Wed", or single "Wed"
  "time": "8:30 AM - 9:50 AM",        // 12-hour format range
  "room": "801"                       // Room number or lab
}
```

### Update Timestamp
At the bottom of `preloaded-data.js`, set:
```javascript
window.SECTION_LAGBE_PRELOADED_UPDATED = 'October 20, 2026, 7:25 PM';
```

---

## 📂 Project Architecture

```text
Section-Lagbe/
├── index.html          # Application engine, styles, UI components, and routine algorithm
├── preloaded-data.js   # Bundled UIU department section catalog & updated timestamp
└── README.md           # Documentation & contributor guide
```

---

## 🤝 Contributing

Contributions, feedback, and suggestions are welcome!
1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/NewFeature`)
3. Commit your Changes (`git commit -m 'Add NewFeature'`)
4. Push to the Branch (`git push origin feature/NewFeature`)
5. Open a Pull Request

---

## 📄 License & Credits

Distributed under the **MIT License**.

Crafted with ❤️ by **[Taohid Bhuiyan](https://github.com/TaohidBhuiyan)** for students of **United International University (UIU)**.
