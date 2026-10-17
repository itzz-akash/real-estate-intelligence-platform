# AI-Powered Real Estate Intelligence (MERN)

A starter full-stack app for listing/searching properties and generating AI-assisted property insights.

## Features
- React + Vite dashboard with search, city/type filters, property cards, and market summary
- Express REST API with MongoDB/Mongoose
- Seed demo properties automatically when MongoDB is connected and the collection is empty
- AI property analysis endpoint (Google Gemini API optional); falls back to a local rule-based analysis when no API key is set
- Demo data mode: frontend/API still work without MongoDB using sample listings

## Requirements
- Node.js 18+
- MongoDB local or Atlas (optional for demo mode)

## Run locally
### 1. Server
```bash
cd server
cp .env.example .env
npm install
npm run dev
```
Server runs at http://localhost:5000

### 2. Client (new terminal)
```bash
cd client
npm install
npm run dev
```
Open the URL printed by Vite (usually http://localhost:5173).

## Environment
`server/.env`:
- `PORT=5000`
- `MONGODB_URI=mongodb://127.0.0.1:27017/real_estate_intelligence`
- `GEMINI_API_KEY=` (optional; set a Google Gemini API key to enable generated AI analysis)

## API
- `GET /api/health`
- `GET /api/properties?search=&city=&type=&minPrice=&maxPrice=`
- `GET /api/properties/:id`
- `POST /api/ai/analyze` body: `{ "property": { ...propertyFields } }`

This is an educational starter, not a professional valuation tool. AI insights are estimates and should not replace local market research or professional advice.
