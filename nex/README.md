# CN1 public knowledge feed for NEX 🧬

This folder contains PUBLIC project statements that NEX can read. **No source code, tokens, wallets, production infrastructure or unpublished project details belong here.**

## Updating a project

1. Finish, test and verify the real project change first.
2. Edit ONLY the relevant record in [public-feed.json](public-feed.json). Keep its `title` stable, adjust `body` and `as_of`, and select the accurate `status`:
   - `reported_live`: owner/public page reports the feature available (not independently checked by NEX)
   - `in_development`: actively being built, not a finished public release
   - `experimental`: prototype or test
   - `planned`: roadmap, not implemented
   - `unknown`: cannot responsibly confirm availability
3. Add an **official public source link** to the public CN1 repository or website. Do not link to a private PR or an inaccessible staging server.
4. Increment the top-level numeric `version` by one, update `published_on`, and get human review before merging to `main`.
5. After merge, NEX's proposed read-only adapter will check the public JSON at most every 15 minutes. It keeps its last valid cached copy if GitHub is unreachable and will **not** publish any Telegram announcement automatically.

## Rules

The `schema` must stay `cn1-nex-public-feed-v1`. Each record must have exactly `title`, `body`, `as_of`, `source` and `status`. Dates are ISO `YYYY-MM-DD` and are never future-dated. No duplicated title, no secrets, no private plans, no unreviewed community statements or project exclusions. Keep summaries short and factual.

**Source date is not deploy verification:** a GitHub file or green build alone does not prove a game is live. NEX must say “CN1 reports …” with the date when it cannot verify production.

Public repository: https://github.com/EggplantQueen/CN1

Private development stays private. Serious work. Terrible decisions. No bluffing.
