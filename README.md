# Project Orpheus

**Recognition • Recovery • Recollection**

Project Orpheus is an open-source exploration into audio identity, archive recovery, acoustic fingerprinting, metadata restoration, and musical memory.

The project began with a simple problem:

> Given an unknown or poorly tagged audio file, can we determine what it is, recover accurate metadata, and preserve it for future discovery?

Longer term, Orpheus explores motif recognition, melody matching, segment identification, and audio recollection from humming, whistling, or partial recordings.

---

## Mission

Project Orpheus seeks to:

- Recognize audio assets from content rather than filenames
- Recover lost or damaged metadata
- Preserve music collections and archives
- Recollect audio through search, fingerprints, motifs, and musical patterns
- Build a reproducible and transparent workflow

---

## Core Principles

- Do not trust filenames
- Do not trust embedded tags
- Preserve original media
- Preserve UTF-8 metadata
- Prefer deterministic processing
- Record confidence scores
- Require human review when confidence is low

---

## Current Milestone

**Phase 1 — Archive Recovery**

Current Focus:

- Repository scaffolding
- Database schemas
- ZIP ingestion
- Audio validation

---

## Workflow

| Step | Name | Purpose | Input | Output | Script | Human Review |
|------|------|---------|-------|--------|--------|--------------|
| 01 | INGEST | Register ZIPs and audio files into the workflow | ZIP, MP3, FLAC, WAV | Inventory records | `ingest_zip.py` | No |
| 02 | VALIDATE | Verify files are valid audio assets | Registered files | Audio metadata | `validate_audio.py` | No |
| 03 | EXTRACT | Extract embedded tags and technical information | Audio files | Artist, Album, Title, Codec, Duration | `extract_metadata.py` | No |
| 04 | FINGERPRINT | Generate recording fingerprints | Audio files | Fingerprints | `fingerprint.py` | No |
| 05 | LOOKUP | Query public music databases | Fingerprints | Candidate matches | `lookup.py` | No |
| 06 | SCORE | Evaluate candidate matches | Candidate matches | Confidence scores | `confidence.py` | No |
| 07 | REVIEW | Route uncertain matches for validation | Scored matches | Review items | `review.py` | Yes |
| 08 | REGISTER | Approve and register confirmed identities | Approved matches | Canonical track records | `register.py` | Optional |
| 09 | ARCHIVE | Move and rename files into archive structure | Registered tracks | Organized archive | `archive.py` | Optional |
| 10 | REPORT | Generate reports and statistics | Database | Reports | `report.py` | No |

---

## Confidence Actions

| Confidence | Action |
|------------|--------|
| >= 95% | Auto Register |
| 75% - 94.99% | Human Review Queue |
| < 75% | Manual Investigation |

---

## Repository Layout

```text
project-orpheus/
├── README.md
├── docs/
├── schemas/
├── scripts/
├── data/
├── output/
└── tests/
```

---

## Local Documentation

| Area | README | Purpose |
|------|--------|---------|
| Documentation | [docs/README.md](docs/README.md) | Design notes, architecture, UTF-8 policy, confidence model, and phase plans |
| Schemas | [schemas/README.md](schemas/README.md) | Database schema files and migration order |
| Scripts | [scripts/README.md](scripts/README.md) | Script responsibilities, execution order, and command examples |
| Data | [data/README.md](data/README.md) | Local input, working, and archive directories |
| Output | [output/README.md](output/README.md) | Generated databases, reports, and review artifacts |
| Tests | [tests/README.md](tests/README.md) | Test strategy and sample validation cases |

---

## Project Documentation

| Document | Description |
|----------|-------------|
| [Architecture](docs/architecture.md) | System architecture and design decisions |
| [Confidence Model](docs/confidence.md) | Match scoring and approval workflow |
| [UTF-8 Policy](docs/utf8.md) | Character encoding and metadata preservation |
| [Archive Recovery](docs/phase1_archive_recovery.md) | Phase 1 implementation plan |

---

## Research Roadmap

| Phase | Name | Goal |
|-------|------|------|
| Phase 1 | Recognition | Identify recordings and recover metadata |
| Phase 2 | Recovery | Build archive registration and organization |
| Phase 3 | Segment Matching | Match clips and excerpts to recordings |
| Phase 4 | Motif Recognition | Match melodies and musical patterns |
| Phase 5 | Recollection | Search via humming, whistling, or singing |

---

## Development Philosophy

Project Orpheus intentionally starts simple.

Rather than building a distributed platform or complex framework, the project begins with small, understandable Python scripts connected through a reproducible workflow.

The objective is understanding the mechanics before introducing abstraction.

---
## Support

Project Orpheus is maintained by Wayne Kirk Schmidt.

If you find the project useful, have suggestions, discover issues, or would like to collaborate on archive recovery, audio identity, metadata restoration, or motif recognition research, please reach out.

### About

Project Orpheus began as an exploration into recovering identity from damaged audio archives, including files with missing metadata, corrupted tags, and incomplete naming conventions.

The long-term vision extends beyond archive recovery into musical recollection, allowing users to identify, recover, and rediscover audio through fingerprints, motifs, and memory.

### Contact

- Website: https://www.waynekirkschmidt.me
- GitHub: https://github.com/wayne-kirk-schmidt
- LinkedIn: https://www.linkedin.com/in/waynekirkschmidt/

### Related Projects

- Project Orpheus

### Contributing

Contributions, ideas, bug reports, and research discussions are welcome.

Please open an Issue or Pull Request to begin the conversation.

### Project Motto

**Recognition • Recovery • Recollection**

*Recovering identity through sound.*

---

## License

This project is licensed under the MIT License.

See [LICENSE](LICENSE) for details.

