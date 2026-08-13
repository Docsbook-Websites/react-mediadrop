# Comparison

| Library | Model | Scope |
| --- | --- | --- |
| [react-dropzone](https://github.com/react-dropzone/react-dropzone) | Headless, hooks-first | Drag/drop and file intake only — no upload |
| [Uppy](https://uppy.io) | Dashboard UI + plugin ecosystem | Upload via `xhr-upload`/`tus`/`aws-s3` plugins, remote-provider import via Companion |
| [FilePond](https://pqina.nl/filepond) | Prebuilt widget | Styled, drop-in upload UI |
| **react-mediadrop** | Headless, hooks-first | File intake, validation, and upload (queue, concurrency, retry, cancel) via one hook — zero runtime dependencies |

Closest to react-dropzone in API shape — `useMediaDrop` returns the same `getRootProps`/`getInputProps`, plus the upload queue react-dropzone doesn't have. Closest to Uppy in upload scope — a pluggable transport contract instead of a plugin ecosystem — but without a dashboard, Companion, or remote-provider import; see the [scope reference](https://github.com/autorender/react-mediadrop/blob/main/skills/mediadrop/references/scope.md) in the repo for what's not included.
