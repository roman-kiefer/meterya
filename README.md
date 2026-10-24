# Meterya

Meterya helps you track household energy consumption and costs. This repository brings together parent issues that coordinate work across Meterya components and provides example files for installation with Docker Compose.

## Installation

- Prepare a Linux server with Docker Engine, the Docker Compose plugin, OpenSSL, and Caddy running on the host. Point your domain to the server, allow ports 80 and 443, and have SMTP credentials ready.
- Copy the repository's installation files to the server, keeping the `postgres` and `realm` subdirectories.
- Configure the included `.env` with your domain, image versions, SMTP settings, and unique passwords and secrets. Keep your configured `.env` private.
- Validate and start the services: `docker compose config --quiet`, `docker compose pull`, `docker compose up -d`, then `docker compose ps`.
- Configure the host Caddy for HTTPS, forwarding your domain to `127.0.0.1:8080`, and check `/health/ready` through your public HTTPS address.
- Follow the installation guide to create the first administrator and workspace, then restore the restriction on public access to the Keycloak administration interface.

## Documentation

See the [full installation guide](https://meterya.com/en/installation/) for configuration details, administrator setup, updates, and backups.

## Community

See the [contribution guide](CONTRIBUTING.md), [security policy](SECURITY.md), and
[accessibility information](ACCESSIBILITY.md). Please follow the
[Code of Conduct](CODE_OF_CONDUCT.md).

## License

Licensed under [AGPL-3.0-only](LICENSE). Copyright (c) 2026 Meterya contributors.
