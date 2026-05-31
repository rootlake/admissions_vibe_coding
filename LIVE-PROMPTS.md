# Live Prompts — GBS Admissions Workshop

Copy-paste pack for live demos. **Never paste raw spreadsheet rows** — use the sanitized JSON below.

---

## Tier 0 — Sanitize (run locally, not in public chat)

```
Remove all names and student IDs from this admissions export.
Output ONLY these aggregates as JSON I can paste into a public AI tool:
- count by admission status
- top 10 countries
- grade distribution (9th–12th)
- top 8 athletic interests (split comma-separated lists)
- inquiries by month from inquiry_submit_date
- financial aid requested Yes/No split
No row-level data. No names.
```

---

## Sanitized aggregate JSON (safe to paste)

```json
{
  "meta": {
    "title": "Admissions Pipeline \u2014 2026\u20132027",
    "recordCount": 407,
    "sanitized": true
  },
  "status": {
    "Inactive Inquiry": 172,
    "Application Withdrawn": 6,
    "Inquiry Completed": 34,
    "Application Incomplete": 42,
    "Enrolled": 55,
    "Remain On Waitlist": 22,
    "Waitlisted": 7,
    "Parent Declined": 20,
    "Applicant": 17,
    "Earlywithdrawal": 4,
    "Denied": 21,
    "Wait One Year": 1,
    "Review In Progress": 4,
    "Declined Waitlist": 1,
    "Inquiry": 1
  },
  "country": {
    "United States": 116,
    "Germany": 37,
    "China": 30,
    "Brazil": 28,
    "Spain": 19,
    "Canada": 13,
    "Bahamas": 11,
    "Jamaica": 10,
    "Italy": 9,
    "Turkey": 8
  },
  "grade": {
    "9th": 125,
    "10th": 112,
    "11th": 128,
    "12th": 42
  },
  "sports": {
    "Tennis": 125,
    "Swimming/Diving": 120,
    "Basketball": 110,
    "Soccer": 106,
    "Volleyball": 83,
    "Track and Field": 80,
    "Golf": 71,
    "Football": 59
  },
  "months": {
    "2021-12": 1,
    "2023-01": 1,
    "2023-09": 1,
    "2023-12": 1,
    "2024-07": 1,
    "2024-08": 1,
    "2024-11": 1,
    "2024-12": 6,
    "2025-01": 3,
    "2025-02": 5,
    "2025-03": 3,
    "2025-04": 12,
    "2025-05": 5,
    "2025-06": 7,
    "2025-07": 21,
    "2025-08": 20,
    "2025-09": 23,
    "2025-10": 29,
    "2025-11": 38,
    "2025-12": 45,
    "2026-01": 63,
    "2026-02": 23,
    "2026-03": 19,
    "2026-04": 16,
    "2026-05": 5
  },
  "aid": {
    "Yes": 137,
    "No": 92
  },
  "mapPoints": [
    {
      "country": "United States",
      "count": 116,
      "lat": 39.8283,
      "lng": -98.5795
    },
    {
      "country": "Germany",
      "count": 37,
      "lat": 51.1657,
      "lng": 10.4515
    },
    {
      "country": "China",
      "count": 30,
      "lat": 35.8617,
      "lng": 104.1954
    },
    {
      "country": "Brazil",
      "count": 28,
      "lat": -14.235,
      "lng": -51.9253
    },
    {
      "country": "Spain",
      "count": 19,
      "lat": 40.4637,
      "lng": -3.7492
    },
    {
      "country": "Canada",
      "count": 13,
      "lat": 56.1304,
      "lng": -106.3468
    },
    {
      "country": "Bahamas",
      "count": 11,
      "lat": 25.0343,
      "lng": -77.3963
    },
    {
      "country": "Jamaica",
      "count": 10,
      "lat": 18.1096,
      "lng": -77.2975
    },
    {
      "country": "Italy",
      "count": 9,
      "lat": 41.8719,
      "lng": 12.5674
    }
  ]
}
```

---

## STYLE block (swap when audience suggests their colors)

```
STYLE & BRANDING:
- Our school colors are [PRIMARY] and [SECONDARY] (e.g. crimson #8B0000 and charcoal #2D2D2D).
- Use gradients and shades of [PRIMARY] as the main theme; [SECONDARY] for headers and accents.
- Background: light neutral. Text: dark, high contrast.
- Typography: serif titles + sans body (or match our marketing site).
- Optional: pull hex codes from our website / viewbook / brand guidelines.
- Do NOT use stock photos of people.
- Add a one-line plain-English subtitle under each chart for admissions staff.
- Footer: "Aggregates only — no student names."
```

**Presets:** Classic navy `#0F2A4A` + gold `#C2A14D` · Crimson `#8B0000` + black · Forest `#1B4332` + sand `#F4E8D1` · Modern blue `#2563EB` + gray-white

---

## Tier 1 — Canvas one-off (slide 6 — all three tools)

Paste into ChatGPT Canvas, Claude Artifacts, and Gemini Canvas:

