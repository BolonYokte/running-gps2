# RunCycle GPS

GPS tracking and racing platform specifically designed for **Running** and **Cycling** activities.

## Features

### 🏃‍♂️ Running Mode
- High-precision GPS tracking
- Waypoints every 100m for detailed splits
- Real-time pace and distance monitoring
- Auto-start/finish detection
- Live leaderboards

### 🚴‍♂️ Cycling Mode  
- GPS tracking optimized for cycling speeds
- Waypoints every 1000m for segment timing
- Speed and distance metrics
- Route creation and navigation
- Performance analytics

### 🗺️ Core Features
- Interactive Leaflet maps with satellite view
- GPX/GeoJSON track upload and management
- Real-time GPS with advanced filtering
- Rally-style timing and scoring system
- Nearby tracks discovery (100km radius)
- Professional UI with gradient buttons and animations

## Tech Stack

- **Frontend**: React 18 + TypeScript + Vite
- **UI**: Tailwind CSS + shadcn/ui components
- **Maps**: Leaflet with custom controls
- **Backend**: Node.js + Express + TypeScript
- **Database**: PostgreSQL with Drizzle ORM
- **Real-time**: WebSockets for live updates
- **GPS**: Advanced filtering and smoothing algorithms

## Getting Started

1. Install dependencies:
```bash
npm install
```

2. Set up environment variables:
```bash
cp .env.example .env
# Add your DATABASE_URL and ORS_API_KEY
```

3. Initialize database:
```bash
npm run db:push
```

4. Start development server:
```bash
npm run dev
```

The app will be available at `http://localhost:5000`

## Environment Variables

- `DATABASE_URL` - PostgreSQL connection string
- `ORS_API_KEY` - OpenRouteService API key for route generation
- `SESSION_SECRET` - Session encryption key

## Deployment

Build for production:
```bash
npm run build
npm start
```

## Project Structure

```
├── client/          # React frontend
│   ├── src/
│   │   ├── components/  # UI components
│   │   ├── hooks/       # Custom React hooks
│   │   ├── lib/         # Utilities and stores
│   │   └── pages/       # Route components
├── server/          # Express backend
│   ├── routes.ts    # API routes
│   └── index.ts     # Server entry point
├── shared/          # Shared types and schemas
└── public/          # Static assets
```

## Features in Detail

### GPS Tracking Engine
- High-accuracy positioning with error filtering
- Anti-drift and anti-jump protection
- Warm-up period for GPS stabilization
- Adaptive smoothing based on signal quality

### Rally System
- Auto-detection of start/finish based on proximity
- Perpendicular gate crossing validation
- Real-time HUD with metrics
- Percentile-based scoring system

### Route Creation
- Point-and-click route building
- Integration with OpenRouteService
- Surface type analysis (on-road vs off-road)
- Automatic waypoint generation

## License

MIT License - see LICENSE file for details