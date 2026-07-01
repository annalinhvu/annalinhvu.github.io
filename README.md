# annalinhvu.github.io

**[annalinhvu.github.io](https://annalinhvu.github.io)**

Hi, I'm Anna (Linh) — a Data Engineer and BI Engineer based in New York City, originally from Hanoi. By day I build data infrastructure for enterprise marketing clients. By night I make small databases about things I care about: film festivals, analog cameras, Vietnamese food, NYC, and places I want to go.

This whole site is one HTML file. No frameworks, no build step, no `npm install`.

---

## What's inside

The portfolio has three tabs:

- **built** — professional data work (ETL pipelines, Snowflake warehouses, BI dashboards, API connectors) and academic projects from Penn Engineering. Every card has a clickable prototype.
- **studio** — personal projects. Each one started because I wanted something that didn't exist yet.
- **career** — work history.

---

## Personal Projects

### Film Festival Tracker
I submit short films and wanted one place to track deadlines, fees, and what kinds of work gets accepted. Ended up building a full directory of documentary and experimental festivals worldwide — filterable by type, region, tier, and premiere status.

**Stack:** HTML · JSON · Vanilla JS

---

### Analog Film Stock Database
Shooting on film means constantly comparing stocks across vendors for price and availability. Built a searchable database of stocks paired with a lab directory filterable by process (C-41, E-6, B&W, ECN-2) and format.

**Stack:** HTML · JSON · Vanilla JS

---

### NYC Film Scene Map
An interactive map of every place in NYC where you can actually engage with film — screening spaces, workshops, darkrooms, labs, galleries, community spots. Filterable by category and borough.

**Stack:** HTML · JSON · Leaflet.js

---

### Auteurs
A personal filmography index. Directors and performers I keep returning to — biographies, curated film lists with synopses, portrait photography. Searchable by era, nationality, and style.

**Stack:** HTML · JSON · Vanilla JS

---

### NYC Food Help Map
A public-service directory of free food assistance across the five boroughs — food pantries, soup kitchens, community meals, mobile programs, and home delivery. Built because these resources exist and not enough people know about them.

**Live:** https://annalinhvu.github.io/projects/nyc-food-help/  
**Stack:** HTML · JSON · Leaflet.js

---

### NYC Adventure Log
A running list of things to do in New York, organized by category and season — Cinema, Food, Arts, Day Trips, Free, Classes, and more. Includes a surprise picker for when you just can't decide.

**Live:** https://annalinhvu.github.io/nyc-adventure/  
**Stack:** HTML · Vanilla JS

---

### Only Good Things
Named after the wall calendar. A catalog of self-care activities filterable by season, duration, mood, and setting. Track completions locally in your browser, no account needed.

**Stack:** HTML · JSON · Vanilla JS

---

### Cơm Nhà
Vietnamese recipes organized by region — Miền Bắc, Miền Trung, Miền Nam. Browse by category, search by ingredient, save favorites. Each region has its own color identity. Built mostly so I'd stop losing recipes in my notes app.

**Stack:** HTML · JSON · Vanilla JS

---

### Departure Lounge
A bucket list formatted as boarding passes. Countries with cities to visit, food to eat, and actual reasons to go — not the usual tourist checklist. Dark, editorial feel.

**Stack:** HTML · JSON · Vanilla JS

---

## Running locally

```bash
git clone https://github.com/annalinhvu/annalinhvu.github.io.git
cd annalinhvu.github.io
python3 -m http.server 8080
```

Open [http://localhost:8080](http://localhost:8080).

---

## Tech

Everything here is vanilla HTML, CSS, and JavaScript. Data lives in JSON files. Maps use Leaflet. Hosted on GitHub Pages.

For the professional side: Snowflake · Matillion · Python · Looker · Tableau · REST APIs · AWS.
