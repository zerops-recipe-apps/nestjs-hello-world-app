# nestjs-hello-world-app

Default NestJS 12 app scaffolded with `nest new`, running on Zerops `nodejs@24` with no external dependencies — baseline NestJS starter.

## Zerops service facts

- HTTP port: `3000`
- Siblings: —
- Runtime base: `nodejs@24`

## Zerops dev

`setup: dev` idles on `zsc noop --silent`; the agent starts the dev server.

- Dev command: `npm run start:dev`
- In-container rebuild without deploy: `npm run build`

**All platform operations (start/stop/status/logs of the dev server, deploy, env / scaling / storage / domains) go through the Zerops development workflow via `zcp` MCP tools. Don't shell out to `zcli`.**

## Notes

- NestJS 12 requires Node.js **v22.12+** (or v20.19+); `engines.node` is set to `>=24.0.0`.
- Prod build uses `npm ci`, `npm run build`, and `npm prune --omit=dev` — no manual node_modules swap.
