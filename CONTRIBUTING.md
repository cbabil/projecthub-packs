# Contributing to ProjectHub Packs

Our contribution process is intentionally strict to keep quality high. Completing every step is required unless noted as "soft gate".

## Prerequisites
- Familiarize yourself with the catalog and style rules in the [Wiki](../../wiki).
- Use kebab-case names for directories and files.
- Choose an existing category when possible; propose a new one via issue if unclear.

## Directory and file layout
- Packs: `packs/<tech>/`
  - Required files: `metadata.yaml`, `README.md`, `LICENSE`
  - Optional subfolders (when present):
    - `templates/<name>/` (no separate README; item metadata optional)
    - `libraries/<name>/` (no separate README; item metadata optional)
- Standalone templates: `templates/<category>/<name>/` (require `metadata.yaml`, `README.md`, `LICENSE`)
- Standalone libraries: `libraries/<category>/<name>/` (require `metadata.yaml`, `README.md`, `LICENSE`)
- Use kebab-case for all path parts.

## `metadata.yaml` required fields (templates/libraries)
```yaml
name: my-template
summary: One-line purpose statement
language: javascript # or python, go, etc.
tags: [web, api, starter]
version: 0.1.0
license: MIT
compatibility: "ProjectHub >=1.0"
maintainer: "Name <email@example.com>"
```

## Pack-level `metadata.yaml` required fields
```yaml
name: node-rest-pack
technology: nodejs
summary: Starter assets for building REST APIs with Node.js
contents:
  - type: template          # template | workspace | configuration | library
    path: templates/basic-api
  - type: library
    path: libraries/logging-middleware
version: 0.1.0
license: MIT
compatibility: "ProjectHub >=1.0"
maintainer: "Name <email@example.com>"
tags: [node, rest, starter]
```

### `type` field
- Allowed values: `template`, `workspace`, `configuration`, `library`.
- Each entry in `contents` must include `type` and `path`.

## Pull request steps
1. Fork/branch and add your item in the correct path.
2. Ensure the required files exist and are filled out (pack level). Nested items in packs do not need their own README, license, or metadata; standalone items do.
3. Update the Wiki catalog entry (or add a note in the PR describing the required update). Soft gate: the PR can proceed but missing wiki updates slow review.
4. Submit the PR using the template and complete all checkboxes.
5. Confirm all required checks are green:
   - **Hard gates**: metadata lint + structure checks.
   - **Soft gates**: README link/spell checks. Fix these unless there is a justified exception.

## Issues
- Use the “New template request” issue template to propose categories or needed templates.
- Use the “Bug in template/library” template to report defects.
- Use the “Doc/wiki fix” template for documentation improvements.

## Style rules
- Keep READMEs concise: purpose, prerequisites, setup steps, usage example, config options, maintenance/updates.
- Prefer MIT or Apache-2.0 licenses; if different, explain why in the PR.
- Keep metadata accurate and updated when making changes.

## Code of Conduct
By participating, you agree to abide by the [Code of Conduct](CODE_OF_CONDUCT.md).
