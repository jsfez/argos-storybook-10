# argos-storybook-10

React + TypeScript + Vite project with Storybook 10, visual testing integration for Argos CI, and quality tooling for linting/formatting.

## Stack

- React 19
- TypeScript 5
- Vite 8 (`@vitejs/plugin-react`)
- Storybook 10 (`@storybook/react-vite`)
- Storybook addons: Docs, A11y, Onboarding, Vitest addon, Chromatic integration
- Vitest 4 + Playwright (browser testing)
- Argos Storybook Vitest plugin (`@argos-ci/storybook`)
- ESLint 9 + `typescript-eslint`
- Biome 2 (formatting)

## Prerequisites

- Node.js 20+
- npm (lockfile is `package-lock.json`)

## Install

```bash
npm install
```

## Commands

```bash
npm run dev              # Start Vite dev server
npm run build            # Type-check and build production bundle
npm run preview          # Preview built app locally
npm run lint             # Run ESLint
npm run format           # Format code with Biome
npm run storybook        # Start Storybook on http://localhost:6006
npm run build-storybook  # Build static Storybook output
```

## Notes

- Storybook stories are loaded from `src/**/*.mdx` and `src/**/*.stories.*`.
- Vitest is configured in `vite.config.ts` to run Storybook browser tests with Playwright.
- Argos upload is enabled in CI via `uploadToArgos: !!process.env.CI`.
