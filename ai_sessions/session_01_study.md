# Session 01 — Study Guide
### Sequenced by slide. Read top to bottom. Talk the same way.

> One sentence everything hangs on: **An LLM does exactly one thing — predict the most probable next token. Everything else — reasoning, code, knowledge — is an emergent side effect of getting extremely good at that one task.**

---

## INTRO · Slides 1–6

---

### Slide 1 · Title

**What this session is**

Not a product demo. Not "AI will replace you." A serious attempt to explain what is actually happening under the hood — so the room can make informed decisions about how they work.

**How to open**

Don't read the slide. Look at the room and say something like:

> "We've been using AI tools for a couple of years now. Most of us have a complicated relationship with them. Today we're going to talk about why — and what changes when you go deeper."

Keep it under 60 seconds. Get to the speakers slide fast.

---

### Slide 2 · Speakers

**What to say**

Brief. Name, role, one honest sentence about your relationship with AI tools. Not a CV read.

Example:
> "I'm Sifat — senior engineer at C-Fat. I resisted this stuff for about a year, then something clicked. That's what we're here to talk about."
> "I'm Anik — frontend engineer. I was the person saying 'it's just autocomplete.' I changed my mind. Here's why."

Under 90 seconds total. They're not here for your biography.

---

### Slide 3 · "You've tried it. It was fine."

**Why this slide exists**

This is the room-check. You're naming the frustration out loud before anyone has to admit it. That builds trust immediately.

**What to do**

Ask the room directly:
- *"Who here has used ChatGPT to debug something in the last month?"* — most hands go up
- *"Who felt like it actually understood your codebase?"* — very few hands

Pause. Let the gap register.

> "That gap — between what you tried and what was possible — is what this session is about."

The experience they had (paste error → get answer → move on) is real and valid. The tool isn't broken. The workflow around it is. That's the reframe.

**What NOT to do**

Don't be condescending about how they've been using it. They're senior engineers. They know things didn't work. You're here to explain why, not to lecture.

---

### Slide 4 · Thesis

**The one idea that drives the whole program**

> "The engineers who understand this will outpace those who don't."

**How to land it**

Pause after the slide appears. Don't rush it. Let them read it.

Then:
> "This isn't about AI replacing you. It's about the same thing that happened with IDEs, with the web, with cloud. The engineers who went deep early had an edge. That window is open right now."

**Why "outpace" not "survive"**

The language is deliberately positive. "Survive" sounds threatening. "Outpace" sounds like opportunity. Same engineers, different speed — and the speed compounds over time.

**The real argument**

- An engineer who learns 20% faster compounds dramatically over 3 years
- The implementation bottleneck is shrinking — problem formulation and judgment are now proportionally more valuable
- Shallow use (autocomplete) gives you 5% of the benefit. Deep use (agents, context, harness) gives you 10x that.

---

### Slide 5 · Productivity Paradox — Coding Faster ≠ Shipping Faster

**The point**

Most engineers who adopt AI feel faster at the keyboard. PRs get written quicker. Autocomplete is genuinely useful. But delivery speed — features shipped, users impacted — barely moves. Why?

Because coding is not the bottleneck. The pipeline is:

```
PRD / Proto → Plan → Spec → Tests → Code → Review
```

AI is only being applied to one step: **Code**. The other five remain manual. According to the Theory of Constraints (Goldratt), optimising a non-bottleneck does not speed up the system. If Tests and Review are the constraint, making Code faster just creates a bigger queue in front of Review.

**The Goldratt quote on the slide**

> *"An hour lost at a bottleneck is an hour lost for the entire system."*

Eliyahu Goldratt wrote *The Goal* in 1984 about manufacturing. Every insight in it applies directly to software delivery. The bottleneck in most engineering teams is not writing code — it's:
- Unclear specs (leads to rewrites)
- Missing test coverage (bugs slip to production, slowing future delivery)
- Slow review cycles (PRs sit for days)

AI can help with all of these. But only if you apply it there.

**What to say**

> "You're probably already faster at writing code with AI. So why aren't you shipping twice as fast? Because code is one step in a pipeline. We're going to talk about what happens when you apply AI to every step — not just the one that already felt fast."

**What this slide sets up**

The next slide shows exactly what that looks like: the AI-native engineer pipeline vs. the typical engineer pipeline.

---

### Slide 6 · AI-Native Engineer — Most Focus Only on Code

**The two pipelines side by side**

| Step | Typical engineer | AI-native engineer |
|---|---|---|
| PRD / Proto | Manual | AI drafts scope, surfaces gaps early |
| Plan | Manual | AI explores approaches, spots risks |
| Spec | Manual | AI generates edge cases, contracts, ambiguity |
| Tests | Manual | AI generates test cases before code is written |
| Code | AI used here | AI implements with full context |
| Review | Manual | AI catches bugs, refactors, documents |

