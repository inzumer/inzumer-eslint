# CLAUDE.md

`inzumer-eslint`: the `@inzumer/eslint` package (shared eslint flat configuration for inzumer projects (typescript, react, a11y, vitest)). Shared packages follow
`inzumer-<name>` → `@inzumer/<name>`; consumers are the Inzumer projects (Milimon, Zamuner) and the
other `inzumer-*` packages.

- Changing a rule or option affects every consumer: prefer additive changes, and use a
  `major` changeset for anything that would break their builds.
- `pnpm check` validates the package; `pnpm format` formats it.
- Conventional Commits for commits and PR titles; work on branches and open PRs to `main`.
- Every published change needs a changeset. Never commit or push unless asked.
