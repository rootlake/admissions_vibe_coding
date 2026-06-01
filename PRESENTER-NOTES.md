# Presenter Notes — GBS Admissions Workshop

Private cheat sheet. Not projected.

---

## Funnel dashboard in 30 seconds

407 inquiries from a CRM export (Veracross-style). Each chart answers a question leadership asks in committee:

| Chart | What it means |
|-------|---------------|
| **Pipeline status** | Where each inquiry sits today — Inactive Inquiry, Application Incomplete, Enrolled, etc. Big bar = bottleneck. |
| **World map** | Geographic reach of your applicant pool. |
| **Grades** | Entry points (9th, 10th, 11th, 12th). |
| **Sports** | Athletic recruiting overlap (students can list multiple). |
| **Monthly timeline** | When inquiries spike — visit season, deadlines. |
| **Financial aid** | How many families asked about aid. |
| **Grade slider** | Filters everything by entry grade. |

---

## Lost-to dashboard in 30 seconds

528 records of students who did not enroll. Fictional school names in demo data.

| Chart | What it means |
|-------|---------------|
| **Top competitors** | Schools your admits chose instead — competitive intel. |
| **Gender split** | Demographics of lost students. |
| **Status donut** | Not Enrolling vs Application Withdrawn vs Declined Waitlist. |
| **Gender toggle** | See if competitor mix shifts by gender. |

---

## Talk arc (what to say when)

1. **Slide 2** — This deck = Claude Design. Fast, beautiful, hits limits on data projects.
2. **Slide 4** — Pre-built funnel. "Spreadsheet in, dashboard out." Open in new tab for full screen.
3. **Slide 2** — Quick poll: ChatGPT / Claude / Gemini / Other (show of hands).
4. **Slide 6** — Sanitize first. Before/after chip + fake-data note for demos.
5. **Slide 7** — Live Canvas demo. Edit prompt on slide; fake data, plain English.
6. **Slide 8** — DATA + CHARTS + STYLE pattern.
7. **Slide 9** — Alt-tab to Cursor. iframe = lost-to artifact.
8. **Slide 10** — Five takeaways (fragments).

---

## Safe answers

| Question | Answer |
|----------|--------|
| Is this FERPA-safe? | Only if you sanitize first — remove names, IDs; use aggregates. |
| Can it connect to our CRM? | Not live today. Export CSV monthly, sanitize, then prompt. |
| Can my team use this? | Yes — share the HTML file or print the report. |
| What if they ask for a column we don't have? | "Great — add it to the sanitized export, then one line in the prompt." |

---

## What NOT to do live

- Paste raw xlsx with student names into public AI
- Promise real-time CRM integration
- Re-identify individuals from aggregates

---

## If embed fails

Open directly: `demos/funnel.html` or `demos/lost-to.html` in a new tab.
