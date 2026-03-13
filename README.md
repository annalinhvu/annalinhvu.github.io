# Anna (Linh) Vu — Portfolio

**[annalinhvu.github.io/portfolio](https://annalinhvu.github.io/portfolio)**

Personal portfolio and lab projects. Built with vanilla HTML, CSS, and JavaScript — no frameworks, no build step, fully static.

---

## Lab Projects

### 01 — Film Festival Tracker
> Documentary and experimental film festivals worldwide.

Deadlines, submission fees, acceptance rates, and past selections — everything in one place to plan smarter submissions. Filter by type (documentary / experimental), region, tier, and premiere requirement.

- **Stack:** Python · SQLite · Vanilla JS

---

### 02 — Analog Film Stock Database
> Price tracking, availability, and lab locations for analog film stocks.

Browse film stocks with current pricing across vendors, availability status, and ISO/format specs. Paired with a directory of development labs, searchable by process (C-41, E-6, B&W, ECN-2) and format.

- **Stack:** Python · SQLite · Vanilla JS

---

### 03 — NYC Film Scene Map
> An interactive map of New York's experimental film world.

Screening venues, workshops, labs, galleries, and community spaces — all in one place. Filter by category and borough. Built for anyone trying to find their people in the NYC film community.

- **Stack:** Python · SQLite · Leaflet.js · Vanilla JS

---

### 04 — Only Good Things
> A browsable catalog of self-care activities.

Inspired by the *Only Good Things* wall calendar. Activities across 6 categories (body, mind, creative, nature, nourish, rest), filterable by season, duration, setting, and difficulty. Track completions and view your progress — all stored locally in your browser.

- **Stack:** Python · SQLite · Vanilla JS

---

## Running Locally

All projects are static files — no API servers needed.

```bash
git clone https://github.com/annalinhvu/portfolio.git
cd portfolio
python3 -m http.server 8080
```

Open [http://localhost:8080](http://localhost:8080).

---

## Architecture

Each lab project was originally backed by a FastAPI + SQLite server. They've since been converted to fully static deployments:

- Seed data lives in `seed_data.py`
- `export_json.py` in each project regenerates the static JSON from the seed data
- The frontend fetches from `data/*.json` at load time
- Write operations (completions in the self-care app) use `localStorage`

This makes everything hostable on GitHub Pages with zero backend.

---

## Stack

| Layer | Tools |
|---|---|
| Frontend | Vanilla HTML · CSS · JavaScript |
| Data | Python · SQLite |
| Maps | Leaflet.js |
| Hosting | GitHub Pages |
