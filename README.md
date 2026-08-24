Static GitHub Pages host for Arcadewick Killer Sudoku.

- Play: https://play.arcadewick.com
- github.io: https://allerance.github.io/arcadewick-web/
- Compiled web output only. Flutter source stays in the private allerance/arcadewick repo.

## Enable Pages (one-time, J.J.)

1. Repo Settings → Pages
2. Source: Deploy from a branch
3. Branch: `main` / root (`/`)
4. Custom domain: `play.arcadewick.com` (CNAME file is already in the repo)
5. After GitHub finishes the certificate, turn on **Enforce HTTPS**

## Recurring publish from private CI

Add repository secret `ARCADEWICK_WEB_TOKEN` on allerance/arcadewick:

- Type: fine-grained PAT
- Repository access: allerance/arcadewick-web only
- Permission: Contents Read and write

Then merge the arcadewick Pages CI PR so pushes to arcadewick `main` publish this site.
