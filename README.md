# Rustzen Platform

> Migrated to [`rustzen/rustzen-hub`](https://github.com/rustzen/rustzen-hub) under `apps/console`.
> This repository is now a legacy source snapshot. Make new console/API changes
> in `rustzen-hub/apps/console`.

Rustzen Platform is the admin dashboard and platform API surface for Rustzen macOS products.

## Scope

- Product, license, device, order, and version management dashboard
- License activation and version-check API routes
- Billing checkout and webhook handling for Rustzen Clear Pro
- Legacy Lemon Squeezy webhook handling
- License server proxy endpoints
- PostgreSQL access through Prisma

## Stack

- Next.js App Router
- React
- TypeScript
- Tailwind CSS
- Prisma
- PostgreSQL
- Vercel

## Development

```bash
pnpm install
pnpm dev
```

Useful checks:

```bash
pnpm db:generate
pnpm db:verify
pnpm lint
pnpm build
```

## Environment

Copy `.env.example` to `.env.local` and configure the database, dashboard auth,
license server, billing provider API key, product identifier, and webhook secrets.

For local database validation, PostgreSQL 17 from Homebrew can be used with a
local `rustzen_console_test` database.
