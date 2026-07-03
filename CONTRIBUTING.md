# Contributing

Thanks for considering a contribution to the GenomixCloud bioinformatics Docker images. This project is community-facing — improvements from outside GenomixCloud are welcome.

## Ways to contribute

- **Report a problem** — open an [issue](../../issues) describing the tool, the image tag/version, and what went wrong.
- **Improve an existing tool** — e.g. bump a version, fix a broken dependency, reduce image size, add a missing flag.
- **Add a new tool** — propose it in an issue first so we can confirm it fits before you invest time building it.

## Adding or updating a tool

1. Fork the repo and create a branch.
2. Each tool lives in its own folder at the repo root, e.g. `<tool-name>/`:
   - `Dockerfile` — the image definition
   - `README.md` — what the tool does, supported versions/tags, example usage, any quirks
   - `conf/` — tool configuration (optional, tool-dependent)
   - `src/` — helper scripts run inside the container (optional, tool-dependent)
3. Keep images minimal — prefer slim/alpine base images where the tool supports it, and multi-stage builds to avoid shipping build-time dependencies.
4. Pin tool versions explicitly (avoid `:latest` inside the Dockerfile itself) so builds are reproducible.
5. Test that the image builds locally:
   ```bash
   cd <tool-name>
   docker build -t <tool-name>:test .
   docker run --rm <tool-name>:test <tool-command> --version
   ```
6. Update the tools list in the root [README.md](README.md).
7. Open a pull request describing the change.

## Review

Once a PR is merged, our GitHub Actions workflow automatically builds and publishes the updated image to the GitHub Container Registry (`ghcr.io/genomixcloud/<tool-name>`).
