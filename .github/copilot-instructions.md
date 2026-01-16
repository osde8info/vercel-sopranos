# Copilot Instructions for Sopranos DVD

- **Purpose**: Single-page Next.js 16 (App Router) landing for a Sopranos DVD CTA; no backend or data fetching. Core surface lives in [app/page.tsx](app/page.tsx).
- **Layout shell**: [app/layout.tsx](app/layout.tsx) wires Geist Sans/Mono via next/font, applies `antialiased`, injects [GoogleTagManager](app/components/GoogleTagManager.tsx), and imports global styles. Update metadata here for SEO.
- **Home composition**: Hero block centered with CTA links (Amazon DVD + Vercel) and Next Image logos; dark mode styles already present. Keep new sections minimal and aligned to the landing intent.
- **Styling**: Tailwind CSS v4 with inline `@theme` tokens in [app/globals.css](app/globals.css); background/foreground CSS variables drive light/dark. Prefer Tailwind utility classes; only extend globals if tokens/variables are needed.
- **Fonts**: Use the provided Geist variables (`--font-geist-sans`, `--font-geist-mono`) from the layout when adding typography to keep consistency.
- **Analytics**: [app/components/GoogleTagManager.tsx](app/components/GoogleTagManager.tsx) is a client component that reads `NEXT_PUBLIC_GTM_ID`; it warns and renders nothing when unset. Avoid duplicating GTM snippets elsewhere.
- **Paths & imports**: Path alias `@/*` maps to project root (see [tsconfig.json](tsconfig.json)); prefer absolute imports for new modules.
- **Assets**: Static logos live in `public/`; continue using Next Image for any new imagery and set `priority` only for above-the-fold assets.
- **Scripts**: `npm run dev|build|start|lint` from [package.json](package.json). Lint uses the Next.js ESLint config; keep TypeScript strict.
- **Design guardrails**: Maintain the Sopranos theme, keep copy concise, and ensure CTAs remain the focal point. Dark mode is already supported—carry `dark:` variants for new elements.
- **Performance/SEO**: Update metadata in the layout for new content; keep the page static-friendly and avoid client components unless necessary (GTM is the only one now).
- **Testing/debugging**: No tests are defined; validate manually via lint and local run. Check console for GTM warnings when `NEXT_PUBLIC_GTM_ID` is missing.