# Real Estate Intelligence Platform (MERN)

A full-stack starter project with a React dashboard, Express REST API, MongoDB persistence, JWT authentication, property listings, search/filtering, saved properties, and market-statistics endpoints.

## Stack
- Frontend: React + Vite, React Router, plain CSS
- Backend: Node.js, Express, Mongoose, JWT, bcryptjs
- Database: MongoDB (local or Atlas)

## Requirements
- Node.js 18+
- MongoDB running locally or a MongoDB Atlas connection string

## Run it

### 1. Backend
```bash
cd backend
cp .env.example .env
# Edit MONGO_URI and JWT_SECRET in .env
npm install
npm run dev
```
Backend runs at `http://localhost:5000`.

### 2. Frontend
Open a second terminal:
```bash
cd frontend
npm install
npm run dev
```
Open the Vite URL shown (usually `http://localhost:5173`).

## Demo mode / data
The frontend calls the API. Seed sample properties:
```bash
cd backend
npm run seed
```
Register a user from the UI, then sign in. The seed script inserts example listings into MongoDB.

## Main API
- `GET /api/health`
- `POST /api/auth/register`
- `POST /api/auth/login`
- `GET /api/auth/me` (JWT)
- `GET /api/properties` (search/filter/sort)
- `GET /api/properties/:id`
- `POST /api/properties` (JWT)
- `PUT /api/properties/:id` (JWT; owner/admin)
- `DELETE /api/properties/:id` (JWT; owner/admin)
- `GET /api/analytics/overview`
- `GET /api/analytics/market?city=...`
- `GET /api/users/saved` (JWT)
- `POST /api/users/saved/:propertyId` (JWT; toggle save)


