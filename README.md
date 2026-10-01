# Section11 plugin for Claude

Marketplace go-live procedures for sellers and agencies, run by Claude against your
[Section11](https://section11.com) account. The plugin bundles the Section11 connector
(`https://section11.com/mcp`) and a set of skills.

| Skill | Ask it |
|-------|--------|
| `/section11:go-live-diagnosis` | "Why aren't my products live yet, and what do I fix first?" |

## Install

In Claude Code:

```
/plugin marketplace add section11com/claude-plugin
/plugin install section11@section11
```

Then turn on auto-update for the `section11` marketplace in `/plugin` → Marketplaces, so new
skills reach you as they ship.

The first time a skill runs, Claude asks you to sign in to Section11. You choose which accounts
the connection may read.

## What leaves your machine

The skills call the Section11 connector, which reads your Section11 data with the access you grant
when you sign in. It can also make a few changes, and Claude asks you to confirm each one: re-sync a
source, create a feed source or change a feed source's settings (credentials are only ever entered in
Section11), pause or resume a schedule, draft category rules (published in Section11), and start an
enrichment or publish to a marketplace within the product limits the account's admins set for AI apps
(per run and per 24 hours). Tool results go to Claude as part of the conversation. This repository
contains no customer data and no credentials.

## Contributing

This repository is exported from Section11's main codebase on every production release and
does not accept pull requests. Report problems at support@section11.com.
