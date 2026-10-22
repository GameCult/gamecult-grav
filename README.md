# gamecult-grav

Archived content tree of the old GameCult website, which ran on the Grav CMS. It is kept as a record. It is not a live site and no running service depends on it.

**Do not deploy this repo.** `config/scheduler.yaml` still carries an enabled job that runs `php` every minute and fetches an obfuscated, base64-encoded remote URL. `config/plugins/git-sync.yaml` still points GitSync at this repository and carries tracked credential and webhook-secret fields. Treat both as compromised residue: inspect any host that ever ran this tree, and rotate whatever those fields protected. The `gamecult-ops` repo-census analysis (`docs/repo-census-2026-09/analysis/compensators.md`) holds the evidence and the recommended quarantine.

## What is here

- `pages/`: Grav page content (`01.home`, `02.aetheria`, `03.blog`, `04.typography`, `05.labor-platform`) and `pages/images/`.
- `themes/`: the `klb4` theme in use and the stock `quark` theme.
- `config/`: Grav site, system, scheduler, security and plugin configuration (`config/plugins/` holds `blackhole`, `git-sync`, `login`).

The last content commits are from 2022. A 2026 commit restored the GameCult logo asset.

## Where the live site is

The public `gamecult.org` site is built from `GameCult/gamecult-site` (Quartz). Aetheria lives at `https://aetheria.gamecult.org`. Go there for anything current; the only reason to open this repo is to recover an old page, image or blog post.
