# Needs Board
TODO: Overview

## Deployment
### Initial deployment sequence
TODO: DB, DB initial migration, Backend, Frontend
1. Update packages/board-worker/wrangler.jsonc
   1. Update "compatibility_date" to today
   1. Clean out the existing "d1_databases" entry
1. `cd packages/board-worker`
1. `pnpm exec wrangler d1 create board-db`
   1. Copy the output into wrangler.jsonc
1. `pnpm exec wrangler deploy`
1. `cd ../web`
1. `wrangler pages deploy dist --project-name=board-frontend`

### Database udpates
`wrangler d1 execute board-db --file=packages/worker/migrations/<migrationName>`
TODO: Make this part of app startup? Simpler.

### Backend
`cd packages/worker && wrangler deploy`

### Frontend
`cd packages/web && wrangler deploy disk --project-name=board-frontend`

### Prerequisites
- Cloudflare
  - TODO
- Google auth
  - TODO
- Microsoft auth
  - TODO

## Technical overview
TODO: Constraints, free, easy to set up for non-technical people
TODO: Tech stack
- Frontend: Cloudflare Pages: React + Vite
- Backend: Cloudflare Workers: Hono
- Database: Cloudflare D1: SQLite

## Development

### Prerequisites
- [Node 26](https://nodejs.org/en/about/previous-releases)
  - Recommended: [fnm](https://github.com/Schniz/fnm)
  - Recommended: [pnpm](https://pnpm.io/installation)
- Run `pnpm ci`

### Run backend
TODO: Command
TODO: .vscode/.launch config?

### Run frontend
TODO: Command
TODO: .vscode/.launch config?

# Technical roadmap
- [x] Scaffold repo
  - [x] Getting started guide
- [ ] Scaffold backend
- [ ] Scaffold DB
- [x] Deploy DB & backend
  - [x] Flesh out guide
- [ ] Scaffold frontend
- [ ] Deploy frontend
  - [ ] Flesh out guide
- [ ] Configure auth
- [ ] Implement login
- [ ] Implement users
- [ ] Implement categories
- [ ] Implement needs
- [ ] Implement authorization
- [ ] Implement comments on need, only visible to attached users