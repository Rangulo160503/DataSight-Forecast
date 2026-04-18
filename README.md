# DataSight Forecast

Data analysis and forecasting system built with a modern, decoupled architecture.

* Backend API in Python (Flask)
* Frontend in React + TypeScript
* Integrated Machine Learning pipeline

---

## Architecture

```text
backend/    → REST API + business logic + ML pipeline  
frontend/   → user interface (React)  
tests/      → automated tests  
```

The system follows an API-first architecture, where the frontend consumes REST endpoints (`/api/v1/...`).

---

## Features

* Execute Machine Learning pipeline on datasets
* Manage runs:

  * Create
  * List
  * Rename
  * Delete
* Persistent storage using SQLite
* Input validation and duplicate control
* Versioned REST API (`/api/v1`)

---

## API

### Runs

```text
GET    /api/v1/runs  
POST   /api/v1/runs  
POST   /api/v1/runs/register  
PATCH  /api/v1/runs/{run_id}  
DELETE /api/v1/runs/{run_id}  
DELETE /api/v1/runs  
```

---

## Tech Stack

### Backend

* Python
* Flask
* SQLite
* Pandas
* NumPy
* Scikit-learn

### Frontend

* React
* TypeScript
* Vite

### DevOps

* Docker
* GitHub Actions (CI)

---

## Getting Started

### Backend

```bash
pip install -r requirements.txt
flask --app backend.main run
```

---

### Frontend

```bash
cd frontend
npm install
npm run dev
```

---

### Tests

```bash
pytest -q
```

---

### Docker (optional)

```bash
docker compose up --build
```

---

## Testing

The project includes tests focused on:

* API endpoints (`/api/v1`)
* Persistence layer (`run_history`)
* HTTP validation and error handling

---

## Design Decisions

* Removed all server-side UI (Jinja templates)
* Strict separation between backend and frontend
* Business logic encapsulated in `services/`
* ML pipeline decoupled from Flask
* API as the main contract of the system

---

## Project Status

Ready for technical demonstrations, interviews, and further production evolution.

---

## Author

Ronald Angulo
