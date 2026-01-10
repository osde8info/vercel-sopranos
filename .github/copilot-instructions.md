# Copilot Instructions for Sopranos DVD Project

## Project Overview
This is a Next.js 16 application built with TypeScript and Tailwind CSS v4. The project is a simple landing page themed around "The Sopranos" DVD collection, featuring links to purchase on Amazon and Vercel deployment information.

## Tech Stack
- **Framework**: Next.js 16 (App Router)
- **Language**: TypeScript
- **Styling**: Tailwind CSS v4
- **Fonts**: Geist Sans and Geist Mono (Google Fonts)
- **Analytics**: Google Tag Manager
- **Linting**: ESLint with Next.js config

## Project Structure
- `app/` - Next.js App Router pages and components
  - `components/` - Reusable components
    - `GoogleTagManager.tsx` - Google Tag Manager integration component
  - `layout.tsx` - Root layout with metadata and fonts
  - `page.tsx` - Home page component
  - `globals.css` - Global styles with Tailwind imports
- `public/` - Static assets (Next.js logo, Vercel logo)
- Configuration files: `tsconfig.json`, `next.config.ts`, `eslint.config.mjs`, `postcss.config.mjs`

## Key Conventions
- Use TypeScript for all new components and utilities
- Follow Next.js App Router conventions
- Use Tailwind CSS classes for styling (v4 syntax)
- Support dark mode with `dark:` prefixes
- Use semantic HTML and accessibility best practices
- Import fonts and metadata in layout.tsx
- Use Next.js Image component for optimized images

## Development Workflow
- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run start` - Start production server
- `npm run lint` - Run ESLint

## Code Style
- Strict TypeScript configuration
- ES2017 target with modern features
- Path aliases: `@/*` maps to `./*`
- React JSX transform (not classic)
- Module resolution: bundler (for Next.js)

## Deployment
- Designed for Vercel deployment
- Static assets in `public/` directory
- Environment variables in `.env.local` (if needed)
- Google Tag Manager ID configured via `NEXT_PUBLIC_GTM_ID` environment variable

## Important Notes
- This is a marketing/landing page, not a full application
- Focus on performance and SEO
- Maintain the Sopranos theme and branding
- Keep dependencies minimal and up-to-date