# GymForge Tracker

GymForge Tracker is a redesigned full-stack gym tracking app built with React, Vite, Express, and PostgreSQL on Neon.

## Stack
- React + Vite frontend
- Express API backend
- PostgreSQL database (Neon-ready)
- Chart.js progress visualization

## Local setup
1. Copy `server/.env.example` to `server/.env`
2. Add your Neon `DATABASE_URL`
3. Install dependencies:
   ```bash
   npm install
   ```
4. Run SQL schema:
   ```bash
   psql "$DATABASE_URL" -f server/sql/schema.sql
   ```
5. Start both apps:
   ```bash
   npm run dev
   ```

## GitHub deployment
### Frontend on Vercel / Netlify
- Set frontend build root to `client`
- Build command: `npm run build`
- Output directory: `dist`
- Set `VITE_API_URL` to your deployed backend URL

### Backend on Render / Railway
- Root directory: `server`
- Build command: `npm install`
- Start command: `npm start`
- Add environment variables:
  - `DATABASE_URL`
  - `CLIENT_URL`
  - `PORT`

## GitHub upload
1. Create a new repository.
2. Upload this project.
3. Never commit `.env` or raw database credentials.
