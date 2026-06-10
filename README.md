# Cap with Docker Compose

<!-- markdownlint-disable-next-line MD001 -->
#### Table of Contents

1. [Description](#description)
2. [Setup](#setup)
3. [Usage](#usage)
4. [Reference](#reference)
5. [Development](#development)
6. [Contributors](#contributors)

## Description

[Docker Compose](https://docs.docker.com/compose/) setup for starting [Cap](https://trycap.dev/)
with [Traefik](https://traefik.io/) by [Solution Libre].

## Setup

```sh
cd /opt
git clone https://usine.solution-libre.fr/docker/cap.git cap
cd cap
```

Declare environment variables or copy the `.env.dist` to `.env` and adjust its values.

## Usage

```sh
cd /opt/cap
docker compose up -d
```

## Optional Integrations

This setup includes pre-configured labels for optional integrations with Traefik.
You can use them, customize them, or remove them based on your needs.

### Traefik (Reverse Proxy)

The Docker Compose file includes [Traefik] labels for automatic HTTPS routing and SSL certificate management.
This is **optional** and recommended for production deployments.

**To use Traefik:**

The labels are already configured in the compose file for Cap.
See [Solution Libre's Traefik setup](https://usine.solution-libre.fr/docker/traefik)
for a complete Traefik configuration compatible with this project.

> **Note:** The admin interface (root path `/`) is disabled by default for security reasons.
> To enable it, edit the `traefik.http.routers.cap.rule` label in `compose.yaml` as described in the inline comments.

## Reference

See [REFERENCE.md](./REFERENCE.md).

## Development

[Solution Libre]'s repositories are open projects,
and community contributions are essential for keeping them great.

[Fork this repo on our Cap](https://usine.solution-libre.fr/docker/cap/-/forks/new) or
[on GitHub](https://github.com/solution-libre/docker-cap/fork)

## Contributors

The list of contributors can be found at: <https://usine.solution-libre.fr/docker/cap/-/graphs/main>

[Solution Libre]: https://www.solution-libre.fr
[Traefik]: https://traefik.io/traefik
