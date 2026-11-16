# Classroom Visual Schedule

A dynamic, single-page visual schedule built for classroom displays and interactive smartboards. It highlights the active block of the school day in real time, supports flexible specialist rotations, and saves daily edits directly in the browser.

**Live Site:** [vs.calebspring.com](https://vs.calebspring.com/)

## Features

* **Real-Time Block Highlighting:** Automatically tracks the system clock (updating every 5 seconds) and highlights the active time column across six structured blocks of the school day (7:45 AM to 2:10 PM).
* **Clock Simulation Mode:** Includes a header time picker to preview how the schedule looks at any point in the day, plus a **Live Clock** button to snap back to the current time.
* **Customizable Specialist Rotations:** Supports dual-slot specialist cards during morning blocks with dropdown selectors for **Music**, **Library**, **P.E.**, and **+ AAC**, dynamically rendering matching SVG icons.
* **Editable Sub-Activity Times & Notes:** Lets staff adjust individual sub-activity time labels and type custom notes directly into specialist slots.
* **Zero-Backend Persistence:** Automatically saves all specialist selections, notes, and custom time ranges to the browser's `localStorage` (`classroom_schedule_data_v3`), keeping changes intact across refreshes without needing an account or server.
* **Single-File Architecture:** Built entirely with vanilla HTML, CSS, and JavaScript in a single `index.html` file with zero external dependencies.

## Daily Schedule Structure

| Block | Time Window | Activities |
| :--- | :--- | :--- |
| **1. Morning Routine** | 7:45 AM – 8:30 AM | Arrival, Breakfast, Morning Meeting |
| **2. Morning Block A** | 8:35 AM – 9:55 AM | Specialists (4 customizable slots), Work Time |
| **3. Morning Block B** | 9:55 AM – 10:45 AM | Specialists (4 customizable slots), Work Time |
| **4. Midday Break** | 11:05 AM – 11:45 AM | Lunch, Recess |
| **5. Centers** | 11:45 AM – 1:00 PM | Cooking, Art, Puzzles / Games, Reading |
| **6. Afternoon Wrap-Up** | 1:00 PM – 2:10 PM | Recess, Snack, Class Jobs, Dismissal |

## Project Files

* `index.html` — Complete application markup, responsive grid styling, embedded SVG icons, and client-side scheduling logic.
* `CNAME` — Custom domain configuration for GitHub Pages (`vs.calebspring.com`).
* `README.md` — Project documentation.

## Running Locally or Deploying

Because the app has no build step or external dependencies, you can run or host it anywhere:

1. **Local Use:** Clone or download the repository and open `index.html` in any modern web browser.
2. **GitHub Pages:** Push changes to the `main` branch to deploy automatically via GitHub Pages.

## Customizing Time Blocks

To change the main column time windows that trigger automatic highlighting, update the `data-start` and `data-end` attributes on each `.schedule-col` element in `index.html` using minutes past midnight (for example, `465` = 7:45 AM, `850` = 2:10 PM).
