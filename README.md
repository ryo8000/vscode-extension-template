# vscode-extension-template

A template repository for developing VS Code extensions.

> [!IMPORTANT]
> This README describes the template itself. Replace it with the documentation for your own extension — `vsce` publishes `README.md` as the Marketplace page.

## Overview

A ready-to-use VS Code extension project: TypeScript, esbuild bundling, ESLint, and the VS Code test runner are already wired up. Clone it, run `npm install`, press `F5`, and you have a working Extension Development Host.

The scaffold is based on the output of [`yo code`](https://code.visualstudio.com/api/get-started/your-first-extension) (Yeoman + `generator-code`), with the placeholder values listed below.

## Structure

```text
.
├── .vscode/              # launch / tasks / recommended extensions
├── src/
│   ├── extension.ts      # extension entry point
│   └── test/             # integration tests run by @vscode/test-cli
├── esbuild.js            # bundler config
├── eslint.config.mjs
├── tsconfig.json
├── .vscode-test.mjs      # test runner config
└── package.json
```

## Getting started

```bash
npm install
npm run compile
```

Open this folder in VS Code and press `F5` to launch the Extension Development Host.
Run `Hello World` from the Command Palette (`Cmd+Shift+P`) to verify it works.

## Placeholders to replace

The template ships with generic values so that it builds and runs as-is. Replace them with your own before publishing.

| File | What to replace |
|---|---|
| `package.json` | `name` (`my-extension`), `displayName`, `description`, `publisher` (`my-publisher`), `author`, `license`, `repository`, `keywords`, `categories`, `icon` |
| `package.json` | `contributes.commands` — command IDs are prefixed with `my-extension.` |
| `src/extension.ts` | Command ID `my-extension.helloWorld` and the sample `Hello World` implementation |
| `CHANGELOG.md` | Extension name in the header |
| `LICENSE` | Copyright holder, or replace with the license of your choice |
| `README.md` | This file — replace with your extension's documentation |

`name` and `publisher` must stay valid npm/Marketplace identifiers, so avoid `{{...}}`-style tokens: keeping the values valid is what lets the template run without editing anything first.

`license` is set to `UNLICENSED` together with `private: true` as a safe default — pick a license deliberately before publishing.

## Key commands

| Command | Description |
|---|---|
| `npm run compile` | Type-check, lint, and build |
| `npm run watch` | Watch for file changes and auto-build |
| `npm test` | Run tests |
| `npm run package` | Generate a production bundle |

## Tech Stack

- TypeScript
- esbuild (bundler)
- ESLint
- `@vscode/test-cli` / `@vscode/test-electron` (testing)

## License

The template itself is MIT licensed (see [LICENSE](LICENSE)). Extensions generated from it are yours — replace `LICENSE` and the `license` field in `package.json` with whatever you choose.
