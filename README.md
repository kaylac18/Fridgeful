# Fridgeful

**Less waste. More dinner.** An interactive BUS 659 class prototype.

**[Open the live Fridgeful demo](https://fridgeful-bus659-kayla.tweedychicory1.chatgpt.site)**

The website is viewable by link. This repository is public: anyone can read or fork the source. For direct group editing, the owner should invite teammates under Settings → Collaborators. Website data remains local to each visitor's browser. GitHub changes are not automatically deployed; the hosting owner publishes reviewed revisions.

## Run locally

Use Node.js 22.13+ (Node 24 recommended).

```sh
npm ci
npm run dev
```

Open the Local URL printed by the server. For a production build use `npm run build`.

```sh
node --experimental-strip-types --test tests/planner.test.ts
npx tsc --noEmit
```

## What works

- Responsive dashboard, ingredient editing, image preview and a labeled sample scan.
- Household size, dinner budget, store label, vegetarian filter, time limit and planning priority.
- Six curated recipes, serving scaling, meal swaps, consolidated package-based shopping math.
- Text shopping-list export, clipboard copy, external Instacart handoff.
- Business SWOT/pricing hypotheses, segment personas and keyword-based pitch feedback.
- Product spec, demo script, incremental build prompts, tasks, editable owners/statuses and notes.
- Browser-local persistence and validated project JSON import/export. Merge tasks/notes or explicitly replace the household project.

## What is simulated or planned

There is no AI image recognition, live grocery pricing, AI recipe generation, automatic grocery cart, order placement, or live multi-user synchronization. Store preferences label lists; illustrative prices do not vary by store. Business outputs are hypotheses, not research. Photos stay in memory and do not persist after refresh.

## Work together

See [CONTRIBUTING.md](CONTRIBUTING.md), [the specification](docs/SPEC.md), [build prompts](docs/BUILD_PROMPTS.md), and [the testing checklist](docs/TESTING.md). Use the downloadable source ZIP or a shared GitHub repository. Repository access and website viewing are separate permissions.

The portable ZIP excludes the owner's Sites identity, credentials, node_modules and runtime state. Teammates can run locally and contribute through GitHub. The original project includes a Sites hosting manifest for its owner. Hosting on another service requires that service's adapter or export configuration; do not assume a server build works on GitHub Pages.

## Source map

- `app/page.tsx`: interactive application and project workspace.
- `app/globals.css`: responsive design.
- `lib/planner.ts`: typed recipe library and planning/shopping calculations.
- `tests/planner.test.ts`: meaningful calculation and constraint tests.
- `docs/`: specification, decisions, testing, demo and group prompts.

Food photography is loaded from Unsplash; images are illustrative and may not match the exact recipes. Fonts load from Google Fonts, with system fallbacks. The functional app does not depend on those requests succeeding.
