# Workspace

## Overview

pnpm workspace monorepo using TypeScript. Each package manages its own dependencies.

## Stack

- **Monorepo tool**: pnpm workspaces
- **Node.js version**: 24
- **Package manager**: pnpm
- **TypeScript version**: 5.9
- **API framework**: Express 5
- **Database**: PostgreSQL + Drizzle ORM
- **Validation**: Zod (`zod/v4`), `drizzle-zod`
- **API codegen**: Orval (from OpenAPI spec)
- **Build**: esbuild (CJS bundle)

## Key Commands

- `pnpm run typecheck` — full typecheck across all packages
- `pnpm run build` — typecheck + build all packages
- `pnpm --filter @workspace/api-spec run codegen` — regenerate API hooks and Zod schemas from OpenAPI spec
- `pnpm --filter @workspace/db run push` — push DB schema changes (dev only)
- `pnpm --filter @workspace/api-server run dev` — run API server locally

See the `pnpm-workspace` skill for workspace structure, TypeScript setup, and package details.

## Artifacts

### Portfolio (`artifacts/portfolio`)
- **Type**: React + Vite (frontend-only, no backend)
- **Preview**: `/` (root path)
- **Port**: 3000
- **Stack**: React, Vite, Tailwind CSS, Framer Motion, next-themes, react-icons, wouter
- **Features**: Single-page IT portfolio for Sree Nishruth Gone with light/dark theme toggle, smooth scroll navigation, animated sections (Hero, About, Skills, Projects, Certifications, Activities, Contact, Footer)
- All content populated from resume data
