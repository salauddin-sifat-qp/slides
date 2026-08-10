# AI Sessions — Glossary

## Program
**AI-Native Software Engineer Program** — A series of 36 sessions across 8 phases, currently in beta. Teaches software engineers how to use AI in coding and beyond.

**Phase** — A thematic grouping of sessions (8 total: Foundations, Development, Learning, Applications, Teams, Production, Leadership, Future).

**Session** — A single live talk in the program. Sessions 1 and 2 are delivered as one combined 50-minute talk.

## Concepts

**Token** — The unit of text an LLM processes. Numeric representation of a text chunk. Not a word, not a character — a subword chunk from the model's vocabulary. Determines cost and context limits.

**Context Window** — The LLM's working memory. Fixed token limit. When full, early information is lost. Understanding this changes how you prompt.

**Harness** — The runtime scaffolding around an LLM call: system prompt, tool definitions, loop logic, and context injection. The thing that separates a raw API call from an agent. A good harness drastically changes output quality.

**Agent CLI** — A tool (e.g. pi, Claude Code, Cursor) that wraps a harness for use in a developer workflow. Concrete example of a harness in the wild.

## Talk Design Terms

**Ponytail/Caveman** — Prompt engineering modes baked into the system prompt to enforce token discipline. Ponytail = lazy/minimal code style. Caveman = terse prose. Used as a live example of token-aware system prompt design.

**Sparse slides** — Presentation style: one big idea per slide, minimal text. Speaker carries the content; slide is a backdrop.
