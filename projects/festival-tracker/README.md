# Doc & Experimental Film Tracker

A searchable static tracker for documentary and experimental film festivals, filmmaker funds, and artist grants in New York, across the U.S., and internationally. Grants can be filtered by focus, region, stage, and community, including women and gender-expansive artists, Global South filmmakers, Black and Indigenous storytellers, disabled creators, LGBTQ+ filmmakers, Native filmmakers, and other supported groups. The GitHub Pages interface reads curated festival and grant data from JSON; the original SQLite and FastAPI festival data tools remain available for local maintenance.

Grant listings are curated from official funder pages. Each record includes a `last_verified` date, and recurring deadlines carried into a future cycle are visibly labeled as estimates in the interface.

## Setup

```bash
pip install -r requirements.txt
python seed_data.py
```

This creates `festivals.db` with 15 curated experimental film festivals, their submission deadlines, and accepted categories.

## API

Start the server:

```bash
uvicorn api:app --reload
```

Interactive docs available at http://localhost:8000/docs

### Endpoints

**List festivals** (with optional filters):
```bash
curl http://localhost:8000/festivals
curl http://localhost:8000/festivals?tier=major
curl http://localhost:8000/festivals?country=USA
curl http://localhost:8000/festivals?focus=experimental
curl http://localhost:8000/festivals?search=ann
```

**Get a single festival** (with deadlines and categories):
```bash
curl http://localhost:8000/festivals/1
```

**List deadlines**:
```bash
curl http://localhost:8000/deadlines
curl http://localhost:8000/deadlines?year=2025
curl http://localhost:8000/deadlines?upcoming=true
```

**List categories**:
```bash
curl http://localhost:8000/categories
curl http://localhost:8000/categories?festival_id=1
```

## Python Usage

```python
import db

conn = db.get_db()

# List all festivals
rows = db.query(conn, "SELECT name, city, country FROM festivals ORDER BY name")
for r in rows:
    print(f"{r['name']} — {r['city']}, {r['country']}")

# Find festivals by tier
majors = db.query(conn, "SELECT name FROM festivals WHERE tier = ?", ("major",))

# Upcoming deadlines
upcoming = db.query(conn, """
    SELECT f.name, d.tier, d.deadline, d.fee_usd
    FROM deadlines d
    JOIN festivals f ON f.id = d.festival_id
    WHERE d.deadline >= date('now')
    ORDER BY d.deadline
""")
```

## Schema

- **festivals** — core info (name, city, country, tier, focus, premiere requirements)
- **deadlines** — submission deadlines per festival per year (with fees)
- **categories** — accepted submission categories (with runtime limits)
