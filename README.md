# Anna (Linh) Vu — Portfolio

**[annalinhvu.github.io/portfolio](https://annalinhvu.github.io/portfolio)**

Personal portfolio and a collection of lab projects built out of curiosity and care. No frameworks, no build step, fully static.

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
