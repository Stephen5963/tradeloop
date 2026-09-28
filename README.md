# TradeLoop — Premium Full-Stack Build

This folder contains the upgraded TradeLoop website, app and a working local backend/database.

## Run it

Requires **Node.js 22.5+**.

```bash
cd tradeloop_work
npm start
```

Optional demo seed:

```bash
npm run seed
```

Open:
- Website: http://localhost:4173/
- App: http://localhost:4173/app
- API health: http://localhost:4173/api/health

The backend uses a real SQLite database at `tradeloop.sqlite` and stores users, sessions, jobs and messages. Passwords are hashed with Node's `scrypt` and sessions use random bearer tokens.

## Included API

- `POST /api/auth/signup`
- `POST /api/auth/login`
- `GET /api/auth/me`
- `POST /api/auth/logout`
- `GET /api/workers`
- `PUT /api/profile`
- `GET /api/jobs`
- `POST /api/jobs`
- `POST /api/jobs/:id/claim`
- `PUT /api/jobs/:id/status`
- `GET /api/messages?peer=<userId>`
- `POST /api/messages`
- `GET /api/stats`

The HTML files still work as standalone demos if opened directly, but when served through the included server they use the live API automatically for authentication and marketplace data.
