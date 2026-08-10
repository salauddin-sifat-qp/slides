# D4X Sessions — Glossary

Talks aimed at teams consuming WickUI (product, design, dev, CSM) — communication workflow, WickUI dev-state updates, and cross-team feedback.

## Language

**Helium Heist**:
Internal codename for the Wick UI v2 launch announcement. Talk-flavor only — don't use it as if it's an official product name.
_Avoid_: "Wick UI 2.0 launch" (fine to use plainly instead)

**Customization Deprecation**:
The v2 policy that consumer teams can no longer override Wick UI component styles (Tailwind classes, `wu-*` classNames, or any other CSS override). Replacement path is a request through `#wick-ui-lib` or the weekly bookable session — not a class override.
_Avoid_: "styling restrictions", "breaking change" (it's framed as a support-channel redirect, not a breakage)

**Known Portal Conflicts**:
Current v2 issue: removing/updating 3rd-party libraries has caused some component portal conflicts, not yet resolved. Deliberately kept to a subtle one-line mention on the v2-live slide, not its own slide — v2 has been out over a month, giving it a dedicated beat overstates it. Named generically (no library names) — report via `#wick-ui-lib`.
_Avoid_: "zero breaking changes", "near-zero breaking changes" — no longer accurate, don't reuse from the original launch announcement

**Migration Phase**:
How v2 is framed to consumers: not the finished state, but a bridge release moving toward Base UI, CSS Modules, and fewer third-party dependencies — with small, low-impact breaking changes expected along the way — in preparation for v3.
_Avoid_: "v2 is done", "final v2"

**`#wick-ui-lib`**:
The single Slack channel for all WickUI-related bugs, feature requests, and questions from consumer teams.
_Avoid_: "support channel", "the wick-ui channel"

**John Wick Session**:
The weekly bookable slot for consumer teams needing deeper Wick UI help than a Slack message covers — named as a pun on the product name ("come with your issues, we'll shoot them away"). Booking link: https://calendar.app.google/adJNMBmHVS27xy6e8
_Avoid_: "weekly session", "office hours" (it has an actual name, use it)

**Current Version**:
v2.19.0 — update this before every session, it moves fast. All four packages (`wick-ui-lib`, `wick-ui-editor`, `wick-ui-i18n`, `wick-ui-icon`) share one version number and release in lockstep — no per-package version checking needed.

**Docs URL**:
`https://wick-ui.questionpro.com` — the confirmed production docs/Storybook site. `llms.txt` in the repo still points at a stale `wick-ui-lib.pages.dev` preview link — don't use that one on-slide.

**React 18 Sunset**:
React 18 support ends end of 2026 ("end of year" per the v2 announcement; year inferred from CHANGELOG dates, month not stated). Deliberately kept to "end of 2026" on-slide, not a specific month — confirm the exact date with devs before ever tightening this.

**Wick UI** (spelling):
Two words, capital U and I — matches the README/package naming. `WickUI` (no space) shows up informally in Slack but isn't the canonical spelling for slides/docs.

**Presenters**:
Sifat and Farhad (dev), Monz (design) present this session; Omar and Saiful help occasionally. Not the same as the shoutout teams (Admin2, Empower, CLF, Middleware), who are consumer teams being thanked, not presenters.

**Telemetry Scope**:
Build-time only — scans consumer app source for `Wu*` component + prop usage, plus `@npm-questionpro/wick-ui-*`/React versions from `node_modules`. No runtime user tracking, no PII. (Source: `wick-ui/apps/storybook/docs/i18n/README.md`.) Who has access to the aggregated data and whether there's an opt-out is not documented — open question if pressed live.

**Open gaps (not on slide, confirm before presenting)**:
- Turnaround SLA for a customization/feature request submitted via `#wick-ui-lib` — not stated anywhere; first question a dev in the room will ask.

**MCP Endpoint**:
`https://wick-ui.questionpro.com/mcp` — confirmed public endpoint. Setup docs: `wick-ui/apps/storybook/docs/guides/AIUsage.mdx` (Claude Code, Cursor, Copilot instructions + `AGENTS.md` project rules + prompt templates).

**AI Usage** (as a talk topic):
Distinct from bug/feature reporting (`#wick-ui-lib`) — it's "how to point your AI agent at Wick UI via MCP," not "how to ask a human for something." Own demo stop, don't fold into Requests.
