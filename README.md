# Needs Board
TODO: Overview

## Deployment

### Prerequisites
- Cloudflare
  - TODO
- Google auth
  - TODO
- Microsoft auth
  - TODO

### Initial deployment sequence
TODO: DB, DB initial migration, Backend, Frontend

### Database udpates
TODO: `wrangler d1 execute needs-board --file=packages/worker/migrations/<migrationName>`

### Backend
TODO: `cd packages/worker && wrangler deploy`

### Frontend
TODO: `cd packages/web && wrangler deploy disk --project-name=needs-board`

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

# Technical roadmap
- [ ] Scaffold repo
- [ ] Scaffold backend
  - [ ] Getting started guide
- [ ] Scaffold DB
- [ ] Deploy DB & backend
  - [ ] Flesh out guide
- [ ] Scaffold frontend
- [ ] Deploy frontend
  - [ ] Flesh out guide
- [ ] Configure auth
- [ ] Implement login
- [ ] Implement users
- [ ] Implement categories
- [ ] Implement needs
- [ ] Implement authorization