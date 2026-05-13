# Gameid

A responsive game discovery web app powered by the [RAWG Video Games Database API](https://rawg.io/apidocs). Browse thousands of games, filter by genre and platform, sort by various criteria, and explore detail pages with trailers, screenshots, and descriptions.

## Features

- Browse games with infinite scrolling
- Filter by genre (sidebar) and platform (dropdown)
- Sort by relevance, date added, name, release date, or Metacritic score
- Search games by name
- Game detail page with trailer, screenshots, description, and attributes
- Metacritic score badges and rating emojis on each card
- Dark mode by default with a light mode toggle
- Fully responsive layout (mobile-first)

## Tech Stack

| Layer | Library |
|---|---|
| UI Framework | React 18 + TypeScript |
| Build Tool | Vite |
| Component Library | Chakra UI v2 |
| Data Fetching & Caching | TanStack React Query v4 |
| Global State | Zustand |
| Routing | React Router v6 |
| HTTP Client | Axios |
| Animation | Framer Motion |
| Icons | React Icons |
| Infinite Scroll | react-infinite-scroll-component |

## Getting Started

### Prerequisites

- Node.js 16+
- A free RAWG API key from [rawg.io/apidocs](https://rawg.io/apidocs)

### Installation

```bash
git clone https://github.com/warsana/gameid.git
cd gameid
npm install
```

### Configuration

Open `src/services/api-client.ts` and replace the API key with your own:

```ts
const axiosInstance = axios.create({
  baseURL: "https://api.rawg.io/api",
  params: {
    key: "YOUR_RAWG_API_KEY",
  },
});
```

### Running Locally

```bash
npm run dev
```

Open [http://localhost:5173](http://localhost:5173) in your browser.

### Building for Production

```bash
npm run build
npm run preview
```

## Project Structure

```
src/
├── components/     # Reusable UI components
├── entities/       # TypeScript interfaces (Game, Genre, Platform, etc.)
├── hooks/          # Custom React Query hooks
├── pages/          # Route-level page components
├── services/       # Axios API client and image URL helper
├── store.ts        # Zustand global game query store
├── theme.ts        # Chakra UI theme (dark mode default)
└── routes.tsx      # React Router configuration
```

## API

This project uses the [RAWG API](https://rawg.io/apidocs) — one of the largest video game databases with data on 500,000+ games.
