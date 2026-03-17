# Spa Booking

Spa Booking is a full-stack booking system project with a React frontend and an Express/MongoDB backend. The current repository snapshot includes Redux store setup, protected-route UI helpers, and backend authentication route wiring.

## Tech Stack

- Frontend: React, Redux Toolkit, React Router, Tailwind CSS
- Backend: Node.js, Express, MongoDB, Mongoose, JWT, bcryptjs

## Current Repository Structure

```text
spa-booking/
├── backend/
│   ├── package.json
│   └── routes/
│       └── authRoutes.js
├── frontend/
│   ├── postcss.config.js
│   ├── public/
│   └── src/
│       ├── app/store.js
│       ├── components/PrivateRoute.jsx
│       ├── components/Spinner.jsx
│       └── index.js
└── README.md
```

## Features In This Snapshot

- Redux store configured for `auth`, `services`, and `bookings`
- Protected frontend routes with redirect-to-login behavior
- Reusable loading spinner component
- Backend auth route definitions for register, login, profile, and current-user access

## API Routes

The backend currently exposes these auth endpoints through `backend/routes/authRoutes.js`:

- `POST /register`
- `POST /login`
- `GET /me`
- `PUT /profile`

Protected routes depend on authentication middleware and controller files that are referenced by the route module.

## Environment Variables

The backend expects these environment variables:

```env
NODE_ENV=
PORT=
MONGO_URI=
JWT_SECRET=
```

## Local Setup

### Backend

```bash
cd backend
npm install
npm run dev
```

### Frontend

This repository currently contains frontend source files, but the committed snapshot does not include `frontend/package.json`, `src/App.js`, `src/index.css`, or the feature slices referenced by the store. Add those files before starting the frontend locally.

Typical frontend start command once the missing files are restored:

```bash
cd frontend
npm install
npm start
```

## Important Notes

- `backend/package.json` points to `server.js`, but that file is not included in the current commit.
- `backend/routes/authRoutes.js` references controller and middleware modules that are not included in the current commit.
- `frontend/src/index.js` references `App` and `index.css`, and the Redux store references feature slices that are not included in the current commit.
- `backend/.env` is currently tracked in Git. It is safer to replace it with a `.env.example` file and keep real secrets out of version control.

## Next Steps

- Restore or add the missing backend entry files and middleware/controllers
- Restore the missing frontend app shell and Redux feature slices
- Add a root script or workspace setup for running frontend and backend together
- Replace committed secrets with environment examples

## Author

GitHub: [Ireshrangana](https://github.com/Ireshrangana)
