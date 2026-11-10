# FitConnect — Backend API

REST API for **FitConnect**, a fitness coaching platform that connects clients with coaches and nutritionists. Built by a five-person team for NJIT CS 490 (Spring 2026).

**My role:** top backend contributor (51 commits). I built coach–client hiring, session booking, subscriptions, payments, notifications, Google OAuth/JWT authentication with role-based access, and set up CI.

---

## Features

- **Auth and roles:** email/password and Google OAuth sign-in, JWT sessions, role-based middleware (client, coach, nutritionist, admin).
- **Coaching workflow:** coach discovery, hiring requests, availability, session booking with double-booking protection (409 conflicts).
- **Payments and subscriptions:** purchases, subscription changes, and coach earnings, with multi-table writes wrapped in database transactions.
- **Training data:** workout and meal logs, coach plans, progress photos (file uploads), surveys.
- **Real-time messaging and notifications** with Socket.IO.
- **API documentation** with Swagger/OpenAPI.

## By the numbers

- 158 REST endpoints across 24 route modules
- 39 Sequelize models with versioned migrations
- Jest + Supertest API tests, run in GitHub Actions CI

## Tech stack

| Layer | Technology |
|---|---|
| Runtime | Node.js, Express 5 |
| Database | MySQL, Sequelize ORM and migrations |
| Auth | JWT, Google OAuth, bcrypt |
| Real-time | Socket.IO |
| Testing and CI | Jest, Supertest, GitHub Actions |
| Docs | Swagger UI |

## Getting started

```bash
git clone https://github.com/melihbed/cs490-groupProject-backend.git
cd cs490-groupProject-backend
npm install
cp .env.example .env          # fill in MySQL credentials, JWT_SECRET, Google OAuth keys
npx sequelize-cli db:migrate
npm run dev                    # API docs at http://localhost:3000/api-docs
```

### Tests

```bash
npm test
```

## Team

Built with four teammates as the CS 490 group project. This repository is my fork of the team backend.