**Why each step compounds**

**PRD / Proto with AI:** A better spec means the engineer builds the right thing the first time. Every hour of bad spec costs 5–10x in rework. AI can draft scope documents, identify missing requirements, and surface contradictions before a line of code is written.

**Plan with AI:** AI can explore multiple implementation approaches in minutes — "what are 3 ways to architect this auth system, with tradeoffs?" A human might explore 1 approach in depth. This is where experienced engineers get the most leverage.

**Spec with AI:** Edge cases that would surface as bugs in production can be caught in the spec phase. AI is very good at generating edge cases: "what inputs would break this function?" "what race conditions exist in this design?"

**Tests with AI:** Writing tests *before* the code (TDD-style) with AI assistance means the code gets written to pass known tests. This changes the quality of the output dramatically compared to writing tests after.

**Code with AI:** This is where most people already are. With a good spec, good plan, and good tests already in place, the code step is faster *and* the output is better — because the AI has more context to work with.

**Review with AI:** AI can review PRs for correctness, security, style, and documentation before human review. This makes human review faster and catches issues that humans are prone to miss when fatigued.

**The compounding effect**

Better spec → fewer rewrites. Better plan → fewer dead ends. Better tests → fewer bugs. Better code → faster review. Each upstream improvement pays dividends downstream. The AI-native engineer isn't just "using AI more" — they've restructured how they work.

**What to say**

> "The typical engineer uses AI like a faster keyboard. The AI-native engineer uses AI as a thinking partner at every step. The difference in output quality is not 2x. It's an order of magnitude — because every upstream improvement compounds."

> "This program is about becoming the second type of engineer. Not just writing faster — thinking better, at every stage."

---

### Slide 7 · Roadmap — 8 Phases, 36 Sessions

**How to explain the program**

Don't read the phases. Show the map and say:

> "This is where we're going. 36 sessions, 8 phases. It's in beta — we'll adjust as we go based on what the room actually needs."

Point to Phase 1 (highlighted, today):
> "Today is Phase 1. Foundations. This is the most important phase — if you don't understand how LLMs work, everything else is cargo cult."

Briefly name what's ahead without detailing it:
> "Phase 2 is how to use AI in your actual day-to-day development. Phase 4 is building AI applications — embeddings, RAG, agents. Phase 6 is running AI in production safely. We go all the way."

**The "beta" caveat**

Say it genuinely, not defensively:
> "Beta means we'll reshape this based on what's useful for you. If a session goes deep on something you all already know, we skip ahead. If something needs more time, we take it."

**What the 8 phases cover**

| Phase | Focus |
|---|---|
| 1 | Mindset & Foundations — what LLMs are, how they work |
| 2 | AI-Powered Development — feature dev, debugging, testing, code review |
| 3 | AI-Powered Learning — DSA, system design, new tech, faster skill acquisition |
| 4 | Building AI Applications — APIs, embeddings, RAG, agents, tool calling |
| 5 | AI in Engineering Teams — requirements, planning, docs, incident management |
| 6 | Production AI Engineering — reliability, hallucination, evaluation, security |
| 7 | AI Leadership — culture, hiring, upskilling, career growth |
| 8 | Future Trends — agentic development, AI-native orgs, next 5 years |

---

### Slide 8 · Today's Agenda

**Set expectations, then stick to them**

Walk through the three blocks:

> "20 minutes on how LLMs actually work — not a surface overview, real mechanics. 15 minutes on what an agent harness is. 5 minutes of a glimpse of a real workflow. That's it for today."

**Why the time breakdown matters**

The LLM mechanics section is the longest because it's the foundation. Without it, everything else is just "cool tool" talk. If someone later asks "why does the model hallucinate?" or "why did it forget what I said earlier?" — the answer is always back here.

---

## STEP 1 · TOKENIZE · Slides 7–12

---

### Slide 9 · Open CLI — The Journey Begins

**What this slide does**

Anchors the whole session in something concrete. You're not starting with theory — you're starting with an action the audience has taken or could take today.

**What to say**

> "Let's follow what actually happens between this keystroke and the answer. Every step we're about to cover is a real step in the pipeline. By the end you'll know what each one does and why it matters."

This sets up the rest of the LLM section as a story, not a lecture.

---

### Slide 10 · Tokens Are the Currency of LLMs

**What is a token?**

A token is a subword chunk — not a word, not a character. A piece of text the model treats as a single unit. Roughly **1 token ≈ 0.75 words** in English. So 1,000 words ≈ 1,333 tokens.

**Why "currency"?**

Because currency has three properties tokens share:
1. **Value** — every token costs money (API pricing is per token)
2. **Budget** — there's a maximum you can spend (context window limit)
3. **Scarcity** — every token you spend on input is one fewer the model can use for thinking

