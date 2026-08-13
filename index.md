# react-mediadrop

**mediadrop** is a headless, hooks-first file uploader for React with zero runtime dependencies. It handles intake, drag/drop, validation, and upload (queue, concurrency, retry, cancel) via a single `useMediaDrop` hook — the same `getRootProps`/`getInputProps` shape you already know from react-dropzone, with upload built in. No prebuilt widget — you own the markup.

`react-mediadrop` ships at **4.4 KB minified + gzipped** (per [Bundlephobia](https://bundlephobia.com/package/react-mediadrop)); the optional `xhr-upload` transport is a separate subpath import, so you only pay for it if you use it.

- [Website](https://mediadrop.dev)
- [GitHub](https://github.com/autorender/react-mediadrop)
- [Discord](https://discord.gg/5snBtW2aJ)

## Why

We built mediadrop for Autorender's own upload widget — the entry point for every file and media asset into our pipeline. It went through several iterations before it looked like this: a lightweight, hooks-first, headless core, with a pluggable transport layer instead of one fixed upload path.

What came out of it is a set of ordinary React primitives — hooks, validation, a transport contract — the same shape whether you're wiring them into a media pipeline or a plain upload form. Autorender open-sourced mediadrop so any team building an uploader can start from the same primitives.

If you've used `react-dropzone`, the API will feel familiar — `useMediaDrop` returns the same `getRootProps`/`getInputProps` shape, plus a built-in upload queue react-dropzone doesn't have.

mediadrop is pre-1.0 (`0.1.1`), following semver — minor version bumps may include breaking changes until 1.0. Full history in the [changelog](https://github.com/autorender/react-mediadrop/blob/main/packages/react/CHANGELOG.md).
