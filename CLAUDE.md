# software-carpentier

- Pull requests: never write the description by hand. Run `node scripts/pr-body.mjs --what "<what and why>" > body.md`, then `gh pr create --body-file body.md`.
- The npm manifest lives in `app/`; the dependency scan and Dependabot are pointed there (kit default is the repo root). Run `node ../scripts/dep-vet.mjs <name>` from `app/` to vet a package.
