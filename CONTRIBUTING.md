# Contributing to ProjectHub Packs

Our process is strict by design to keep quality high. Complete every step unless explicitly marked optional.

## Prerequisites
- Read the catalog and rules in the [Wiki](../../wiki).
- Use kebab-case for all folder/file names.
- Contribute via **packs** (preferred); standalone items are discouraged unless maintainers request them.

## Directory and file layout (current repo)
- Packs: `packs/<pack-name>/`
  - Required: `metadata.yaml`, `README.md`, `LICENSE`, `templates/`
  - Templates/workspaces live directly under `templates/` (no category subfolders today).
  - Items inside a pack do **not** have their own README/metadata; everything is declared at pack level.
- Standalone templates/libraries outside packs: avoid unless maintainers approve in an issue/PR discussion.

## Pack-level `metadata.yaml` (required fields)
```yaml
name: react-pack                 # matches folder name
technology: react                # display/filter tag
summary: React-focused assets including .gitignore
contents:                        # every item listed with type + path
  - type: template               # template | workspace
    path: templates/react-gitignore
  - type: workspace
    path: templates/react-workspace
version: 0.1.0                   # SemVer
license: MIT
compatibility: "ProjectHub >=1.0" # optional note
maintainer: "Name <email@example.com>"
tags: [react, node, gitignore]    # optional
releasedOn: 2025-11-20            # optional; shown as “Released On” if present
```

Rules:
- `path` is relative to the pack root and must exist in the ZIP.
- Allowed `type`: `template` or `workspace` (use `workspace` for full starters, `template` for configs/single-file drops).
- Per-template `metadata.yaml` is **not used**; keep metadata centralized.

## Pull request steps
1. Fork and branch; add your pack under `packs/<pack-name>/` with required files and updated `contents`.
2. Bump `version` and (if used) `releasedOn`.
3. Zip the pack root (no extra top-level folder) and confirm install via ProjectHub Settings → Packs using the ZIP URL (local `file://` is fine for test).
4. Update the Wiki page if structure or instructions change (or note the needed update in the PR).
5. Open the PR, complete all template checkboxes, and link to the test evidence.
6. Ensure checks pass:
   - **Hard gates:** metadata/structure lint.
   - **Soft gates:** link/spell checks—fix unless justified.

## Issues
- “New pack/template request” for new ideas.
- “Bug” for defects in existing packs.
- “Doc/wiki fix” for documentation tweaks.

## Style rules
- Keep READMEs concise: purpose, contents list, how to use, compatibility.
- Prefer MIT or Apache-2.0 licenses; justify exceptions.
- Keep metadata accurate and in sync with files and releases.

## Code of Conduct
By participating, you agree to abide by the [Code of Conduct](CODE_OF_CONDUCT.md).
