# Packages

Only `react-mediadrop` is published to npm — `packages/core` and `packages/xhr-upload` are internal, workspace-only source packages bundled directly into it at build time. `skills/mediadrop` is a separate integration guide, not bundled into the package. Only `react-mediadrop` matters if you're a consumer — the rest is listed here for contributors.

| Package | Published? | What it is |
| --- | --- | --- |
| [`packages/react`](https://github.com/autorender/react-mediadrop/tree/main/packages/react) | `react-mediadrop` | The `useMediaDrop` hook + the `react-mediadrop/xhr-upload` subpath |
| [`packages/core`](https://github.com/autorender/react-mediadrop/tree/main/packages/core) | internal | File intake, validation, drag/drop, upload-queue/retry primitives |
| [`packages/xhr-upload`](https://github.com/autorender/react-mediadrop/tree/main/packages/xhr-upload) | internal | Reference `XMLHttpRequest` upload transport |
| [`skills/mediadrop`](https://github.com/autorender/react-mediadrop/tree/main/skills/mediadrop) | — | Integration guide for coding agents |
