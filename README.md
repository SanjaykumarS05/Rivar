# Rivar CRM

React + Laravel API + PostgreSQL CRM rebuilt from the Salez-Robot-Main domain model.

## Stack

- Backend: Laravel 12 API, Sanctum tokens, PostgreSQL control DB and CRM DB
- Frontend: React, TypeScript, Vite, TanStack Query
- Tenant model: shared PostgreSQL tables with `tenant_id`, tenant middleware, and PostgreSQL RLS policies on CRM tables

## Local URLs

- API: `http://127.0.0.1:8000/api`
- React app: `http://localhost:5173`

## Setup

Create two PostgreSQL databases:

```bash
rivar_control
rivar_crm
```

Configure `backend/.env` from `backend/.env.example`, then run:

```bash
cd backend
composer install
php artisan migrate --force
php artisan db:seed --force
php artisan serve
```

In another terminal:

```bash
cd frontend
npm install
npm run dev
```

## Demo Login

- Company: `Demo Realty`
- Email: `demo@rivar.test`
- Password: `password`

## Verification

```bash
cd backend
php artisan test

cd ../frontend
npm run build
```
