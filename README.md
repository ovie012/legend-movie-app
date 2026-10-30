# Legend Movie App 🎬

A cross-platform (iOS & Android) movie discovery app built with **React Native** and **Expo**.

Browse the latest movies, search the TMDB catalogue, open detailed movie pages, and see what's **trending**. Trending is calculated from real user searches, which are stored in Appwrite.

## Features

- **Latest movies** feed from the TMDB API
- **Search** with live results
- **Trending movies** ranked by how often users search for them (Appwrite database)
- **Movie details** page using dynamic routes (`/movies/[id]`)
- **Tab navigation**: Home, Search, Saved, Profile
- Custom reusable components: `MovieCard`, `TrendingCard`, `SearchBar`
- A reusable `useFetch` hook for loading, error and refetch states

## Tech stack

| Area | Tools |
|---|---|
| Framework | React Native 0.81, Expo SDK 54 |
| Routing | Expo Router (file-based), React Navigation bottom tabs |
| Language | TypeScript |
| Styling | NativeWind (Tailwind CSS for React Native) |
| Backend | Appwrite (search analytics / trending) |
| Data | TMDB REST API |

## Project structure

```
app/
  (tabs)/        # Home, Search, Saved, Profile tabs
  movies/[id].tsx  # Movie details (dynamic route)
components/      # MovieCard, TrendingCard, SearchBar
services/        # TMDB API, Appwrite client, useFetch hook
constants/ interfaces/ types/
```

## Run locally

1. Install dependencies:
   ```bash
   npm install
   ```
2. Create a `.env` file in the project root:
   ```
   EXPO_PUBLIC_MOVIE_API_KEY=your_tmdb_read_access_token
   EXPO_PUBLIC_APPWRITE_PROJECT_ID=your_project_id
   EXPO_PUBLIC_APPWRITE_DATABASE_ID=your_database_id
   EXPO_PUBLIC_APPWRITE_COLLECTION_ID=your_collection_id
   ```
3. Start the app:
   ```bash
   npx expo start
   ```
   Then open it in **Expo Go** on your phone, or in an Android emulator or iOS simulator.

## Author

**Emonefe Ovie Ezekiel** · [Portfolio](https://legenddev-phi.vercel.app) · [GitHub](https://github.com/ovie012) · [LinkedIn](https://www.linkedin.com/in/ovieemonefe/)
