# ETH Sessions — Glossary

Engineering Townhall talks. Each team takes a turn presenting on AI work in the new ~40-minute format.

## Format

**ETH (Engineering Townhall)** — A recurring all-engineering session. In the new format it has three segments: AI in Action, LivePoll, and Kudos.

**AI in Action** — The 30-minute main segment. It is demo-first: it shows what was actually built, implemented, or learned rather than slides about AI.

**LivePoll segment** — A 5-minute audience poll whose questions test the key concepts from AI in Action.
_Avoid_: Quiz (reserved for Library output)

**Kudos** — A 5-minute recognition of one team member's contribution.

## LivePolls engineering workflow

**Weekly Update** — The AI-generated engineering status report for LivePolls, posted to the #livepolls-bd Slack channel. It combines metrics (bugs, users, errors, query performance, tests) with task updates classified by deploy stage.
_Avoid_: Weekly report, status post

**Deploy stage**  — Where a change currently lives: Production (reachable from prod), Staging (merged to master, not yet in prod), or In Progress (open, unmerged).

**AI command** — A team-shared, repo-committed slash command (such as `/weekly-update`, `/commit`, `/pr`, `/pr-check`) that runs a written prompt on a model tier chosen for the task.
_Avoid_: Skill (pi-specific), macro

**Guardrail** — A deterministic, non-AI check that runs automatically on commit or push (lint, format, commit message, related tests). Work a Guardrail can do is never given to an AI command.
_Avoid_: Hook (implementation detail)

## LivePolls product AI

**AI question generation** — The existing LivePolls feature that drafts poll questions from a topic or an attached file, one request at a time.

**Library** — A proposed persistent collection of a user's source material (PDF, docs, later audio/video) that is indexed once so quizzes can be generated from any book or chapter quickly and repeatedly. It is a pitch only, not built yet.
_Avoid_: RAG (implementation detail), knowledge base

**Quiz** — A set of generated questions drawn from a specific part of the Library, such as a chapter.
