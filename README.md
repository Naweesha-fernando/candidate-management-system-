# Workforce — Candidate Management System

Responsive HTML, CSS and vanilla JavaScript implementation of the Workforce Figma wireframes.

## Open the application

Download or clone this repository, then open `index.html` in a browser. For the best document-storage behaviour, run a local web server:

```bash
python3 -m http.server 8080
```

Visit `http://localhost:8080`. No build step or runtime dependencies are required.

## Screens and interactions

- Manager login screen: show/hide password, remember email and demo entry.
- Overview: live totals derived from the sample employee records.
- Employees: name/email/ID search and status filtering; no CSV import.
- Find workers: profession, city/postcode, minimum experience, skills and availability-status filters. No shift-preference filter.
- Add/edit employee: personal and contact information, date of birth with calculated age, profession, experience, skills, qualifications, employment history and availability preferences.
- Documents: attach multiple PDF, DOC or DOCX files (up to 10 MB each), retain them in this browser, and download them from profiles or the documents screen.
- Employee profile: overview, experience and skills, availability, documents and saved internal notes.
- Availability: editable current-week grid with a Save changes button; no coverage summary or quick-update panels.
- Additional reports and demo settings screens.
- Responsive desktop/mobile layouts, visible keyboard focus, labelled form inputs and live status feedback.

## Important: front-end prototype

**This is a browser-only demonstration, not a production employee database.**

The login form accepts any sample email and password; it does not authenticate a real user. Passwords are not stored or sent anywhere. Remember email stores only the entered email address. The demo routes are freely accessible.

Employee records and notes are saved in localStorage. Document bytes are saved in IndexedDB on the same browser and origin. They are not uploaded to GitHub or a server. Clearing browser data deletes those records/files. Use fictional data only. The public repository contains only fictional seed data.

Location search is a case-insensitive city/postcode text match, not geocoded radius search. Availability status filters the employee's general status. The current-week planner stores dated week-specific entries separately from typical availability; it does not infer date-range availability or change employee status automatically.

Password recovery is an explanatory demo dialog; it sends no emails. Real authentication, role permissions, shared database storage, secure document uploads, server validation, audit trails, notifications and geographic/date-range matching require a backend before live use.

The CSS loads the Figma font, `42dot Sans`, from Google Fonts, with Arial/sans-serif as an offline fallback. No remote images or temporary Figma URLs are used.

## GitHub Pages

The files can be hosted as a static demo on GitHub Pages. In the repository, open **Settings → Pages**, select **Deploy from a branch**, choose **main** and **/ (root)**, then save. This publishes only the front-end demo; it does not add a backend or secure login.

## Project files

- `index.html` — accessible document shell
- `styles.css` — responsive layout, design tokens and controls
- `app.js` — sample data, navigation and browser interactions

## Design

Based on the approved [Workforce Figma wireframes](https://www.figma.com/design/6h4NG9xcTgeTNpUva1isUt).
