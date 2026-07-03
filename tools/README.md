# Tools

Each subfolder here is one bioinformatics tool, built into its own Docker image.

```
tools/
└── <tool-name>/
    ├── Dockerfile   # required — the image definition
    └── README.md    # required — usage, supported versions, examples
```

Adding a new folder with a `Dockerfile` here is all that's needed — the GitHub Actions workflow automatically discovers it and publishes `ghcr.io/genomixcloud/<tool-name>` on every push to `main`.

See [../CONTRIBUTING.md](../CONTRIBUTING.md) for the full process.
