# Anna (Linh) Vu — Portfolio

**[annalinhvu.github.io/portfolio](https://annalinhvu.github.io/portfolio)**

Personal portfolio and a collection of lab projects built out of curiosity and care. No frameworks, no build step, fully static.

---

## Lab Projects

### 01 - Film Festival Tracker
> Documentary and experimental film festivals worldwide.

Deadlines, submission fees, acceptance rates, and past selections in one place to plan smarter submissions. Filter by type (documentary / experimental), region, tier, and premiere requirement.

- **Stack:** HTML, JSON, Vanilla JS

---

### 02 - Analog Film Stock Database
> Price tracking, availability, and lab locations for analog film stocks.

Browse film stocks with current pricing across vendors, availability status, and ISO/format specs. Paired with a directory of development labs, searchable by process (C-41, E-6, B&W, ECN-2) and format.

- **Stack:** HTML, JSON, Vanilla JS

---

### 03 - NYC Film Scene Map
> An interactive map of New York's experimental film world.

Screening venues, workshops, labs, galleries, and community spaces. Filter by category and borough. Built for anyone trying to find their people in the NYC film community.

- **Stack:** HTML, JSON, Leaflet.js

---

### 04 - Auteurs
> A personal index of filmmakers.

100 filmmakers filterable by era and nationality.

- **Stack:** HTML, JSON

---

### 05 - Only Good Things
> A browsable catalog of self-care activities.

Inspired by the *Only Good Things* wall calendar. Activities across 6 categories (body, mind, creative, nature, nourish, rest), filterable by season, duration, setting, and difficulty. Track completions locally in your browser.

- **Stack:** HTML, JSON, Vanilla JS

---

### 06 - Com Nha
> 175 Vietnamese recipes from Mien Bac, Mien Trung, and Mien Nam.

Browse by region or category, search by ingredient, and save favorites. Each region has its own color identity throughout the UI.

- **Stack:** HTML, JSON, Vanilla JS

---

## Running Locally

```bash
git clone https://github.com/annalinhvu/portfolio.git
cd portfolio
python3 -m http.server 8080
```

Open [http://localhost:8080](http://localhost:8080).

---

## Architecture

All lab projects are fully static and hosted on GitHub Pages:

- Seed data lives in `seed_data.py` per project
- `export_json.py` regenerates the static JSON from seed data
- The frontend fetches from `data/*.json` at load time
- Client-side state (favorites, completions) uses `localStorage`

---

## Stack

| Layer | Tools |
|---|---|
| Frontend | Vanilla HTML, CSS, JavaScript |
| Data | Python, JSON |
| Maps | Leaflet.js |
| Hosting | GitHub Pages |
