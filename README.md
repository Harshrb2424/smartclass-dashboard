# SmartClass Display Dashboard

A lightweight and dynamic classroom dashboard built to be displayed on smart boards. It automatically pulls and displays the day's schedule, subject details, and syllabus content, along with an engaging wallpaper background. Fully configurable via a JSON file and supports offline use.

## Key Features

- Day-wise Class Timetable
- Subject Syllabus with Unit-wise Topics
- Faculty Details for Each Subject
- Dynamic Wallpaper Display
- Powered by a Simple JSON Schedule File
- Responsive for Smartboards and Displays

## Project Structure

```

SmartClass-Display/
├── images/             # Wallpapers or logos shown in the background
├── index.html          # Main UI template
├── schedule.json       # Timetable, subjects, syllabus, and topics
├── script.js           # Core logic for dynamic updates
├── styles.css          # Styles for layout and responsiveness

````

## How It Works

- `schedule.json` contains complete weekly data — each day includes multiple periods, and each period has:
  - `subject`
  - `timing`
  - `faculty`
  - `code`
  - `units` (List of unit titles)
  - `topics` (Nested arrays of topics per unit)

- On page load, `script.js` reads the current day (e.g., Monday) and updates the UI with corresponding classes.

- If a subject is scheduled, its details (like faculty name, units, and topics) are dynamically injected.

## Sample Schedule Structure (excerpt from `schedule.json`)

```json
{
  "schedule": {
    "Monday": [
      {
        "subject": "Software Testing Methodologies",
        "timing": "09:30-10:30",
        "code": "STM",
        "faculty": "Mrs. Anju Gopi",
        "units": ["Unit 1", "Unit 2", "Unit 3", "Unit 4", "Unit 5"],
        "topics": [
          [
            "Purpose of testing, model for testing, taxonomy of bugs",
            "Path testing, predicates, path sensitizing"
          ],
          ...
        ]
      },
      ...
    ],
    ...
  }
}
````

## Getting Started

1. Clone or download the repository.
2. Replace the contents of `schedule.json` with your own schedule and topics.
3. Add custom wallpapers to the `images/` folder.
4. Open `index.html` in a browser (or set as home screen on a smartboard browser).
5. You’re ready to go!

## Customization

* Add more subjects or change units/topics in `schedule.json`
* Modify theme in `styles.css`
* Add features like date-based notices or auto-refresh logic in `script.js`

## Update Cycle

This schedule data is typically updated every 6 months, but edits can be made anytime by updating `schedule.json`.

---

Made with ❤️ to improve learning spaces in classrooms.