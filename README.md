# Admin Dashboard System

## Overview

A polished responsive React administration interface for operational metrics, revenue trends, team access, recent activity, reports, and settings.

## Features

Responsive sidebar/mobile navigation, asynchronous mock API, animated metrics, revenue visualization, activity feed, searchable team directory, status indicators, accessible labels, loading states, and route-based pages.

## Technology Stack

React 19, TypeScript 7, Vite 8, React Router 7, Lucide icons, Testing Library, Vitest 5, Nginx, and Docker.

## Requirements / Installation

Install Node.js 24+ and npm 11+, then run `npm install`.

## Environment Variables

`VITE_API_BASE_URL` is documented in `.env.example`. Only public browser configuration may use the `VITE_` prefix; never place secrets there.

## Database Setup

This frontend demonstration uses an isolated asynchronous mock service and has no database. Replace `src/services/mockApi.ts` with calls to a separately secured backend.

## Running the Application

Run `npm run dev`; use `npm run build` for the production bundle.

## Running Tests

Run `npm run check`. Tests cover dashboard loading, navigation, and directory filtering.

## Default Development Accounts

The UI displays a development-only Administrator persona, Maya Chen. Authentication is intentionally delegated to the future backend.

## API Endpoints

Expected backend resources are dashboard summaries, activity, and users under `VITE_API_BASE_URL`; the included mock keeps the portfolio app runnable alone.

## Folder Structure

`components` contains reusable UI, `pages` contains routes, `services` provides the mock API boundary, `types` owns contracts, and `tests` contains interaction tests.

## Security Notes

No secrets or real personal data are stored. Content is rendered through React escaping, and Nginx adds baseline headers. Route visibility in a browser is only a UX control: a real backend must authenticate every request, enforce roles and object permissions, validate inputs, apply rate limits, and return minimized data.

## Known Limitations

Charts use lightweight CSS rather than a charting dependency, and authentication, mutations, exports, and live server data require a backend integration.

## License

MIT
