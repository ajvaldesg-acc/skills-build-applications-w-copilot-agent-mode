# OctoFit Tracker - Modern Multi-Tier Application

This is a modern full-stack application for fitness tracking with a React 19 frontend and Express.js + MongoDB backend.

## Project Structure

```
octofit-tracker/
├── frontend/          # React 19 + Vite application
│   ├── src/          # React components and app logic
│   ├── public/       # Static assets
│   └── index.html    # HTML entry point
└── backend/          # Express.js + TypeScript + MongoDB API
    ├── src/          # TypeScript source code
    └── dist/         # Compiled JavaScript (after build)
```

## Technology Stack

### Frontend
- **React 19** - Latest React library
- **Vite 8** - Fast build tool and dev server
- **ESLint** - Code linting
- **Port**: 5173

### Backend
- **Node.js + Express 5** - Web framework
- **TypeScript** - Type-safe JavaScript
- **Mongoose** - MongoDB ODM
- **Port**: 8000

### Database
- **MongoDB** - NoSQL database
- **Port**: 27017

## Prerequisites

- Node.js (v18 or higher)
- npm or yarn
- MongoDB (local or remote instance)

## Installation

### Frontend Setup

```bash
cd octofit-tracker/frontend
npm install
cp .env.example .env.local
```

### Backend Setup

```bash
cd octofit-tracker/backend
npm install
cp .env.example .env
```

## Running the Application

### Start MongoDB (if running locally)

```bash
# Make sure MongoDB is running on localhost:27017
mongod
```

### Start Backend

```bash
cd octofit-tracker/backend

# Development mode (with hot reload)
npm run dev

# Build for production
npm run build

# Run production build
npm start
```

Backend will be available at `http://localhost:8000`

### Start Frontend

In a new terminal:

```bash
cd octofit-tracker/frontend

# Development mode
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview
```

Frontend will be available at `http://localhost:5173`

## Environment Variables

### Backend (.env)
```
PORT=8000
MONGODB_URI=mongodb://localhost:27017/octofit-tracker
NODE_ENV=development
```

### Frontend (.env.local)
```
VITE_API_URL=http://localhost:8000
```

## API Endpoints

- `GET /` - API information
- `GET /health` - Health check endpoint

## Development Workflow

1. Terminal 1: Start MongoDB
2. Terminal 2: Start backend (`npm run dev`)
3. Terminal 3: Start frontend (`npm run dev`)
4. Open browser to `http://localhost:5173`

## Building for Production

### Backend
```bash
cd octofit-tracker/backend
npm run build
npm start
```

### Frontend
```bash
cd octofit-tracker/frontend
npm run build
# Static files will be in dist/
```

## Next Steps

- Add authentication (JWT, OAuth)
- Create API routes for fitness tracking
- Implement MongoDB schemas and models
- Add React components and pages
- Set up CI/CD pipeline