```
Build one self-contained HTML page with Chart.js and Leaflet from this sanitized aggregate JSON:

[PASTE JSON FROM ABOVE]

CHARTS (each needs a plain-English subtitle):
1. Admission status bar — "Where inquiries sit in the pipeline"
2. World map, circle markers sized by count — "Where families are from"
3. Grade doughnut — "Grades applying for"
4. Top sports horizontal bar — "Athletic interests"
5. Monthly inquiry line chart — "When inquiries arrive"
6. Financial aid donut — "Aid requests"

STYLE & BRANDING:
- Our school colors are crimson #8B0000 and charcoal #2D2D2D.
- Use gradients and shades of crimson as the main theme.
- Clean, board-meeting ready. Inter + JetBrains Mono fonts.

Add a grade filter slider (9th–12th + All) that updates all charts.
Single file, no backend, works offline from file://.
Title: "Admissions Pipeline — sanitized demo data".
Include a Print report button.
```

---

## Tier 1b — Field audience requests

| If they ask… | Paste this |
|--------------|------------|
| "Use our colors — red and black" | Replace STYLE block only; keep data and charts |
| "Add yield / conversion" | `Add a summary card: enrolled ÷ total inquiries as % yield.` |
| "Boarding vs day" | `We'd need a boarding/day column in the export first — show a sample 70/30 split as placeholder.` |
| "Compare to last year" | `Add a dashed line series labeled "Prior cycle (sample)".` |
| "Printable for head of school" | `Add @media print CSS: one page, hide slider, date stamp in footer.` |
| "Lost-to / competitors" | Use lost-to JSON below + lost-to prompt |
| "International vs domestic" | `Add a US vs international toggle using the country field.` |

---

## Tier 1c — Meta-prompting (takeaway #4)

After building the funnel in Cursor:

```
Look at demos/funnel.html and the aggregate data structure.
Write a reusable prompt that would recreate this dashboard from sanitized JSON only.
Include: chart list with plain-English subtitles, STYLE block placeholder, grade slider, print button.
Output the prompt only — no code.
```

Follow-up:

```
Shorten that prompt to under 200 words. Keep DATA / CHARTS / STYLE sections.
```

---

## Tier 2 — Cursor (slide 8)

See `cursor-handoff.md` for the full sequence. Short version:

1. Set up project structure; raw data in `data-source/` only
2. Compute aggregates → `demos/data/funnel-data.js` → `demos/funnel.html`
3. Compute lost-to aggregates → `demos/data/lost-to-data.js` → `demos/lost-to.html`
4. Wire embeds in `index.html`

**Re-skin prompt:**

```
Restyle demos/lost-to.html: our colors are [X] and [Y].
Keep all data and chart logic. Update CSS and chart colors only.
```

---

## Lost-to aggregate JSON (second dataset)

```json
{
  "meta": {
    "title": "Where Admits Go Instead \u2014 'Lost To'",
    "recordCount": 528,
    "sanitized": true
  },
  "schools": {
    "Moonridge Collegiate School": 33,
    "Ravencrest College Preparatory": 31,
    "Dawnspire Academy": 27,
    "Thornfield Preparatory Institute": 23,
    "Ironwood Collegiate": 23,
    "Falconmere Preparatory": 19,
    "Crownfield Preparatory School": 19,
    "Valecrest Preparatory": 17,
    "Sunvale Preparatory Academy": 16,
    "Northlight Collegiate School": 16,
    "Larkhaven Preparatory": 13,
    "Foxglove Academy": 13,
    "Emberwick Preparatory": 13,
    "Highspire Preparatory School": 12,
    "Skylark Preparatory": 12
  },
  "gender": {
    "Male": 295,
    "Female": 233
  },
  "status": {
    "Not Enrolling": 511,
    "Application Withdrawn": 8,
    "Declined Waitlist": 6,
    "Waitlisted": 1,
    "Denied": 2
  },
  "byGender": {
    "Male": {
      "Ravencrest College Preparatory": 21,
      "Moonridge Collegiate School": 20,
      "Dawnspire Academy": 16,
      "Ironwood Collegiate": 14,
      "Crownfield Preparatory School": 12,
      "Elderglen Preparatory School": 11,
      "Valecrest Preparatory": 10,
      "Wintermere School": 9,
      "Skylark Preparatory": 9,
      "Northlight Collegiate School": 9,
      "Falconmere Preparatory": 9,
      "Larkhaven Preparatory": 8,
      "Public School": 7,
      "Stormwatch Academy": 7,
      "Mythvale Collegiate": 7
    },
    "Female": {
      "Thornfield Preparatory Institute": 18,
      "Moonridge Collegiate School": 13,
      "Dawnspire Academy": 11,
      "Falconmere Preparatory": 10,
      "Sunvale Preparatory Academy": 10,
      "Ravencrest College Preparatory": 10,
      "Ironwood Collegiate": 9,
      "Emberwick Preparatory": 9,
      "Nightwell Academy": 9,
      "Foxglove Academy": 8,
      "Northlight Collegiate School": 7,
      "Valecrest Preparatory": 7,
      "Highspire Preparatory School": 7,
      "Crownfield Preparatory School": 7,
      "Crystalgate Academy": 6
    }
  }
}
```

**Lost-to Canvas prompt:**

```
Build a self-contained HTML page with Chart.js from this sanitized JSON: [paste lost-to JSON above]
- Horizontal bar: top 15 competitor schools — subtitle "Schools our admits chose instead"
- Gender doughnut — subtitle "Who we're losing"
- Status doughnut — subtitle "Not enrolling vs withdrew vs waitlist"
- Gender toggle buttons (All / Male / Female) filter the bar chart

STYLE: forest green #1B4332, sand #F4E8D1, copper #B5651D accents. Sans-forward.
Single file, no backend. Print button. Footer: aggregates only.
```
