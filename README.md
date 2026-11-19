# BankEase – NextGen Net Banking Application (P18)

BankEase is an enterprise-grade net banking application developed for MCA academic submission. It features role-based access control (Customer and Bank Officer), a double-entry ledger financial transaction engine, complete loan management with EMI repayment, utility bill payments, investment tracking, and customer support.

## Architecture & Technology Stack

- **Backend**: Python 3.12, Django 6.1.3, Django REST Framework 3.18.3, SimpleJWT, Gunicorn, WhiteNoise
- **Database**: PostgreSQL (hosted on Supabase) with SSL mode required
- **Frontend**: Responsive Single-Page Application (HTML5, CSS3, ES6+ Vanilla JavaScript)
- **Deployment**:
  - Frontend: Netlify (Continuous Deployment from `Bankease-Frontend` repo)
  - Backend: Render Web Service (Continuous Deployment from `Bankease-Backend` repo)
  - Deployment Repo: `Bankease-Deployment` (Blueprints, Docker Compose, CI/CD, Documentation)

---

## 3 Independent Repositories

1. **Frontend**: https://github.com/Sadique-Saifi/Bankease-Frontend
2. **Backend**: https://github.com/Sadique-Saifi/Bankease-Backend
3. **Deployment**: https://github.com/Sadique-Saifi/Bankease-Deployment

---

## Local Development Setup

### Backend Setup:
```bash
cd backend
# Activate virtual environment
..\BankEase\Scripts\activate
# Install requirements
pip install -r requirements.txt
# Run migrations (already applied to Supabase)
python manage.py migrate
# Seed demo data
python manage.py seed_data
# Start dev server
python manage.py runserver
```

### Frontend Setup:
Open `frontend/index.html` via Live Server or any static HTTP server on port 5500:
```bash
cd frontend
python -m http.server 5500
```
Then navigate to `http://127.0.0.1:5500`.

---

## Demo Credentials
- **Bank Officer**: `officer1` / `Admin@1234`
- **Customer**: `customer1` / `Customer@1234`
