# Qwik Template

A starter template for [bolt.diy](https://github.com/stackblitz-labs/bolt.diy).

## Purpose

This template is designed for use with **<https://github.com/stackblitz-labs/bolt.diy>**. bolt.diy fetches
these files at runtime and imports them into a fresh WebContainer project when you ask for a Qwik project,
so everything here needs to install and build with no extra setup.

Modified by [Dustin Loring](https://github.com/Dustinwloring1988) (Dustinwloring1988) in October 2026.

## Stack

| Package | Version |
| --- | --- |
| @builder.io/qwik | ^1.20.2 |
| @builder.io/qwik-city | ^1.20.2 |
| Vite | ^7.3.7 |
| TypeScript | ^6.0.3 |

Node 18.17.0 || ^20.3.0 || >=21.0.0 is required.

## Commands

```bash
npm install   # install dependencies
npm run dev   # vite --mode ssr — dev server
npm run build # qwik build — production build
npm run preview # qwik build preview && vite preview --open
npm run typecheck # tsc --incremental --noEmit
```

## About this template

A Qwik City project with SSR mode enabled. Qwik's fine-grained reactivity and lazy-loading means the
initial bundle is small. Qwik's peer range for Vite is `>=5 <8`, so Vite is held at 7.3.7.

## Upgraded to Qwik 1.20.2, Vite 7.3.7 (October 2026)

Moved from older Qwik and Vite 5/6. Each step was verified:
- @builder.io/qwik and @builder.io/qwik-city updated to 1.20.2 (latest 1.x)
- Vite was held at ^7.3.7 because Qwik's peer range explicitly caps Vite at `>=5 <8`. Upgrading Vite
  to 8 would break the build due to peer dependency conflicts.
- TypeScript was updated to ^6.0.3 (Qwik 1.20's peer range).

Vite 7.3.7 is the latest compatible with Qwik 1.20.2. Any Vite 8 upgrade would require Qwik to release
a new version with updated peer ranges, which was not available in October 2026.

## Verification

- `npm install` and `npm run build` pass without errors
- Confirmed the dev server starts and the Qwik lazy-loading works
- `npm run build` produces a production SSR build