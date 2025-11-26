# TripX - AI-Powered Travel Platform with Web3 Integration

A modern travel planning application with AI trip generation, quest system, and NFT rewards.

## Quick Start

1. Install dependencies:
```bash
npm install
```

2. Copy `.env.example` to `.env` and fill in your API keys (or use the provided `.env`)

3. Start development server:
```bash
npm run dev
```

## Features

- 🗺️ **AI Trip Generation** - Gemini AI creates personalized travel itineraries
- 🎯 **Quest System** - Complete quests at destinations to earn rewards
- 🏆 **NFT Passport** - Mint your travel passport as an NFT
- 💰 **TPX Tokens** - Earn tokens for completed quests
- 📊 **Leaderboard** - Compete with other travelers
- 🚌 **Transit Planner** - Find public transport connections

## Tech Stack

- React 18 + TypeScript
- Vite
- Tailwind CSS
- Framer Motion
- Supabase (Database + Edge Functions)
- wagmi + viem (Web3)
- RainbowKit (Wallet Connection)
- Mapbox GL / Leaflet (Maps)

## Environment Variables

The app requires these environment variables (already set in `.env`):

- `VITE_SUPABASE_URL` - Supabase project URL
- `VITE_SUPABASE_ANON_KEY` - Supabase anonymous key
- `VITE_GOOGLE_MAPS_API_KEY` - Google Maps API key
- `VITE_MAPBOX_TOKEN` - Mapbox access token
- `VITE_TPX_CONTRACT_ADDRESS` - TPX token contract (Sepolia)
- `VITE_NFT_PASSPORT_CONTRACT_ADDRESS` - NFT Passport contract (Sepolia)

## Deployment

Build for production:
```bash
npm run build
```

The `dist` folder can be deployed to any static hosting service.
