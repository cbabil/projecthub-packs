# ProjectHub Packs

ProjectHub Packs is the canonical hub for community templates and libraries used with ProjectHub. The goals are:

- Offer ready-to-consume, best-practice templates and libraries.
- Provide a clear, strict submission pathway for contributors.
- Keep the catalog discoverable via the GitHub wiki and consistent in structure.

## Using this repository
- Browse the catalog in the [Wiki](../../wiki) for the latest packs, templates, and guidance.
- Packs live under `packs/<pack-name>/` (current: `react-pack`, `python-pack`). Each pack includes `metadata.yaml`, `README.md`, `LICENSE`, and a `templates/` folder containing item folders listed in `metadata.yaml:contents`.
- Current packs do **not** use per-template metadata; everything is declared in the pack’s `metadata.yaml` with `type` (`template` or `workspace`) and `path` (relative to the pack root).
- Standalone items outside packs are not used at the moment; contribute via packs unless instructed otherwise.
- Follow the pack README for quickstart; pack install/update is via ProjectHub Settings → Packs using a ZIP of the pack root (no extra nesting).

## Current packs (this repo)

| Pack | Description | Version |
| --- | --- | --- |
| react-pack | React-focused assets including .gitignore | 0.1.0 |
| python-pack | Python-focused assets including .gitignore | 0.1.0 |

## Contributing (strict)
1. Read the full guidelines in [CONTRIBUTING.md](CONTRIBUTING.md) and the detailed steps in the Wiki’s “Submission Guide”.
2. Place contributions under the correct path (kebab-case names):
   - Packs: `packs/<pack-name>/` containing `metadata.yaml`, `README.md`, `LICENSE`, `templates/`
   - Templates/libraries outside packs: currently discouraged; align with maintainers before adding.
3. Include **all required files** at the pack root: `metadata.yaml`, `README.md`, `LICENSE`. Items inside the pack don’t need their own README unless specified by maintainers.
4. Submit a PR and complete every checkbox in the PR template, including a note about the related Wiki update.
5. Hard gates: metadata lint workflow must pass. Soft gates: link/spell checks may fail but should be fixed unless there’s a reason.

## Governance
- Branch protection should require passing hard-gate checks before merge; squash merges recommended.
- Security reporting details are in [SECURITY.md](SECURITY.md).

## Getting help
Open an issue using the appropriate template (bug, new template request, doc fix).

<!-- PROJECT SHIELDS -->
[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![License][license-shield]][license-url]
[![LinkedIn][linkedin-shield]][linkedin-url]

<!-- MARKDOWN REFERENCE LINKS -->
[contributors-shield]: https://img.shields.io/github/contributors/cbabil/projecthub-packs.svg?style=for-the-badge
[contributors-url]: https://github.com/cbabil/projecthub-packs/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/cbabil/projecthub-packs.svg?style=for-the-badge
[forks-url]: https://github.com/cbabil/projecthub-packs/network/members
[stars-shield]: https://img.shields.io/github/stars/cbabil/projecthub-packs.svg?style=for-the-badge
[stars-url]: https://github.com/cbabil/projecthub-packs/stargazers
[issues-shield]: https://img.shields.io/github/issues/cbabil/projecthub-packs.svg?style=for-the-badge
[issues-url]: https://github.com/cbabil/projecthub-packs/issues
[license-shield]: https://img.shields.io/github/license/cbabil/projecthub-packs.svg?style=for-the-badge
[license-url]: https://github.com/cbabil/projecthub-packs/blob/main/LICENSE
[linkedin-shield]: https://img.shields.io/badge/LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://www.linkedin.com/in/christophebabilotte/
