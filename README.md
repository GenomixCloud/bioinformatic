# GenomixCloud Bioinformatics Docker Images

Ready-to-use, versioned Docker images for the bioinformatics tools that power the [GenomixCloud](https://www.genomixcloud.com) genomics pipeline — shared freely with the bioinformatics and genomics community.

These are the same images we run in production. If you're building your own pipeline and need a reliable, pre-configured container for a common genomics tool, you're welcome to pull these directly instead of building your own from scratch.

## Why we're sharing this

Bioinformatics tooling is notoriously fiddly to install and version correctly — dependency hell, mismatched reference formats, undocumented flags. We already solved that problem for our own pipeline, so instead of every lab and every company re-solving it independently, we're publishing the images we depend on. Use them, fork them, improve them.

## Available tools

| Tool | Description | Image | Docs |
|------|-------------|-------|------|
| _coming soon_ | | | |

*(This table grows as tools are added — see [Contributing](#contributing) if you'd like to add one.)*

## Usage

Each tool lives in its own folder under [`tools/`](tools/) with its own `Dockerfile` and a short `README.md` covering usage, versioning, and any tool-specific notes.

```bash
# Pull a pre-built image (once published)
docker pull ghcr.io/genomixcloud/<tool-name>:latest

# Or build it yourself from source
git clone https://github.com/GenomixCloud/GenomixCloudPublicRepo.git
cd GenomixCloudPublicRepo/tools/<tool-name>
docker build -t <tool-name> .
```

## Contributing

Found a bug, want to bump a tool version, or have a genomics tool you'd like to see added? See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

Released under the [MIT License](LICENSE) — use freely, including commercially, with attribution.
