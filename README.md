DEMO BETA VER. SEPOLIA TESTNET.

<div align="center">

# 🌍 TripX

### **AI-Powered Travel Planning with Web3 Rewards**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![React](https://img.shields.io/badge/React-18.3-61DAFB?logo=react)](https://reactjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.5-3178C6?logo=typescript)](https://www.typescriptlang.org/)
[![Vite](https://img.shields.io/badge/Vite-6.4-646CFF?logo=vite)](https://vitejs.dev/)
[![Supabase](https://img.shields.io/badge/Supabase-Database-3ECF8E?logo=supabase)](https://supabase.com/)
[![Ethereum](https://img.shields.io/badge/Ethereum-Sepolia-627EEA?logo=ethereum)](https://sepolia.etherscan.io/)

**Transform trip planning from a chore into an adventure**

[Features](#-features) • [Tech Stack](#-tech-stack) • [Getting Started](#-getting-started) • [Architecture](#-architecture)

</div>

---

## 🎯 What is TripX?

**TripX** is an AI-powered travel companion that creates personalized trip itineraries, gamifies exploration through quests, and rewards travelers with blockchain-based tokens and NFTs.

```
📝 Your Input              🤖 AI Magic                    ✨ Your Trip
─────────────              ──────────                     ──────────
• Destination              Gemini 2.5 Pro                 • Day-by-day itinerary
• Duration            ──►  + Google Places           ──►  • Cost estimates
• Budget                   + Real-time data               • Hotel recommendations
• Interests                                               • Quests to complete
```

---

## ✨ Features

### 🗺️ AI Trip Generator
Create personalized travel itineraries in seconds using **Google Gemini 2.5 Pro**.

- **Smart Interest Matching** - Only shows places matching your selected categories (Food, Culture, Nature, Nightlife)
- **Budget-Aware Planning** - Low/Medium/High budget tiers with realistic costs
- **Dynamic Day Planning** - 4-5 activities per day, properly scheduled
- **Hotel Recommendations** - Best accommodations within your budget with pricing
- **Nearby Exploration** - Suggests attractions within 25km when local options are limited

### 🎮 Quest System
Complete challenges at destinations to earn rewards.

- **Location-based Quests** - Visit specific places, take photos
- **XP & Leveling** - Progress through traveler ranks
- **Daily Challenges** - Fresh quests every day
- **Photo Verification** - AI verifies quest completion

### 🏆 Web3 Rewards

| Token | Type | Purpose |
|-------|------|---------|
| 🪙 **TPX** | ERC-20 | Utility token earned for completing trips and quests |
| 🎫 **NFT Passport** | ERC-721 | Your unique travel identity on the blockchain |
| 🏅 **Achievement NFTs** | ERC-721 | Collectible badges for milestones |

**Smart Contracts (Ethereum Sepolia):**
```
TPX Token:        0x6A19B0E01cB227B9fcc7eD95b8f13D2894d63Ffd
NFT Passport:     0xFc22556bb4ae5740610bE43457d46AdA5200b994  
Achievement NFT:  0x110D62545d416d3DFEfA12D0298aBf197CF0e828
```

### 🚌 Real-Time Transit
Live public transportation data for route planning.

- Metro/Subway schedules
- Bus tracking
- Train connections
- Multi-modal journey planning

### 📊 Leaderboard & Achievements
Compete with other travelers worldwide.

- Global rankings by XP
- Achievement badges collection
- Travel statistics

---

## 🛠️ Tech Stack

### Frontend
| Technology | Purpose |
|------------|---------|
| React 18 | UI Framework |
| TypeScript | Type Safety |
| Vite | Build Tool |
| Tailwind CSS | Styling |
| Framer Motion | Animations |
| Lucide Icons | Icon System |

### Backend & Database
| Technology | Purpose |
|------------|---------|
| Supabase | PostgreSQL Database + Auth |
| Edge Functions | Serverless API (Deno) |
| Row Level Security | Data Protection |

### AI & Maps
| Technology | Purpose |
|------------|---------|
| Google Gemini 2.5 Pro | Trip Generation AI |
| Google Places API | Location Data |
| Google Maps | Geocoding & Directions |
| Mapbox GL JS | Interactive Maps |

### Web3
| Technology | Purpose |
|------------|---------|
| wagmi + viem | Ethereum Integration |
| RainbowKit | Wallet Connection |
| Ethereum Sepolia | Testnet Blockchain |

---

## 🚀 Getting Started

### Prerequisites
- Node.js 18+
- npm or yarn

### Installation

```bash
# Install dependencies
npm install

# Start development server
npm run dev
```

### Environment Variables

Create a `.env` file with:

```env
# Supabase (Required)
VITE_SUPABASE_URL=your_supabase_url
VITE_SUPABASE_ANON_KEY=your_supabase_anon_key

# Google APIs (Required)
VITE_GOOGLE_MAPS_API_KEY=your_google_maps_key
VITE_GOOGLE_AI_KEY=your_gemini_api_key
VITE_MAPBOX_TOKEN=your_mapbox_token

# Web3 (Required for blockchain features)
VITE_TPX_CONTRACT_ADDRESS=0x6A19B0E01cB227B9fcc7eD95b8f13D2894d63Ffd
VITE_NFT_PASSPORT_CONTRACT_ADDRESS=0xFc22556bb4ae5740610bE43457d46AdA5200b994
VITE_ACHIEVEMENT_NFT_CONTRACT_ADDRESS=0x110D62545d416d3DFEfA12D0298aBf197CF0e828
VITE_ADMIN_WALLET_PRIVATE_KEY=your_admin_wallet_key
VITE_ETH_SEPOLIA_RPC_URL=https://ethereum-sepolia.publicnode.com
```

### Build for Production

```bash
npm run build
```

---

## 🏗️ Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                    FRONTEND (React + Vite)                   │
├─────────────────────────────────────────────────────────────┤
│  components/     │  services/      │  hooks/                │
│  (45+ UI)        │  (33+ APIs)     │  (Auth, NFT, etc.)    │
└─────────────────────────────┬───────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────┐
│                    SUPABASE                                  │
├─────────────────────────────────────────────────────────────┤
│  PostgreSQL      │  Edge Functions  │  Authentication       │
│  (trips, users,  │  (generate-trip  │  (Magic Link,        │
│   quests, etc.)  │   -ai, etc.)     │   Wallet)            │
└─────────────────────────────┬───────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────┐
│                    EXTERNAL SERVICES                         │
├─────────────────────────────────────────────────────────────┤
│  Google Gemini   │  Google Places  │  Ethereum Sepolia      │
│  (AI)            │  (Locations)    │  (Smart Contracts)     │
└─────────────────────────────────────────────────────────────┘
```

---

## 📁 Project Structure

```
tripx/
├── components/           # React components
│   ├── pages/           # Page components (Dashboard, CreateTrip, etc.)
│   ├── layout/          # Layout components (Header, Sidebar)
│   └── ...              # Shared components
├── services/            # API services
│   ├── aiTripService.ts # AI trip generation
│   ├── web3Service.ts   # Blockchain interactions
│   └── ...              # Other services
├── hooks/               # Custom React hooks
├── lib/                 # Utilities (Supabase client, etc.)
├── styles/              # Global styles
├── types/               # TypeScript types
└── data/                # Static data (operators, etc.)
```

---

## 🔐 Security

- **Authentication**: Supabase Auth with Magic Link & Wallet
- **API Keys**: Environment variables, never exposed to client
- **Database**: Row Level Security (RLS) policies
- **Smart Contracts**: Deployed on testnet, admin-controlled minting

---

## 📄 License

MIT License - see LICENSE file for details.

---

<div align="center">

**Built with ❤️ using React, Supabase & Ethereum**

</div>

