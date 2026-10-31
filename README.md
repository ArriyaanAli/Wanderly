# Wanderly 🌍

Wanderly is a full-stack project combining a modern React frontend, a FastAPI backend, and AI services to provide travel/experience features.

## 🛠️ Tech Stack

- **Frontend**: React (Vite), Tailwind CSS, Axios, React Router
- **Backend**: FastAPI, SQLAlchemy, Pydantic, Uvicorn
- **Auth & Security**: python-jose (JWT), Passlib (bcrypt)
- **Database**: PostgreSQL (local for dev, Render for production)
- **AI Integration**: Hugging Face Inference API, open-source LLMs (Mistral/Gemma), prompt engineering
- **Image Storage**: Cloudinary
- **Deployment**: Backend on Render, Frontend on Vercel

---

## 📁 Project Structure

```
wanderly/
├── frontend/                 # React + Vite application
├── backend/                  # FastAPI backend (Python)
│   ├── main.py
│   ├── database.py
│   ├── models.py
│   ├── schemas.py
│   ├── crud.py
│   └── auth.py
├── ai_service/               # AI helper services or experiments
└── README.md
```

---

## 🚀 Getting Started (Local)

### Prerequisites

- **React.js**
- **Python** (v3.9+)
- **PostgreSQL** (local dev instance; you've indicated it's installed)
- **Git**

### Setup Frontend

```bash
cd frontend
npm install
npm run dev
```

### Setup Backend (FastAPI)

1. Create a virtual environment and install deps:

```bash
cd backend
python -m venv .venv
# Windows
.venv\\Scripts\\activate
pip install -r requirements.txt
```

2. Create `.env` from `.env.example` and update `DATABASE_URL` to point to your local Postgres.

3. Run the backend:

```bash
uvicorn backend.main:app --reload --port 8000
```

API docs will be available at `http://localhost:8000/docs`.

---

## ▶️ Running Services

- Frontend: `npm run dev` (default Vite port `5173`)
- Backend: `uvicorn backend.main:app --reload --port 8000`

---

## 📦 Environment Variables

Copy and update environment examples in each service (e.g., `backend/.env.example`).

---

If you need help connecting your local Postgres or adjusting the `DATABASE_URL`, open an issue or ask here.
**Happy Coding! 🚀**
