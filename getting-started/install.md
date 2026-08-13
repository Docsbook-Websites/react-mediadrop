# Install

```sh
pnpm add react-mediadrop
# or: npm install react-mediadrop
# or: yarn add react-mediadrop
```

Using an AI coding agent? Also install the Agent Skill so it integrates the API correctly on the first try instead of guessing from the package name:

```sh
npx skills add autorender/react-mediadrop
```

Also indexed on [Context7](https://context7.com/autorender/react-mediadrop) — reachable via MCP from Cursor, Claude Code, Windsurf, and other Context7-compatible tools with no local install.

- Ships as **ESM** with TypeScript types included — works with any modern bundler.
- Peer dependency on React 18+, nothing else.
- No `window`/`document` access at render time — safe to import in SSR frameworks (Next.js, Remix, etc.); browser APIs only run inside event handlers, on the client.
