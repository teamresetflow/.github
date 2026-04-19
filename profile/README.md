# DoThisNow

Electron desktop app for habit tracking, health metrics, and productivity with AI-powered insights.

## What is "Do This Now"?

DoThisNow is an intelligent productivity companion that helps you build better habits and maintain your health throughout the day. It combines habit tracking, health monitoring, and AI-powered recommendations to guide you toward your goals.

The app learns from your behavior patterns and suggests the most impactful action you should take right now - whether that's completing a habit, taking a break, drinking water, or working on a goal. It's designed to reduce decision fatigue by telling you exactly what to do next based on your priorities, schedule, and current state.

Key features include:
- Smart habit tracking with streak management and completion analytics
- Health metrics logging (mood, energy, sleep, stress)
- Hydration and break reminders with intelligent timing
- Focus sessions with Pomodoro-style tracking
- Gamification system with XP, levels, and achievements
- AI-powered insights that detect patterns and suggest optimizations
- Multi-profile support for different users or contexts
- Real-time activity feed showing your progress throughout the day

The "Do This Now" feature is the heart of the app - it analyzes your habits, goals, recent activity, and time of day to recommend the single most important thing you should focus on right now.

## Tech Stack

- React 18 + Tailwind CSS + Zustand
- Electron 28
- Express.js + SQLite3

## Quick Start

```bash
# Install
npm install

# Setup environment
cp .env.example .env
# Edit .env and change JWT_SECRET

# Run
npm start
```

Backend: http://localhost:3001  
Frontend: http://localhost:3000

## Requirements

- Node.js v16 or v20 LTS
- Windows: Visual Studio Build Tools

## Project Structure

```
backend/
├── server.js           # Express app + middleware
├── database.js         # SQLite initialization
├── middleware/
│   └── auth.js         # JWT authentication (ready)
└── routes/
    ├── habits.js       # Habit CRUD + completions
    ├── healthLogs.js   # Health metrics tracking
    ├── hydration.js    # Water intake logging
    ├── breaks.js       # Break activity tracking
    ├── goals.js        # Goal management
    ├── gamification.js # XP, levels, achievements
    └── sessions.js     # Focus session tracking

src/
  ├── pages/      # React components
  ├── services/   # API clients
  ├── store/      # Zustand state
  └── utils/      # AI utilities

electron.js       # Electron main process
```

## Commands

```bash
npm start              # Start dev server
npm run electron:dev   # Launch Electron app
npm run verify         # Check installation
npm run build          # Production build
```

## API Endpoints

- `/api/habits` - Habit tracking
- `/api/health-logs` - Health metrics
- `/api/hydration` - Water intake
- `/api/goals` - Goal management
- `/api/gamification` - XP and achievements
- `/api/profile` - User profile

## Troubleshooting

**sqlite3 errors:**
```bash
npm rebuild sqlite3
```

**Port in use:**
Change `PORT` in `.env`

**Complete reset:**
```bash
rm -rf node_modules package-lock.json
npm install
```

## License

MIT
