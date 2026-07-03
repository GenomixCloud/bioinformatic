![GitHub commit activity](https://img.shields.io/github/commit-activity/m/GenomixCloud/bioinformatic?style=flat-square) ![Twitter Follow](https://img.shields.io/twitter/follow/genomixcloud?style=social)

[Genomix Cloud](https://genomixcloud.com/) is a cloud platform that gives researchers, bioinformatic specialists, and other genomics professionals a powerful suite of bioinformatics tools to analyze and interpret genomic data.

We've already built and battle-tested a lot of this tooling for our own pipelines. Rather than keep it locked away, we're publishing pieces of it here for the wider bioinformatics community — free to use, fork, and improve.

---
Start here
[Genomix Cloud Docker images repository](https://hub.docker.com/u/genomixcloud) — ready-to-use Docker images for common bioinformatics tools (Abricate, Bakta, CheckM, FastQC, Kraken2, SPAdes, and more), the same ones we run in production.

---

More tools will land here as we open-source more of our stack.

---

Please note that this repository is continuously evolving and includes the source code for our Docker images. You will find in this repository instructions on building the Docker images used in our various workflows. Additionally, we provide suggestions on enhancing performance and automation within the AWS ecosystem.

The repository hosts the plain images of the bioinformatic tools that are part of the Genomixcloud platform. These images form the foundation for our suite of bioinformatic tools and can help support various genomic analysis tasks.

| Tool | Version | License |
|---|---|---|
| [Abricate](abricate) | 1.0.0 | GPL-2.0 |
| [Bakta](bakta) | 1.11.4 | GPL-3.0 |
| [CheckM](checkm) | 1.2.4 | GPL-3.0 |
| [FastQC](fastqc) | 0.12.0 | GPL-3.0-or-later |
| [FastP](fastp) | 1.0.1 | MIT |
| [FimTyper](fimtyper) | — | — |
| [Kraken2](kraken2) | 2.1.6 | MIT |
| [MacSyFinder](macsyfinder) | — |
| [Mlst](mlst) | 2.23.0 | GPL-2.0 |
| [Pilon](pilon) | 1.23 | GPL-2.0-only |
| [Platon](platon) | 1.7 | GPL-3.0 |
| [Prokka](prokka) | — | — |
| [Quast](quast) | 5.2.0 | GPL-2.0-only |
| [Roary](roary) | 3.13.0 | GPL-3.0 |
| [SPAdes](spades) | 3.15.3 | GPL-2.0-only |

Versions above reflect what's currently packaged in each tool's Dockerfile. FimTyper and Prokka versions aren't tracked yet — see [CONTRIBUTING.md](CONTRIBUTING.md) if you'd like to help document them.

**Note on licensing:** the MIT license below covers this repository's own Dockerfiles, scripts, and documentation. Each wrapped tool keeps its own upstream license (see table above), and some tools support optional reference databases with their own separate usage terms — check the tool's own documentation before relying on any bundled database for commercial work.

---

## Contributing

Found a bug, want to bump a tool version, or have a bioinformatic tool you'd like to see added? See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

Released under the [MIT License](LICENSE) — use freely, including commercially, with attribution.

See [Manifest.md](Manifest.md) for the full product manifest (purpose, roadmap, design principles).
