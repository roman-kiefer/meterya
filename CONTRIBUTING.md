# Contributing to Meterya

Contributions are welcome. This repository covers installation examples, Docker Compose, proxy routing, and changes spanning multiple Meterya components. For substantial changes, open a feature request before starting implementation so the approach can be discussed.

## Where to report issues

- [Meterya](https://github.com/roman-kiefer/meterya/issues/new/choose): installation, Compose, and cross-component issues.
- [Meterya API](https://github.com/roman-kiefer/meterya-api/issues/new/choose): backend, persistence, and the bundled Keycloak provider and theme.
- [Meterya App](https://github.com/roman-kiefer/meterya-app/issues/new/choose): web interface and browser behavior.

Search existing issues before opening a new one. If the responsible component is unclear, start in Meterya and link related component issues instead of copying the same report into several repositories.

Use the bug report or feature request form. List the API, Keycloak, and app image tags and, where possible, digests, plus the installation repository commit. The latest tag changes over time. Include the host operating system, CPU architecture, Docker Engine and Compose versions, and the relevant proxy setup.

Suspected vulnerabilities belong in the confidential process described in [SECURITY.md](SECURITY.md), not in public issues or pull requests.

## Protect private data

Use synthetic examples. Remove passwords, tokens, cookies, authorization headers, SMTP credentials, personal email addresses, household data, and identifying details from logs, screenshots, photos, and reproduction files. Do not attach configured `.env` files, rendered realm files, database dumps, or backups. Do not paste expanded `docker compose config` output.

## Development and validation

Fork the repository, create a focused branch from `main`, and read the README and any applicable `AGENTS.md` instructions. Keep unrelated formatting or refactoring out of the change.

Review the installation examples without using production credentials or data. With a private, disposable configuration, validate Compose without printing expanded secrets:

```sh
docker compose config --quiet
```

For proxy changes, validate both the gateway and host Caddy configurations using the Caddy version used by the deployment. Follow the installation guide for required environment variables and realm rendering. For runtime changes, use a disposable deployment to check readiness, sign-in, sign-out, and the restriction on public Keycloak administration. Do not run test deployments against production databases.

## Pull requests

Write new repository text, issue descriptions, commit messages, and pull requests in English. Existing German and English product translations and website documentation remain maintained in both languages.

Explain what changes and why, link relevant issues, and list the checks performed and their results. State explicitly when checks were skipped. Update documentation when behavior or configuration changes. Flag compatibility changes, database effects, and operator actions needed for deployment.

Maintainers manage release tags and image publication. A contribution does not need to publish an image or create a release.

## Community and licensing

Follow the [Code of Conduct](CODE_OF_CONDUCT.md). Report conduct concerns confidentially to [conduct@meterya.com](mailto:conduct@meterya.com). Communicate respectfully and keep discussion focused on the work.

By contributing, you agree that your contribution may be distributed under the repository's [license](LICENSE). Preserve existing third-party license notices.
