# NEX public laboratory feed

This directory contains **public editorial project records** read by the separate Telegram assistant `@CN1Nex_bot`. It is not CN1's private source-code repository or a production status monitor.

- [Current machine-readable feed](public-feed.json)
- [November 3, 2026: MUTANT / GENESIS and NEX update](updates/2026-11-03.md)
- [November 4, 2026: Raid Bot, NEX X Radar pilot, and curated X discovery](updates/2026-11-04-x-community-tools.md)
- [November 4, 2026: MUTANT 3D laboratory — real machines, pending buttons, fluids and decor](updates/2026-11-04-mutant-lab-3d-progress.md)

## How publication works

NEX reads `https://raw.githubusercontent.com/EggplantQueen/CN1/main/nex/public-feed.json` in read-only mode, normally checking about every **15 minutes**. A verified owner may also request `/nexsync` in a private NEX chat; it is rate-limited and sends **no public group announcement**.

An update is published by editing the JSON feed **only after** an approved, dated, public-facing note exists. Every edited feed must increase its integer `version`. `published_on` and every `as_of` date must not be in the future. Existing titles may be replaced with newer dated facts; older notes must not override more recent ones.

Every record has **exactly** these fields: `title`, `body`, `as_of`, `source`, `status`. The machine-readable `status` can be `reported_live`, `in_development`, `experimental`, `planned` or `unknown`. Even `reported_live` means *owner-reported*, not independently monitored production health.

Approved evidence links must point to public official CN1 sources. No private source repositories, internal operations, IP addresses, account records, API keys, tokens, unpublished URLs or unreviewed member data should appear here.

**Distinguish clearly:**
- design canon and roadmap are not shipped features;
- private test/previews are not public launches;
- a model or asset loading in an isolated test is not a verified public game;
- votes, NFT, paid XP or persistent creature evolution are only live once separately evidenced.

This public feed complements older built-in NEX facts. If fetch, validation or the latest revision fails, NEX should preserve the last valid record and **not invent current status**. For the complete technical contract, NEX's private release must be audited independently.
