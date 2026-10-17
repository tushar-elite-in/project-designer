# Sample Brief 11 — Command-Line Backup Tool

> Illustrative sample input for planning practice. This is not a real assignment, contract, or fixed technology mandate.

## Problem Statement

Developers need a simple command-line utility to back up selected folders to a configured destination and verify that backups can be restored.

## Users
- Individual developer: configures paths, runs backups, and restores a chosen snapshot.
- Team administrator: publishes approved defaults and retention rules.

## Core requirements
- Provide commands to initialize configuration, run a backup, list snapshots, verify integrity, and restore files.
- Exclude configured paths and avoid following unsafe symlinks by default.
- Detect incomplete runs and report which files failed.
- Preserve timestamps and metadata where supported; document platform limitations.
- Support a dry-run preview and confirmation for overwriting existing files.
- Store credentials securely if a remote destination is supported.
- Return stable exit codes and machine-readable output mode.

## Data concepts
Config, BackupRun, Snapshot, FileManifest, ExclusionRule, Destination.

## Constraints to resolve
Choose supported operating systems, local versus remote destinations, encryption needs, retention, package format, and compatibility policy. Verify licensing and platform-specific file semantics.

## Optional ideas
Incremental backups, compression, remote cloud destination, scheduled runs.

## Acceptance and delivery
Show backup, integrity verification, dry run, exclusion, failed-file reporting, and safe restore on supported platforms. Provide installation, configuration, and recovery documentation.

You are required to build the application described below and demonstrate the role-based workflows.

## Frameworks to Be Used

These are the illustrative technology constraints for this sample brief:
- Python 3 with argparse, pathlib, hashlib, and logging.
- JSON configuration and manifest format.
- Local filesystem backup destination for core features.
- Remote cloud storage is optional and outside this sample scope.

## Notes

Choose supported operating systems, local versus remote destinations, encryption needs, retention, package format, and compatibility policy. Verify licensing and platform-specific file semantics.
- Demonstrate the core workflows in a reproducible local or documented test environment.
- Create or initialize required data through application code or versioned scripts; do not depend on manual database editing.

## Roles & Functionalities

### User / Developer
- Can initialize or edit a configuration, run a backup, list snapshots, verify integrity, and restore a selected snapshot.
- Can preview actions with a dry run and select exclusions.
- Must see clear errors for inaccessible files, incomplete backups, and unsafe restore paths.

### Team Administrator
- Can distribute a default configuration and retention policy.
- Can document a supported version and migration path for configuration changes.

### Maintainer
- Can package a release, publish a command reference, and review compatibility changes.

## Key Terminologies and Attributes

- Configuration: source paths, destination, exclusions, retention.
- Backup Run: ID, times, result, counts, failures.
- Snapshot: ID, creation time, manifest hash, file count.
- Manifest Entry: relative path, size, hash, timestamp, supported metadata.
- Restore Plan: snapshot, target path, overwrite policy, dry-run result.

The listed tables and attributes are starting points. Add fields or related tables only when required by a workflow, and document important relationships and integrity rules.

## Similar Apps

- Restic and BorgBackup are workflow references only; compatibility is not implied.

## Application Wireframe

A wireframe may be supplied separately to illustrate application flow and navigation. Exact UI replication is not mandatory unless the actual project statement says so. Maintain the intended functionality and navigation while designing an appropriate interface for the target platform.

## Core Features

1. Provide commands to initialize configuration, run a backup, list snapshots, verify integrity, and restore files.
2. Exclude configured paths and avoid following unsafe symlinks by default.
3. Detect incomplete runs and report which files failed.
4. Preserve timestamps and metadata where supported; document platform limitations.
5. Support a dry-run preview and confirmation for overwriting existing files.
6. Store credentials securely if a remote destination is supported.
7. Return stable exit codes and machine-readable output mode.

## Recommended and/or Optional Functionalities

- Incremental backups, compression, remote cloud destination, scheduled runs.
- Additional feature relevant to the stated user problem, provided all core features are complete.

## Evaluation and Submission

The sample project report should include: student/team details; the problem statement and approach; AI/LLM usage declaration; frameworks and libraries; ER/data-flow diagram where applicable; API endpoints/contracts where applicable; and a link to the demo video.


Submit the source code and required documentation in the format requested by the actual course or client. For this illustrative assignment format, package the project as a single ZIP and include setup instructions. The presenter should be able to explain the submitted code and demonstrate the required workflows.

## Possible Folder Structure

```text
src/ command parsing and backup library.
tests/ path safety, manifests, restore behavior.
docs/ command reference and recovery instructions.
examples/ sample configuration.
pyproject.toml/ packaging configuration.
```

## Video Presentation Guidelines

1. Short introduction (up to 30 seconds).
2. Explain the problem and approach (about 30 seconds).
3. Demonstrate the core features (about 90 seconds).
4. Mention additional features (about 30 seconds).

Keep the full video within the actual course/client limit. The original example brief suggests a 5–10 minute limit. Provide a link accessible to the reviewer and ensure the project can also be demonstrated live where required.

> This sample is modeled on the structure of the supplied Trekking Management project statement. Technology choices and requirements here are illustrative, not external or binding requirements.