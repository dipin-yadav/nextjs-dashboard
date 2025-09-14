# Copilot Instructions for AI Agents

## Project Overview
- This is a Next.js 13+ dashboard app using the App Router, TypeScript, and Tailwind CSS.
- The main UI and logic are under `app/`, with subfolders for routes and features (e.g., `dashboard/`, `invoices/`, `customers/`).
- Shared UI components are in `app/ui/`, organized by feature.
- Data and business logic live in `app/lib/` (e.g., `actions.ts`, `data.ts`).

## Key Patterns & Conventions
- **Server Actions**: Use `useActionState` and server functions from `app/lib/actions.ts` for form handling and mutations.
- **Client Components**: Mark with `'use client'` at the top. Most UI in `app/ui/` is client-side.
- **Routing**: Follows Next.js App Router conventions. Route segments are folders with `page.tsx`, `layout.tsx`, and optional subfolders.
- **Error Handling**: Use `error.tsx` and `not-found.tsx` in route folders for error boundaries and 404s.
- **Styling**: Tailwind CSS is used throughout. Global styles in `app/ui/global.css`.
- **Icons**: Uses `@heroicons/react` for consistent iconography.

## Developer Workflows
- **Install dependencies**: `pnpm install`
- **Run dev server**: `pnpm dev` (or `pnpm next dev`)
- **Build for production**: `pnpm build`
- **Preview production build**: `pnpm start`
- **No custom test setup**: (No test scripts or test folders found)

## Integration Points
- **Data**: Uses placeholder/mock data in `app/lib/placeholder-data.ts`.
- **API routes**: See `app/query/route.ts` and `app/seed/route.ts` for serverless endpoints.
- **Public assets**: Images and static files in `public/`.

## Examples
- To add a new invoice form, see `app/ui/invoices/create-form.tsx` and use `createInvoice` from `app/lib/actions.ts`.
- For navigation, update `app/ui/dashboard/sidenav.tsx` and `app/ui/dashboard/nav-links.tsx`.

## Special Notes
- No custom ESLint, Prettier, or CI rules are present.
- This project is based on a Next.js course starter; follow idiomatic Next.js and Tailwind patterns unless otherwise specified.
