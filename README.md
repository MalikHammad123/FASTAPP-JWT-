# FastAPI JWT Authentication

Simple FastAPI app with JWT login and user registration.

## What it does
- Register new users
- Login with username/password
- Get JWT token for authentication
- Access protected routes with token

## Setup

1. **Install Python packages:**
```bash
pip install fastapi uvicorn python-jose passlib bcrypt python-dotenv
```

2. **Create .env file:**
```
SECRET_KEY=my-secret-key
```

3. **Run the app:**
```bash
uvicorn simple_app:app --reload
```

4. **Open in browser:**
- App: http://localhost:8000
- Docs: http://localhost:8000/docs

## How to use

### Test user (already exists):
- Username: `admin`
- Password: `secret`

### API endpoints:
- `POST /register` - Create new user
- `POST /login` - Get JWT token
- `GET /me` - Get user info (needs token)
- `GET /protected` - Protected route (needs token)

## Quick test:

1. Go to http://localhost:8000/docs
2. Try `/login` with admin/secret
3. Copy the token
4. Click "Authorize" button and paste token
5. Try `/protected` endpoint

## Files:
- `simple_app.py` - Main app
- `.env` - Secret key
- `requirements.txt` - Dependencies

That's it! 🚀
