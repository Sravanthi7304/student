# Student Dashboard

A responsive student dashboard built with HTML, CSS and JavaScript in a single file. It uses a clean white and light blue theme.

**Live preview:** https://sravanthi7304.github.io/student/

**Author:** Sravanthi

## Features

- Summary cards: total courses, pending assignments, attendance and CGPA
- Course list with progress bars
- Upcoming tasks with checkboxes; ticking a task marks it done and updates the pending count
- Due dates calculated from today's date (Today, Tomorrow, or a date such as 24 Oct)
- Weekly timetable
- Recent results table
- Announcements
- Student profile information
- Quick links that scroll to the matching section
- Responsive layout: the sidebar becomes a scrolling top bar on phones, and tables scroll sideways on small screens
- Accessible markup: `nav` landmark, labelled progress bars and checkboxes, visible keyboard focus, reduced-motion support

## Getting started

1. Download `index.html`.
2. Double-click it to open it in any modern browser (Chrome, Edge, Firefox, Safari).

No installation, build step or internet connection is needed.

## Project structure

```
index.html   # HTML, CSS (inside <style>) and JavaScript (inside <script>)
README.md
```

To split it into separate files, move the contents of `<style>` into `style.css` and the contents of `<script>` into `script.js`, then link them:

```html
<link rel="stylesheet" href="style.css">
<script src="script.js"></script>
```

## Customising

**Student details:** edit the name, course, semester, section and ID in the `Student Information` section and the welcome line in the header.

**Courses:** edit the `courses` array in the script. Each entry is `["Course name", progressPercent]`.

```js
const courses = [["Data Science", 75], ["Machine Learning", 60]];
```

**Tasks:** edit the `tasks` array. `off` is the number of days from today until the task is due (`0` = today, `1` = tomorrow, `-1` = overdue).

```js
const tasks = [{ t: "AI seminar", d: "Prepare seminar notes.", off: 5 }];
```

**Timetable, results and announcements:** edit the table rows and notice blocks directly in the HTML.

**Colours:** change the CSS variables at the top of the `<style>` block.

```css
--accent: #2b7bc4;      /* buttons, progress bars, tags */
--accent-soft: #e3f1fd; /* light blue highlights */
--side: #d6ebfb;        /* sidebar background */
--bg: #f4f9fe;          /* page background */
```

## Notes

- Courses, tasks, timetable and results contain sample data. Replace them with your real information.
- Task completion is not saved; refreshing the page resets the checkboxes.

## Possible improvements

- Save task progress with `localStorage`
- Load data from a JSON file or API
- Add a login page
- Add an attendance chart

## Tech stack

HTML5, CSS3 (custom properties, grid, flexbox) and vanilla JavaScript.

## Author

**Sravanthi**
B.Tech CSE (AIML), Mohan Babu University

- Live preview: https://claude.ai/artifact/1zxyeRgMES2sk7WeVJRp7x
