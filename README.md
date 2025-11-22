# ProjectHub Packs

ProjectHub Packs is the canonical hub for community templates and libraries used with ProjectHub. The goals are:

- Offer ready-to-consume, best-practice templates and libraries.
- Provide a clear, strict submission pathway for contributors.
- Keep the catalog discoverable via the GitHub wiki and consistent in structure.

## Using this repository
- Browse the catalog in the [Wiki](../../wiki) for the latest packs, templates, libraries, and style guidance.
- Packs group assets by technology: `packs/<tech>/` and can include templates and/or libraries under that tech.
- Standalone items may also live under `templates/<category>/<name>/` or `libraries/<category>/<name>/` when not part of a pack.
- Each pack includes one `README.md`, `metadata.yaml`, and `LICENSE` at the pack root. Items inside a pack do not have their own README (keep per-item docs in the pack README or wiki). Item metadata is optional.
- Follow the README inside each item for quickstart instructions.

## Contributing (strict)
1. Read the full guidelines in [CONTRIBUTING.md](CONTRIBUTING.md) and the detailed steps in the Wiki’s “Submission Guide”.
2. Place contributions under the correct path (kebab-case names):
   - Packs: `packs/<tech>/` (may contain `templates/` and/or `libraries/` subfolders)
   - Templates: `templates/<category>/<name>/`
   - Libraries: `libraries/<category>/<name>/`
3. Include **all required files**: `metadata.yaml`, `README.md`, and `LICENSE` (at pack level and for each contained item).
4. Submit a PR and complete every checkbox in the PR template, including a note about the related Wiki update.
5. Hard gates: metadata lint workflow must pass. Soft gates: link/spell checks may fail but should be fixed unless there’s a reason.

## Governance
- Branch protection should require passing hard-gate checks before merge; squash merges recommended.
- Security reporting details are in [SECURITY.md](SECURITY.md).

## Getting help
Open an issue using the appropriate template (bug, new template request, doc fix).
