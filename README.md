<p>
  <img src="assets/projecthub-packs.png" alt="ProjectHub Packs" width="320" align="left" style="margin-right:12px;">
  <em>ProjectHub Packs: curated, versioned templates and starters installable via a single ZIP URL.</em>
</p>

<br clear="both">

<br>

[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![License][license-shield]][license-url]

ProjectHub Packs is the **official marketplace** for community templates and libraries used with ProjectHub. This repository is built into ProjectHub by default—users can install packs from here without any configuration.

We aim to:

- Offer ready-to-consume, best-practice templates and libraries.
- Provide a clear, strict submission pathway for contributors.
- Keep the catalog discoverable via the GitHub wiki and consistent in structure.

## Using this repository
- Browse the catalog in the [Wiki](../../wiki) for the latest packs and guidance.
- Packs live under `packs/<pack-name>/` (current: `react-pack`, `python-pack`). Each pack includes `metadata.yaml`, `README.md`, `LICENSE`, and a `templates/` folder containing item folders listed in `metadata.yaml:contents`.
- Releases publish one ZIP per pack **and** a `packs-manifest.json` that lists name, description, version, license, technology, download filename, and SHA-256 checksum. ProjectHub reads this manifest to show pack details without downloading ZIPs.
- Current packs do **not** use per-template metadata; everything is declared in the pack’s `metadata.yaml` with `type` (`template` or `workspace`) and `path` (relative to the pack root).
- Standalone items outside packs are not used at the moment; contribute via packs unless instructed otherwise.
- Install/update via ProjectHub Settings → Packs using a ZIP of the pack root (no extra nesting).

## Current packs (this repo)

| Pack         | Description                                | Version |
| ------------ | ------------------------------------------ | ------- |
| react-pack   | React-focused assets including .gitignore  | 0.2.1   |
| python-pack  | Python-focused assets including .gitignore | 0.2.1   |

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

## Creating your own marketplace

Want to host your own packs? ProjectHub supports multiple marketplaces. Users can add your marketplace alongside the official one.

1. Create a GitHub repository with packs under `packs/<pack-name>/`
2. Publish releases with ZIP files and a `packs-manifest.json`
3. Users add your marketplace via `owner/repo` in Settings → Packs

See the [Wiki: Authoring a Pack](../../wiki/Authoring-a-pack#creating-your-own-marketplace) for full instructions.

## Getting help
Open an issue using the appropriate template (bug, new template request, doc fix).

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
