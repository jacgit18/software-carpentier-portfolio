# software-carpentier

- Pull requests: never write the description by hand. Run `node scripts/pr-body.mjs --what "<what and why>" > body.md`, then `gh pr create --body-file body.md`.
- The npm manifest lives in `app/`; the dependency scan and Dependabot are pointed there (kit default is the repo root). Run `node ../scripts/dep-vet.mjs <name>` from `app/` to vet a package.
- Definition of done, CI budget: every GitHub Actions job has `timeout-minutes` (about 2x its worst run, 10 or less unless `# timeout-ok: why`); a workflow or test-suite change puts PR wall-clock and runner minutes before and after in the PR. Enforcer: `scripts/ci-timeouts.mjs` (`.github/workflows/ci-timeouts.yml`); the budget itself is advisory.
