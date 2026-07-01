# Contributing

Please follow these conventions when contributing to the repository.

## General rules
- Keep the logical architecture vendor-neutral.
- Use Oracle-style solution document structure for volumes and chapters.
- Prefer concise, action-oriented writing.
- Keep diagrams editable (`drawio`, `plantuml`) and avoid image-only sources.
- Introduce architectural changes through ADRs.
- Update `README.md` and `ROADMAP.md` when scope changes.

## File naming
- Use lower-case, hyphen-separated file names.
- Prefix ADRs with zero-padded numbers when adding new records.
- Keep schema files versionable and human-readable.

## Review expectations
- Every new capability should describe purpose, inputs, outputs, and security implications.
- Every operational pattern should describe deployment, monitoring, and recovery expectations.
- Every OCI mapping should clearly separate logical intent from physical service choice.
