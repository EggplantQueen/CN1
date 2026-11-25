# NEX public laboratory feed

This directory contains **public editorial project records** read by the separate Telegram assistant `@CN1Nex_bot`. It is not CN1's private source-code repository or a production status monitor.

- [Current machine-readable feed](public-feed.json)
- [November 25, 2026: Guild Hall entrance, dice-tower corrections and modular tabletop terrain](updates/2026-11-25-guild-portal-and-tabletop-prototypes.md)
- [November 23, 2026: NEX-01, dice tower, original dice, workshop, Guild Hall and community progress](updates/2026-11-23-workshop-world-and-community.md)
- [November 3, 2026: MUTANT / GENESIS and NEX update](updates/2026-11-03.md)
- [November 4, 2026: Raid Bot, NEX X Radar pilot, and curated X discovery](updates/2026-11-04-x-community-tools.md)
- [November 4, 2026: MUTANT 3D laboratory — real machines, pending buttons, fluids and decor](updates/2026-11-04-mutant-lab-3d-progress.md)
- [November 6, 2026: MUTANT official entrance, public branding and Black Lab verification limits](updates/2026-11-06-mutant-public-entry.md)
- [November 6, 2026: owner-tested NEX welcome in Brazilian Portuguese; conversational expansion not yet live](updates/2026-11-06-nex-multilingual-welcome.md)

## How publication works

NEX reads `https://raw.githubusercontent.com/EggplantQueen/CN1/main/nex/public-feed.json` in read-only mode, normally checking about every **15 minutes**. A verified owner may also request `/nexsync` in a private NEX chat; it is rate-limited and sends **no public group announcement**.

An update is published by editing the JSON feed **only after** an approved, dated, public-facing note exists. Every edited feed must increase its integer `version`. `published_on` and every `as_of` date must not be in the future. Existing titles may be replaced with newer dated facts; older notes must not override more recent ones.

The current edition is **12**, published **November 25, 2026**, with 25 feed records. A recent-news overview accompanies the individual project records so broad questions can find concrete progress. Physical prototypes, successful owner tests and approved designs count as progress; describe their actual state instead of treating the absence of a public release as no news. Keep the overview current when publishing later editions.

For owner verification, `/nexsync` refreshes the source and `/nexfeed` reports the accepted edition. `/nexupdates` lists recent dated records; `/nexproject figurine` selects the physical NEX-01 record. `/brief` concerns private notes and reminders, not project news. Publishing the source is distinct from observing its acceptance by a running bot.

Every record has **exactly** these fields: `title`, `body`, `as_of`, `source`, `status`. The machine-readable `status` can be `reported_live`, `in_development`, `experimental`, `planned` or `unknown`. Even `reported_live` means *owner-reported*, not independently monitored production health.

Approved evidence links must point to public official CN1 sources. No private source repositories, internal operations, IP addresses, account records, API keys, tokens, unpublished URLs or unreviewed member data should appear here.

**Distinguish clearly:**
- design canon and roadmap are not shipped features;
- private test/previews are not public launches;
- a model or asset loading in an isolated test is not a verified public game;
- votes, NFT, paid XP or persistent creature evolution are only live once separately evidenced.

This public feed complements older built-in NEX facts. If fetch, validation or the latest revision fails, NEX should preserve the last valid record and **not invent current status**. For the complete technical contract, NEX's private release must be audited independently.
