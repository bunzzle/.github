# Contributing

Thanks for helping. Bunzzle is small and young, so the rules are few.

## Before you start

- **Open an issue first** for anything bigger than a typo. Say what you want to change and why, and wait for a reply before writing code. This saves your time if the change does not fit.
- Issues marked `good first issue` are a good place to start.
- Security problems never go in a public issue. See [SECURITY.md](SECURITY.md).

## Setup

You need [Bun](https://bun.sh). Nothing else.

```sh
git clone https://github.com/bunzzle/bunzzle
cd bunzzle
bun install
bun run check
```

`bun run check` runs the type check, the linter and all tests. It must pass before you open a pull request.

## How the code is written

- **Bun only.** No Node-only APIs, no frameworks, no ORMs.
- **New dependencies need an issue first.** Bunzzle runs on Bun and zod; every new package is something users have to trust.
- **No comments in code.** Names and small functions carry the meaning. Explain the why in the pull request.
- Biome formats and lints: `bun run format`.
- Every parser that reads outside input gets a fuzz test.

## Pull requests

- One change per pull request. Link the issue: `Closes #12`.
- The title becomes the commit message on `main`, so write it in the [Conventional Commits](https://www.conventionalcommits.org) format: `fix: retry on 421 replies`, `feat: add domain limits to keys`, `docs: explain PTR records`.
- Pull requests are squash-merged by a maintainer.

## License

By contributing, you agree that your work is released under the license of the repository you contribute to (AGPL-3.0 for the engine, MIT for the website).
