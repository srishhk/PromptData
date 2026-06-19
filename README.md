# PromptData ✨
> Describe your dataset. Get it instantly.

AI-powered synthetic dataset generator — type a prompt in plain English and download clean data in seconds.

🔗 **Live:** [promptdata.vercel.app](https://promptdata.vercel.app)


## Features
- Natural language prompt → instant dataset
- Quick templates & regional locales (All India, North, South, Maharashtra, Gujarat, East)
- Export as Excel, JSON, CSV, SQL, XML
- Preview with sort, search, stats & history


## Tech Stack
| Layer | Tech |
|-------|------|
| Frontend | Next.js 14, TypeScript, Tailwind CSS |
| Backend | FastAPI (Python) |
| AI | Groq API |
| Data | Pandas, NumPy, Faker |


## Local Setup

```bash
# Clone
git clone https://github.com/srishhk/PromptData.git

# Backend
cd backend
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
# Add GROQ_API_KEY to .env
uvicorn main:app --reload        # local only
# On Render, start command is: uvicorn main:app --host 0.0.0.0 --port $PORT

# Frontend
cd frontend
npm install
# Add NEXT_PUBLIC_API_URL=http://localhost:8000 to .env.local
npm run dev
```


## API
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/` | Health check |
| POST | `/api/generate` | Generate dataset |
| POST | `/api/export` | Export dataset |
| GET | `/api/library` | Saved datasets |


## Deployment
- **Backend** → [Render](https://render.com) (Root: `backend/`)
- **Frontend** → [Vercel](https://vercel.com) (Root: `frontend/`)


MIT License
