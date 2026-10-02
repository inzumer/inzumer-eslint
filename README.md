# @inzumer/eslint

Shared ESLint flat configuration for Inzumer projects (TypeScript, React, a11y, Vitest). Part of the Inzumer shared packages (one repository per package:
`inzumer-<name>` published as `@inzumer/<name>`).

## Install

```sh
pnpm add -D @inzumer/eslint
```

## Usage

```js
// eslint.config.mjs
import { base, react, testing } from '@inzumer/eslint';

export default [...base, ...react, ...testing];
```

| Export    | Adds                                                                                        |
| --------- | ------------------------------------------------------------------------------------------- |
| `base`    | TypeScript, imports (`import-x`), unused imports, blank line after `if` and before `return` |
| `react`   | React, hooks and `jsx-a11y`                                                                 |
| `testing` | Vitest rules for `*.test.*` files                                                           |

Needs `eslint` 9 or later as a peer dependency.

## Releases

[Changesets](https://github.com/changesets/changesets): add a changeset (`pnpm changeset`) with each
change. On `main`, `.github/workflows/release.yml` opens a "Version Packages" PR and, when it is
merged, publishes to npm (needs the `NPM_TOKEN` repository secret).

Previously @inzumer/eslint-config (private, in ui-library).