Once you see tokens as currency, everything downstream makes sense: why short prompts are better, why context windows fill up, why switching models changes your bill.

**What to say**

> "Tokens are the unit of everything. Cost, memory, speed — all measured in tokens. By the end of this section you'll think in tokens."

---

### Slide 11 · Split — Text Becomes Chunks

**How tokenization works**

When you send text to an LLM, the first thing that happens is **tokenization** — the text is split into chunks using the model's vocabulary.

These chunks are **not words**:
- `"Why"` → 1 chunk
- `" is"` → 1 chunk (note the leading space — it's part of the token)
- `" null"` → 1 chunk
- `"?"` → 1 chunk

**How the vocabulary is built (Byte-Pair Encoding)**

You don't need to explain the full algorithm, but understand it:

1. Start with individual characters
2. Find the most common two-character pair in the training data — merge it into one token
3. Repeat until you have ~100k tokens

Result: common sequences get their own token. Rare or invented words get broken into small pieces. This is why `"function"` is 1 token (seen billions of times) but `"frabjous"` is 4 (Lewis Carroll made it up).

**What to say**

> "The model doesn't see words. It sees chunks. And those chunks were decided by what was most common in the training data."

---

### Slide 12 · Encode — Each Chunk Becomes a Number

**The key fact**

Every chunk gets looked up in a vocabulary table and replaced with an integer ID. From this point forward in the pipeline, **text does not exist**. The model only ever processes numbers.

- `"Why"` → `10445`
- `" is"` → `374`
- `" null"` → `1202`

These numbers are arbitrary — they're just indices into a lookup table. There's nothing meaningful about the number 1202. It just means "the chunk ' null' in this model's vocabulary."

**What to say**

> "Text is an illusion. By the time your message reaches the model, it's a list of integers. That's it. The model has never seen a letter in its life."

**Why this matters practically**

- The model can't "read" code the way you can. It sees token IDs.
- Whitespace, indentation, brackets — all tokenized separately, can behave unexpectedly
- If a word tokenizes into 10 pieces, the model has 10 separate "things" to track instead of 1

---

### Slide 13 · Vocabulary — Every Model Is Different

**Why vocabularies differ**

Each model is trained with its own tokenizer. The same sentence sent to Claude and GPT-4 produces different token counts because their vocabularies were built from different training runs with different merge priorities.

**Practical implications**

1. **Cost changes when you switch models** — even with identical prompts, different token counts → different bills
2. **Vocabulary size matters** — bigger vocabulary = model can represent larger chunks = fewer tokens for the same text = more efficient
   - GPT-2: ~50k tokens
   - GPT-4 / Claude: ~100k tokens
   - Gemini: ~256k tokens
3. **You can't assume token counts** — always measure with the specific model you're using

**What to say**

> "When you switch from GPT-4 to Claude, your token bill can change even if you didn't change a single word. This is why."

---

### Slide 14 · Common is Cheap, Rare is Expensive

**The pattern**

The vocabulary was built from training data. Tokens that appear frequently in that data get efficient (short) representations. Tokens that are rare get broken into many pieces.

| Text | Tokens | Why |
|---|---|---|
| `function` | 1 | Seen millions of times in JS/Python training data |
| `return` | 1 | Same |
| `frabjous` | 4: `fr` `aj` `b` `ous` | Lewis Carroll invented it |
| `src/components/UserDashboard` | ~8 | Long, specific path, breaks at natural boundaries |

**What this means for you**

- Popular languages (JavaScript, Python) tokenize more efficiently than obscure ones
- Your company's internal jargon likely breaks into many tokens
- Descriptive variable names (`getUserAuthenticationStatus`) cost more than short ones (`getAuthStatus`)
- This is a real engineering consideration at scale — not just academic

**What to say**

> "You're paying per token. Every time you use obscure terminology or long internal names, you're spending more budget. At scale, this adds up."

---

## STEP 2 · INTO THE LLM · Slides 13–18

---

### Slide 15 · What Is a Parameter?

**The core definition**

A parameter (also called a weight) is a single floating-point number stored inside the model. It's a number like `0.3721847` or `-1.2048392`.

**Scale**

- GPT-2 (2019): 1.5 billion parameters
- GPT-3 (2020): 175 billion parameters
- GPT-4 (estimated): ~1.8 trillion parameters
- Claude 3 (estimated): hundreds of billions to ~1 trillion

**What parameters do**

Parameters are the model's entire knowledge. Every fact, every grammar rule, every coding pattern, every language the model knows — all encoded in these numbers. Not stored as text. Not stored as a database. Encoded as numerical relationships between billions of values.

**The crucial point**

> Prompting never changes the parameters. They are fixed after training. When you prompt a model, you're providing context that activates different patterns in the fixed weights — but you're not teaching it anything permanently.

This is why the model doesn't "remember" you between sessions unless you re-provide the context. Nothing changed in the model. Your conversation lived only in the context window.

**Analogy**

The parameters are like the collective memory of everyone who ever wrote on the internet, mathematics textbooks, code repositories, and scientific papers — compressed into numbers over months of computation.

**What to say**

> "Those highlighted numbers on the slide — there are 1.8 trillion more of them in GPT-4. That's the model's entire brain. And your prompt doesn't change a single one."

---

### Slide 16 · Training — It Read the Internet

**The training process**

Pre-training is how the model gets its knowledge. Here's what happens:

**1. Collect the dataset**
Trillions of tokens from the internet: Common Crawl (web pages), Wikipedia, GitHub, books, papers, Reddit, Stack Overflow. For GPT-4 and Claude 3, estimated 10–15 trillion tokens.

**2. The training loop — one pass**
- Take a sequence of tokens from the dataset: `[10445, 374, 420, 1202, 30]`
- Feed the first N tokens into the model
- Ask it to predict token N+1
- Compare prediction to the real answer
- Measure the error (called **loss** — a single number representing how wrong it was)

**3. Backpropagation**
Work backwards through every layer of the network. For each parameter, calculate: "how much did this specific number contribute to the error, and which direction should I nudge it to reduce the error?"

Then nudge it. By a tiny amount — maybe changing `0.3721847` to `0.3721851`.

**4. Repeat — 10 trillion times**
Do this for every sequence in the training dataset. The parameters settle into positions that produce correct predictions across the entire dataset.

**Cost**
Training a frontier model requires thousands of H100 GPUs running for months. Electricity alone costs millions. Total training cost for GPT-4: estimated $100M+.

**What to say**

> "Backpropagation is just: measure how wrong you were, then nudge every number slightly in the direction that would have been less wrong. Do this 10 trillion times. That's the whole algorithm."

---

### Slide 17 · RLHF — Humans Rated Its Answers

**The problem pre-training creates**

After pre-training, the model can predict text — but it predicts text the way the internet writes it. Ask it "What is the capital of France?" and it might complete the prompt like a Wikipedia article instead of answering you directly. It doesn't know it's supposed to be a helpful assistant.

**RLHF fixes this in three steps**

**Step 1 — Supervised Fine-Tuning (SFT)**
Human contractors (thousands of them, contracted by OpenAI/Anthropic/etc.) write examples of ideal conversations:
```
User: What is the capital of France?
Assistant: The capital of France is Paris.
```
The model is trained on tens of thousands of these. Now it knows the format: user asks, assistant answers clearly.

**Step 2 — Reward Model**
Present the model with a prompt. Generate 4–8 different responses. Have humans rank them best to worst. Train a *separate* neural network (the reward model) to predict human preference scores. This becomes the proxy for "what humans consider a good response."

**Step 3 — Reinforcement Learning**
Run the LLM, score its outputs with the reward model, adjust the LLM's parameters to produce outputs that score higher. Repeat many times.

Result: the model is helpful, polite, honest, and safe — not because those properties were programmed, but because humans consistently rated those outputs higher.

**Why this matters**

- RLHF is why the model says "I don't know" sometimes — honest uncertainty scored higher than confident hallucination
- RLHF is why the model is sometimes overly cautious — safety scored high, and it over-generalised
- RLHF is why the system prompt works — operators wrote system prompts during fine-tuning, so the model learned to treat them as authoritative
- Different models feel different to use largely because of RLHF differences, not pre-training differences

**What to say**

> "Pre-training gives the model knowledge. RLHF gives it manners. And the manners are the whole reason you can actually use it."

---

### Slide 18 · Attention — Every Token Looks at Every Other Token

**The transformer's core mechanism**

The transformer processes all tokens simultaneously (in parallel, not one at a time). For each token, it asks: "which other tokens are most relevant to understanding what this token means in this context?"

**The "bank" example**

`"I deposited money at the bank"` — "bank" = financial institution
`"I sat by the river bank"` — "bank" = riverbank

Same token ID. Completely different meaning. The transformer uses attention to let "bank" look at "money" or "river" and update its internal representation accordingly.

**How attention works (simplified)**

For each token, the model computes three things:
- **Query (Q):** "What am I looking for?"
- **Key (K):** "What do I contain?"
- **Value (V):** "What do I contribute if you pay attention to me?"

The attention score between token A and token B = how well A's Query matches B's Key.

High score → B is very relevant → B's Value gets weighted heavily in A's representation.

**Multiple heads, multiple layers**

- GPT-4 (estimated): 96 attention heads per layer, 96 layers
- Each head specialises in different relationships: some track syntax, some track coreference ("it" = "the cat" from 3 sentences ago), some track factual associations
- Early layers: local syntax patterns. Later layers: semantics, reasoning, world knowledge

**Why this matters for prompting**

Attention is why context placement matters. Information at the beginning (system prompt) and end (most recent message) gets more reliable attention than information buried in the middle of a long context. Your instructions on page 3 of a long document may be effectively ignored.

**What to say**

> "Attention is how the model figures out that 'bank' next to 'money' means something completely different from 'bank' next to 'river.' It's not lookup — it's relationship-weighted math."

---

### Slide 19 · Emergent Behaviour — Nobody Programmed Reasoning

**What emergence means**

The researchers defined:
- The architecture (transformer)
- The training objective (predict the next token)
- The training data (the internet)

They did NOT program:
- Reasoning
- Code generation
- Translation
- Maths
- In-context learning (learning a task from examples in the prompt)

These appeared at scale. They were not present at 1B parameters. They emerged around 10B–100B parameters. Nobody fully understands why.

**Concrete examples of emergent capabilities**

| Capability | When it appeared |
|---|---|
| Basic reasoning | ~10B parameters |
| Chain-of-thought reasoning | ~100B parameters |
| Code generation | ~50B parameters |
| In-context learning | ~10B parameters |
| Arithmetic | ~50B parameters |

**What this means honestly**

The most capable AI systems in the world are built by people who cannot fully explain why they work. The architecture and training process are well-understood. The final model's specific capabilities are not entirely predictable before training. This is simultaneously why AI is powerful and why it's unpredictable.

**What to say**

> "Nobody wrote code for 'be able to reason.' It appeared. At scale. That's remarkable — and slightly unsettling. Even the people who built it don't fully understand what they made."

---

### Slide 20 · Probabilistic Engine — The Output Is a Distribution

**What the model actually outputs**

After all the attention and feedforward layers, the model produces one thing: **a probability distribution over every token in its vocabulary**.

Given `"This returns null …"`, the model assigns probabilities:
- `"because"` → 58%
- `"due"` → 24%
- `"since"` → 11%
- `"as"` → 7%
- (every other token in the vocabulary gets a tiny probability)

Then a token is **sampled** from this distribution. With default settings, the highest-probability token wins most of the time.

**Temperature**

Temperature controls how the sampling works:
- **Low temperature (0.1–0.3):** Almost always picks the highest-probability token. Deterministic, repetitive, but predictable. Good for code.
- **High temperature (0.8–1.2):** Samples more randomly from the distribution. Creative, surprising, sometimes incoherent. Good for brainstorming.
- **Temperature 0:** Fully deterministic. Always picks the top token. Exact same output every time.

**Why this matters**

- The model generates **one token at a time**, each time running the full network again with the new token appended
- That's why streaming works — you see tokens appear as they're generated
- That's why the model can't "take back" what it wrote — it committed to early tokens and now must follow the probability gradient of its own output
- That's why hallucination happens — sometimes the most probable next token is factually wrong, and the model doesn't know the difference

**What to say**

> "It's not thinking in sentences. It's betting on one word at a time. Every word you see is the result of that bet. Sometimes the bet is wrong and the model doesn't know it."

---

## STEP 3 · TOOL CALL & LOOP · Slide 19

---

### Slide 21 · Tool Call & Loop

**The difference between a model and an agent**

A raw API call: you send text → you get text back. One turn. No memory. No tools. No loop.

An agent: the model can call tools, and the loop runs until the task is complete.

**How tool calling works**

You (or the harness) declare available tools to the model:

```json
{
  "name": "read_file",
  "description": "Read the contents of a file",
  "input_schema": {
    "type": "object",
    "properties": {
      "path": { "type": "string" }
    }
  }
}
```

When the model needs to read a file, instead of generating prose, it outputs a structured **tool call**:
```json
{ "tool": "read_file", "path": "src/auth.ts" }
```

The harness intercepts this, actually reads the file, and injects the result back into the context. The model never reads the file — the harness does. The model just asked for it.

**The loop**

```
1. Inject context (system prompt + files + history)
2. Call the model
3. Model returns:
   a. Tool call → harness executes → append result → go to step 2
   b. Final answer → loop ends
```

A complex task might loop 10–30 times. A simple question returns immediately.

**Why a raw API call is not enough**

With just an API call:
- The model can't read your actual files
- It can't run your tests
- It can't search the web
- It has no memory of previous calls unless you re-send everything

With an agent loop:
- It can read any file, run any bash command, call any API
- It loops until the task is complete
- The harness manages all the state

**What to say**

> "A raw API call is a very smart autocomplete. The loop is what makes it an agent. That's the whole difference."

---

## STEP 4 · THINKING · Slide 20

---

### Slide 22 · Before Answering, It Thinks

**What "thinking" means technically**

Some models (Claude 3.7, o1, o3) generate **internal reasoning tokens** before producing a visible response. These tokens are generated, processed, and consumed by the model — but not shown to the user.

The model reasons through the problem in these hidden tokens, then produces the visible answer based on that reasoning.

**Why "think step by step" works**

Even in models without explicit extended thinking, adding "think step by step" to a prompt dramatically improves accuracy on complex tasks. Why?

During training, the model saw millions of examples where humans wrote out their reasoning:
```
"Let me think about this step by step.
First, the function signature shows...
Second, the call site expects...
Therefore, the bug is..."
```

These step-by-step reasoning sequences were statistically associated with *correct* answers in the training data. By prompting "think step by step," you're steering the model toward token sequences that precede correct answers.

It's not magic. It's pattern activation.

**What to say**

> "The hidden tokens aren't the model 'thinking' the way you think. It's generating reasoning text for itself to condition on. It's writing its way to the answer. And that works because correct answers in the training data were usually preceded by written reasoning."

---

## STEP 5 · CONTEXT · Slides 21–23

---

### Slide 23 · Context Window — Fixed Window, Everything Competes

**What the context window is**

Everything the model can see at the moment it generates the next token:
1. System prompt
2. All previous messages in the conversation
3. Tool call results
4. The model's own output so far

It has a hard upper limit measured in tokens.

**Current limits**

| Model | Context window |
|---|---|
| GPT-4o | 128k tokens |
| Claude 3.5 / 3.7 Sonnet | 200k tokens |
| Gemini 1.5 / 2.0 Pro | 1 million tokens |

**What happens when it fills**

The earliest tokens fall off the beginning, silently. The model doesn't get an error. It simply loses access to what fell off. This means:
- The original task description might disappear
- Early instructions might be forgotten
- A conversation from 10 minutes ago may no longer be visible

**The "lost in the middle" problem**

Research shows LLMs pay *less attention* to information in the middle of a long context. They're most reliable about the beginning (system prompt) and end (most recent message). Critical instructions buried in the middle of a 100k token context may be effectively ignored.

**What to say**

> "The model isn't forgetting. It never had access to what fell off. And even what's still technically in the window — if it's in the middle — the model might not be paying much attention to it."

---

### Slide 24 · Token Discipline — Every Token Is Taken from Thinking

**The shared budget**

The context window is shared between:
- System prompt (your instructions)
- Conversation history
- Tool call results (file contents, bash output, search results)
- The model's own generated output

Every token you spend on a bloated system prompt is one fewer token available for the model to reason with.

**Common waste**

| Source | Wasteful | Better |
|---|---|---|
| System prompt | 500 words of pleasantries and redundant instructions | 50 precise directives |
| File context | Include entire 2000-line file | Include only the 50 relevant lines |
| Conversation history | Full history from session start | Last 3–5 turns |
| Instructions | "Please try to be as helpful as possible" | "Be concise." |

**Why this affects quality, not just cost**

1. More input tokens → more diluted attention → model loses focus
2. Signal-to-noise ratio drops → model gets confused about what matters
3. Context fills faster → window limit hit sooner on long tasks
4. More tokens → slower time to first response

**What to say**

> "Every line of bloat in your system prompt is stealing attention from the actual task. This is engineering, not style."

---

### Slide 25 · Ponytail / Caveman — Engineer the Behaviour

**What these are**

Two prompt engineering modes baked into a system prompt. They enforce token discipline at the model level — so you don't have to think about it per-prompt.

**Ponytail Mode**

A "lazy senior developer" persona:
> *Write the minimum code that works. No scaffolding, no speculative abstractions. Stop at the first rung that holds. Every unnecessary line is debt.*

Effect: the model writes tighter code, doesn't add unrequested features, doesn't pad with comments, doesn't create abstractions "for later."

Token impact: shorter responses = fewer output tokens = lower cost = faster responses = more room in the window for the next turn.

**Caveman Mode**

A terse-prose persona:
> *Answer first, explain only if asked. No preamble, no padding, no defending your choices in prose.*

Effect: the model doesn't write "Great question! Let me help you with that..." before answering. It just answers.

Token impact: same as above. A response that skips 50 words of preamble saves ~65 tokens every call. At 10,000 calls/month, that's 650,000 tokens saved.

**The principle**

You can engineer the model's behaviour — its style, its verbosity, its coding habits — entirely through the system prompt. This is a real engineering discipline. A well-crafted system prompt is not "nice instructions." It's a control surface.

**What to say**

> "These aren't prompting tricks. They're engineering decisions baked into my harness. The model I work with is a different model from the default one — same weights, different operating mode."

---

## STEP 6 · OUTPUT · Slide 24

---

### Slide 26 · Output — Decoded Back to Text

**The final step**

The model outputs token IDs — integers, just like the input. The harness passes these through a **detokenizer** — the vocabulary lookup table in reverse — converting each ID back to its text chunk.

```
2028 → "The"
2523 → " issue"
374  → " is"
1202 → " null"
```

**One token at a time**

The model doesn't generate the full response and then send it. It generates **one token at a time**, each time running the full network again with the previous token appended to the context.

This is why:
- **Streaming works** — each token arrives as it's generated, you see it appear character by character
- **The model can't take back early words** — once "The issue is" is generated, those tokens are in the context. The model must now produce tokens that follow plausibly from what it already wrote.
- **Confident wrong answers happen** — if the first few tokens commit to an incorrect direction, the model follows that direction because it's now conditioning on its own wrong output

**What to say**

> "By the time you see the first word, the model has already committed to a direction. It can't backtrack. This is why you get confidently wrong answers — the model followed its own momentum."

---

## AGENT HARNESS · Slides 25–28

---

### Slide 27 · A Raw API Call Is Not an Agent

**What you get from a raw API call**

```
POST /v1/messages
→ { "content": "Here is the answer..." }
```

One shot. No memory of previous calls unless you re-send the full history. No tools. No loop. No access to your filesystem.

This is useful for simple Q&A. It is not an agent.

**What makes something an agent**

1. **A loop** that keeps running until the task is complete
2. **Tools** the model can call (read files, run code, search web)
3. **Context injection** — relevant information fed in before the loop starts
4. **Memory/state management** across turns

---

### Slide 28 · Harness — Loop + Context + Tools

**The four layers**

**System Prompt**
Where you control the model's behaviour. Persona, constraints, style, world model ("you're working in a TypeScript monorepo"). This is where ponytail and caveman live. A well-engineered system prompt is the single highest-leverage thing in the harness.

**Tool Definitions**
Declare what tools exist. The model decides when to call them. Common tools: `read_file`, `write_file`, `bash`, `web_search`, `list_directory`. The harness executes them; the model just requests them.

**Loop Logic**
Model runs → tool call → harness executes → result appended → model runs again. Repeats until the model produces a final answer (no tool call). Good loop logic handles: tool failures, infinite loops, dangerous commands, user confirmation prompts.

**Context Injection**
Before the loop starts, inject relevant information: current file, related files, recent git diff, docs, memory from previous sessions. A good harness is surgical — only include what's relevant. A naive harness dumps everything in and wastes the window.

---

### Slide 29 · Same Model, Different Harness

**Copilot — shallow harness**
- Context: current file + a few neighbours (~4–8k tokens)
- Tools: none (autocomplete only)
- Loop: no loop
- Use case: line-by-line autocomplete. Good at local patterns.

**Cursor — medium harness**
- Context: more of the repo via indexing
- Tools: file reads, some shell commands in Agent mode
- Loop: short loops in Agent mode
- Use case: feature implementation with some cross-file context

**pi / Claude Code — deep harness**
- Context: full repo, arbitrary file reads, web search
- Tools: full bash, file ops, web search, subagents, custom tools
- Loop: runs until task is complete
- System prompt: fully configurable
- Use case: complex multi-step tasks, architecture changes, debugging across many files

**The car analogy**

The model (Claude, GPT-4) is the engine. All four of these products can use the same engine. The harness is the car.

A go-kart with a Formula 1 engine goes 40mph. A Formula 1 car with the same engine goes 220mph. The difference is not the engine — it's what's around it.

---

### Slide 30 · A Good Harness Changes the Output Drastically

**The core insight**

Most engineers blame the model when output is bad. The model is usually fine. What's bad is:
- Not enough context (model answering from general knowledge instead of your codebase)
- No loop (model can't verify its own output by running tests)
- No tools (model can't read the actual file it's supposed to fix)
- Bloated system prompt (model's attention is scattered)

All of these are harness problems.

**Going deeper**

MCP, RAG, multi-agent systems — all covered in Phase 2 and Phase 4. Today you just need the concept: the quality of what's around the model matters as much as the model itself.

---

## WORKFLOW · Slides 29–30

---

### Slide 31 · My Stack

**tmux**
Terminal multiplexer. Persistent sessions that survive disconnects. The agent runs in one pane, the editor in another, tests in a third. Everything stays alive between tasks. Zero context switch to get to the AI.

**pi**
The agent CLI. This is the harness. Custom skills (reusable instructions for specific tasks), subagents (specialist agents for code review, testing, etc.), fast commands. The system prompt lives here — ponytail, caveman, and more.

**neovim**
Terminal-native editor. Integrates tightly with tmux. Opening a file, jumping to a line, reading output — all from the keyboard without leaving the terminal context.

**supermaven**
Inline autocomplete inside neovim. Very fast (~50ms latency). Trained on code. Stays out of the way — it suggests, you accept or ignore. Complements the agent loop; you're not reaching for a different tool.

**The point**

None of these tools is magic individually. The integration is the point. AI is never more than a keystroke away. There's no "let me open another window and paste this in." The friction is near zero.

**What to say**

> "We'll go deep on each of these in a later session. For now — notice that none of this is a special AI tool. It's a regular development environment where AI is woven in everywhere."

---

### Slide 32 · Close — AI as a Thinking Partner

**What "thinking partner" means**

The next session goes from mechanics to workflow. Not "how does it work" but "how do you actually collaborate with a model."

The difference:
- **Prompt + hope** — you write a request, you get output, you accept or reject it
- **Thinking partner** — you're in a loop with it, iterating, steering, disagreeing, asking follow-up questions, using its output as input to your own thinking

The second mode is dramatically more powerful and most engineers never reach it because they never went deep enough on the mechanics.

**Close line**

> "You now know what a token is, what a context window is, what a parameter is, what RLHF is, what an agent harness does. That's the foundation. Next session we use it."

---

## Glossary

| Term | Definition |
|---|---|
| **Token** | Subword chunk — the unit LLMs process. ~0.75 words on average in English. |
| **BPE** | Byte-Pair Encoding. Algorithm that builds token vocabularies by merging the most common character pairs. |
| **Vocabulary** | The complete set of tokens a model knows. Typically 100k–256k tokens. |
| **Parameter / Weight** | A single floating-point number inside the model. GPT-4: ~1.8 trillion of them. Frozen after training. |
| **Loss** | A number measuring how wrong a prediction was. Training = minimising loss across trillions of examples. |
| **Backpropagation** | The training algorithm. Measures prediction error, nudges every parameter slightly in the direction that reduces it. Repeated trillions of times. |
| **Pre-training** | Training the model on vast text data to predict the next token. Produces raw knowledge. |
| **SFT** | Supervised Fine-Tuning. First step of RLHF — training on human-written ideal Q&A examples. |
| **RLHF** | Reinforcement Learning from Human Feedback. Fine-tuning process that makes the model helpful, not just accurate. |
| **Reward model** | A separate neural network trained to predict human preference scores. Used as proxy for human judgment in RLHF. |
| **Context window** | The maximum number of tokens a model can see at once. The model's working memory. |
| **Attention** | The mechanism letting each token update its meaning based on all other tokens. Core of the transformer. |
| **Transformer** | The neural network architecture used by all major LLMs. Based on attention + feedforward layers. |
| **Embedding** | A high-dimensional vector representing a token. Where "meaning" lives in the model's internal space. |
| **Temperature** | Controls randomness of token sampling. Low = deterministic. High = creative/erratic. |
| **Hallucination** | Model generating plausible but incorrect information. Not a bug — the model is predicting probable tokens, and the most probable token happened to be wrong. |
| **Emergent behaviour** | Capabilities that appeared at scale without being explicitly programmed — reasoning, code generation, translation. |
| **System prompt** | Instructions prepended to every conversation that shape the model's behaviour. Authoritative due to RLHF. |
| **Harness** | Scaffolding around an LLM: system prompt + tool definitions + loop logic + context injection. |
| **Tool call** | A structured request from the model to execute a function. The harness executes it; the model just asks. |
| **Agent** | A model with a harness. Can call tools, run in a loop, complete multi-step tasks autonomously. |
| **Context injection** | Putting relevant information (files, docs, memory) into the context window before the loop starts. |
| **Compaction** | Truncating or summarising old context when the window fills. Keeps the loop running without hitting limits. |
| **RAG** | Retrieval-Augmented Generation. Using semantic search to inject relevant context dynamically. Session 9. |
| **Ponytail mode** | System prompt persona enforcing minimal, non-speculative code. Token-efficient. |
| **Caveman mode** | System prompt persona enforcing terse prose — answer first, no padding. Token-efficient. |
| **Autoregressive** | Generating one token at a time, feeding each output back as input for the next prediction. |

---

## What to watch next

- **3Blue1Brown — "But what is a GPT?"** — Visual deep dive into transformers, attention, embeddings. You've seen it. Rewatch the attention section with this guide open.
- **Andrej Karpathy — "Let's build GPT from scratch"** — 2-hour video. Builds a small GPT in Python. Best way to truly understand the architecture. Do this before Session 2.
- **Anthropic — "Building effective agents"** — Short official doc on agent design patterns. Read it.
- **OpenAI Tokenizer** — `platform.openai.com/tokenizer` — Paste any text, see exact tokens. Run your own prompts.

---

*AI-Native Software Engineer Program · Session 01 · Beta*
