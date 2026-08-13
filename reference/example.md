# Example

`examples/react-demo` exercises `react-mediadrop` against a real backend (`examples/test-server`, a plain Express app) instead of a faked dev-server mock.

| Example | Binding | Transports covered |
| --- | --- | --- |
| [`react-demo`](https://github.com/autorender/react-mediadrop/tree/main/examples/react-demo) | `react-mediadrop` | `react-mediadrop/xhr-upload` |
| [`test-server`](https://github.com/autorender/react-mediadrop/tree/main/examples/test-server) | — | Real Express backend for `react-demo` |

```sh
# terminal 1 — backend, listens on http://localhost:8787
pnpm --filter test-server dev

# terminal 2 — frontend
pnpm --filter react-demo dev
```

Open the demo, drop a file, hit "Upload all" — bytes land in `examples/test-server/uploads/` (git-ignored).

## Commands

```sh
pnpm install
pnpm build
pnpm test
pnpm typecheck
pnpm lint
pnpm size    # checks each published/bundled package's gzipped dist against its size budget
```
