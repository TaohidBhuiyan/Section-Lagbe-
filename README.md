# Section Lagbe

**Build a class routine that fits your semester.** Section Lagbe helps students compare course sections, set schedule preferences, and generate conflict-free routine options.

🌐 **Live app:** [sectionlagbe.netlify.app](https://sectionlagbe.netlify.app/)

## Features

- Load the bundled department schedule, upload a spreadsheet, or enter sections manually.
- Select courses and optionally prefer or lock faculty and sections.
- Set class-day limits, daily class limits, time preferences, and blocked periods.
- Generate, filter, compare, share, and export routine options.
- Use the responsive interface on desktop and mobile.

## Run locally

This is a static website with no build step.

1. Keep `index.html` and `preloaded-data.js` in the same folder.
2. Open `index.html` in a browser, or serve the project folder with any static web server.

The preloaded schedule is loaded from `preloaded-data.js` before the app starts. Keep that file beside `index.html` when moving or deploying the app.

## Update the preloaded schedule

Edit **`preloaded-data.js`**. You do not need to edit the app code in `index.html`.

The file contains two values:

- `window.SECTION_LAGBE_PRELOADED_DATA`: an array with one record for each course section.
- `window.SECTION_LAGBE_PRELOADED_UPDATED`: the date and time shown to users as the data update timestamp.

Each section record follows this format:

```js
{
  "id": 0,
  "type": "Theory",
  "course_code": "CSE 1111",
  "course_name": "Structured Programming Language",
  "section": "A",
  "faculty": "Faculty Name",
  "day": "Sat,Tue",
  "time": "8:30 AM - 9:50 AM",
  "room": "801"
}
```

### Data entry notes

- Add one record per section. Reuse the same course code and course name for all sections of that course.
- Give every record a unique numeric `id`.
- Use `Theory` or `Lab` for `type`.
- Use day abbreviations such as `Sat`, `Sun`, `Mon`, `Tue`, `Wed`, or `Thu`. For a section meeting twice weekly, separate days with a comma, such as `Sat,Tue`.
- Write `time` as a 12-hour range, for example `8:30 AM - 9:50 AM`.
- Use an empty string (`""`) when faculty or room is not known. Use `TBA` for an announced-to-be-determined faculty.
- Keep the JavaScript array syntax valid: records are separated by commas, and the last record has no trailing comma for broad browser compatibility.
- Update the timestamp after changing the schedule.

After editing, reload the app and choose **Preloaded Data** to confirm the new term's sections appear.

## Project structure

```text
.
├── index.html          # App interface, styles, and routine-generation logic
├── preloaded-data.js   # Bundled course-section schedule and update timestamp
└── README.md           # Project and maintenance guide
```
