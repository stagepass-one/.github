# Contributing to Stagepass

Thanks for helping. Bug reports, ideas and pull requests are welcome.

This is the default guide for the stagepass-one organization. If a repository has its own `CONTRIBUTING.md`, that one applies. For the CLI, loader and modules, read the [contributing guide in stagepass-one/os](https://github.com/stagepass-one/os/blob/master/CONTRIBUTING.md). It covers setup, the Docker test recipe and browser tests.

## Before you start

- Check the [docs](https://stagepass.one/docs/) and [troubleshooting](https://stagepass.one/docs/troubleshooting/) first. Many questions are answered there.
- Search [existing issues](https://github.com/stagepass-one/os/issues) before opening a new one.
- For larger changes, open an issue first so we can agree on the approach before you write code.
- Never report security issues in public. See [SECURITY.md](SECURITY.md).

## Pull requests

1. Fork the repository and branch from the default branch.
2. Keep changes small and focused. Update docs and tests when behaviour changes.
3. Make sure tests pass. In `os` this means the Docker test recipe on Node 22 and 24.
4. Describe what changed, why, and how you verified it.
5. Do not include secrets, tokens, private URLs or local machine paths.

Commit messages follow a short conventional style, for example `fix(cli): ...`, `docs: ...` or `chore: ...`.

## AI agents and releases

Stagepass is built with AI coding agents and tools. Commits and pull requests from agents come from the account [@stagepass-workforce](https://github.com/stagepass-workforce). The agents are fast, tireless and occasionally very sure of themselves, which is exactly why a human reviews every change.

- Merges, tags and npm releases are done by a maintainer, never by an agent.
- Publishing to npm needs a manual approval with two-factor authentication.
- CI runs on self-hosted runners.

AI-assisted contributions from the community are welcome too. You are responsible for reviewing every line you submit. Please do not name specific AI models or tools in project docs.

## Code of Conduct

By participating you agree to the [Code of Conduct](CODE_OF_CONDUCT.md).

## License

Contributions are licensed under the license of the repository you contribute to. For `os` that is the [MIT license](https://github.com/stagepass-one/os/blob/master/LICENSE).
