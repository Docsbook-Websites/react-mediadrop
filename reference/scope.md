# What's implemented

**Core**: file intake from a picker or drag/drop, sync validation (`accept`/`maxFiles`/`minSize`/`maxSize` + a custom `validator`), and drag state (`isDragActive`/`isDragAccept`/`isDragReject`).

**Upload** (opt-in via `transport`): a pluggable transport contract, a queue with concurrency limit + shared retry/backoff, cancel via `AbortSignal`, and a reference `react-mediadrop/xhr-upload` transport.

Pause/resume, remote-provider import, OAuth, image transforms, a prebuilt widget, and any vendor-specific adapter are not implemented — see the [scope reference](https://github.com/autorender/react-mediadrop/blob/main/skills/mediadrop/references/scope.md) in the repo for the full, authoritative list.
