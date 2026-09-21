# 🤖 Awesome Agent Personas

> A curated collection of **AI agent personas, SOUL.md files, persona distillation techniques, cognitive clones, character agents, and identity engineering**.

AI agents do not have to sound like the same generic assistant.

This list collects projects that explore how agents can develop or reproduce consistent:

- 🧠 ways of thinking
- 🎭 personalities
- 💬 communication styles
- 🧭 values and boundaries
- 🧬 decision patterns
- 🪞 cognitive perspectives
- 🧠 memory and identity
- 👥 roles inside multi-agent systems

The focus is on **interesting techniques and real implementations**, not giant dumps of generic “You are an expert...” prompts.

---

## 🧭 Contents

- [Start Here](#-start-here)
- [Highlighted Personas](#-highlighted-personas)
  - [Writers](#-writers)
  - [Directors](#-directors)
  - [Fictional Characters](#-fictional-characters)
  - [Multi-Persona Experiments](#-multi-persona-experiments)
- [What Is an Agent Persona?](#-what-is-an-agent-persona)
- [SOUL.md and Agent Identity](#-soulmd-and-agent-identity)
- [Persona Distillation](#-persona-distillation)
- [Character and Evolving Personas](#-character-and-evolving-personas)
- [Cognitive Clones](#-cognitive-clones)
- [Multi-Agent Personas](#-multi-agent-personas)
- [Chinese Agent Ecosystem](#-chinese-agent-ecosystem)
- [Specifications and Tooling](#-specifications-and-tooling)
- [Collections](#-collections)
- [Design Patterns](#-design-patterns)
- [Resources](#-resources)
- [Contributing](#-contributing)

---

## 🚀 Start Here

If you are new to agent personas, these three projects show very different approaches.

### 🧠 OpenClaw

A practical example of using `SOUL.md` as a persistent identity and personality layer.

**Why it is interesting:** it separates who the agent is from project instructions and individual tasks.

🔗 https://github.com/openclaw/openclaw

### 🧬 Nuwa Persona Distillation

A system for reconstructing **how a person thinks**, rather than simply copying their vocabulary.

It attempts to extract mental models, decision heuristics, values, communication patterns, behavioral boundaries, and recurring ways of reasoning.

**Key idea:** model the person's thinking process, not just things they have said.

🔗 https://github.com/alchaincyf/nuwa-skill

### 👥 DirectorAgents

Uses different personas as **cognitive perspectives inside a multi-agent system**.

Personas can debate, vote, review ideas, or approach the same problem using different mental models.

🔗 https://github.com/momozi1996/DirectorAgents

---


# 🌟 Highlighted Personas

Want to see the actual personas before reading about the frameworks? Start here.

These are concrete persona files and packs hidden inside some of the larger projects above.

## ✍️ Writers

| Persona | What is modeled | Direct link |
|---|---|---|
| **Liu Cixin** | Hard science fiction, civilization-scale thinking, scientific concepts turned into social conflict, and large-scale speculative reasoning. | [Open persona](https://github.com/momozi1996/awesome-ai-persona-skills/blob/main/Novelists/liucixin-skill/SKILL.md) |
| **Yu Hua** | Plain language around heavy themes, suffering, restrained warmth, folk perspective, and narrative repetition. | [Open persona](https://github.com/momozi1996/awesome-ai-persona-skills/blob/main/Novelists/yuhua-skill/SKILL.md) |
| **Mo Yan** | Magical realism, sensory-heavy narration, rural storytelling, multiple viewpoints, and historical layering. | [Open persona](https://github.com/momozi1996/awesome-ai-persona-skills/blob/main/Novelists/moyan-skill/SKILL.md) |
| **Eileen Chang** | Urban psychological realism, material detail, emotional distance, contrast, and melancholy. | [Open persona](https://github.com/momozi1996/awesome-ai-persona-skills/blob/main/Novelists/zhangailing-skill/SKILL.md) |

**Why this set is interesting:** these are not simple biography prompts. Each skill attempts to turn recurring creative choices into reusable writing and reasoning patterns.

## 🎬 Directors

| Persona | What is modeled | Direct link |
|---|---|---|
| **Christopher Nolan** | Nonlinear structure, high-concept storytelling, time, science, and philosophical framing. | [Open persona](https://github.com/momozi1996/DirectorAgents/blob/main/skills/christophernolan-perspective/SKILL.md) |
| **Quentin Tarantino** | Dialogue-driven scenes, genre collision, nonlinear storytelling, and heightened dramatic tension. | [Open persona](https://github.com/momozi1996/DirectorAgents/blob/main/skills/quentintarantino-perspective/SKILL.md) |
| **Hayao Miyazaki** | Hand-crafted visual thinking, childhood perspective, flight, nature, environmental themes, and emotional wonder. | [Open persona](https://github.com/momozi1996/DirectorAgents/blob/main/skills/hayaomiyazaki-perspective/SKILL.md) |
| **Ang Lee** | Cross-cultural storytelling, ethical tension, emotional restraint, and competing interpretations of the same event. | [Open persona](https://github.com/momozi1996/DirectorAgents/blob/main/skills/anglee-perspective/SKILL.md) |

The interesting part is not impersonation. These personas are used as **creative lenses** that can be combined in sequential chains, debates, voting, or expert panels.

## 🎭 Fictional Characters

The [Arknights Persona Distillation](https://github.com/JNGKZbird/Arknights-Persona-Distill) project is useful because every character is built from source material into structured persona packs with motivations, boundaries, behavior, speech, relationships, memories, and worldview.

| Persona | Why it is interesting | Direct link |
|---|---|---|
| **Amiya** | A leader persona with responsibility, empathy, internal conflict, and strong role boundaries. | [Open persona](https://github.com/JNGKZbird/Arknights-Persona-Distill/tree/main/amiya) |
| **Texas** | A restrained, quiet persona where consistency depends heavily on what the agent does *not* say. | [Open persona](https://github.com/JNGKZbird/Arknights-Persona-Distill/tree/main/texas-base) |
| **Lappland** | A deliberately unstable and intense character, useful for testing whether strong personalities remain coherent without becoming random. | [Open persona](https://github.com/JNGKZbird/Arknights-Persona-Distill/tree/main/lappland-base) |
| **Closure** | An engineer and hacker character with a strong professional role layered together with a distinctive personality. | [Open persona](https://github.com/JNGKZbird/Arknights-Persona-Distill/tree/main/closure) |
| **Theresa** | A leadership-focused persona built around history, relationships, political responsibility, and memory anchors. | [Open persona](https://github.com/JNGKZbird/Arknights-Persona-Distill/tree/main/theresa) |

The project also ships both **full** and **compact** persona bundles, which makes it useful for comparing how much identity survives prompt compression.

## 👥 Multi-Persona Experiments

Some of the most interesting examples are not single personas at all.

- **Texas vs. Lappland**: two-way roleplay packs model both the active persona and its relationship with the other character. [Open the pack](https://github.com/JNGKZbird/Arknights-Persona-Distill/tree/main/texas-lappland)
- **Lappland vs. Texas**: the same relationship with the roles reversed, useful for studying asymmetric perspective. [Open the pack](https://github.com/JNGKZbird/Arknights-Persona-Distill/tree/main/lappland-texas)
- **Two versions of Exusiai in one scene**: one agent response performs two versions of the same character while keeping them distinct. [Open the pack](https://github.com/JNGKZbird/Arknights-Persona-Distill/tree/main/exusiai-duo-doctor)
- **Director panel**: DirectorAgents can combine multiple creative personas into chains, debates, voting groups, and expert panels instead of using one personality at a time. [Explore DirectorAgents](https://github.com/momozi1996/DirectorAgents)

This is where personas start becoming an **agent architecture primitive**, rather than just a roleplay feature.

---

# 🧠 What Is an Agent Persona?

An agent persona is more than a role prompt.

A simple role prompt might say:

```text
You are a senior software engineer.
```

A deeper persona may instead define:

```text
Identity
Values
Decision heuristics
Communication style
Boundaries
Preferences
Behavior under uncertainty
Relationships
Memory
Typical failure modes
Ways of disagreeing
```

The goal is usually **behavioral consistency across many interactions**.

---

## 📖 Quick Glossary

| Term | Meaning |
|---|---|
| **Agent Persona** | A persistent behavioral identity for an AI agent. |
| **SOUL.md** | A file used by some agent systems to describe identity, personality, values, and behavior. |
| **Persona Distillation** | Extracting a usable persona from writings, conversations, behavior, media, or other evidence. |
| **Cognitive Clone** | An agent designed to reproduce another person's decision patterns or reasoning style. |
| **Character Distillation** | Reconstructing a fictional character as a consistent interactive agent. |
| **Persona Drift** | When an agent gradually loses its intended personality during a long interaction. |
| **Identity Layer** | Persistent instructions describing who an agent is, separate from the task it is currently performing. |
| **Multi-Agent Persona** | Using different personalities or cognitive styles as specialized agents in a larger system. |

---

# 🧠 SOUL.md and Agent Identity

## OpenClaw

One of the clearest real-world examples of `SOUL.md`.

The soul layer can describe personality, principles, communication style, boundaries, and behavioral preferences.

**Interesting because:**

- identity is separated from task instructions
- personality persists across tasks
- the agent can have opinions and preferences
- boundaries are explicit
- behavior is more specific than a generic system prompt

🔗 https://github.com/openclaw/openclaw

---

## Hermes Agent

An agent framework from Nous Research with a layered approach to personality.

It distinguishes persistent identity from project instructions and temporary personality customization.

A useful way to think about the architecture:

```text
Persistent personality
        +
Project instructions
        +
Current task
        +
Temporary context
```

🔗 https://github.com/NousResearch/hermes-agent

---

## Aeon Soul

Explores separating an agent into persistent layers such as:

- soul
- style
- memory

This makes personality easier to reason about than putting every behavior into one giant system prompt.

🔗 https://github.com/aeonfun/soul.md

---

## Twynzen Soul MD

A research-oriented exploration of persistent agent identity.

Topics include:

- persona drift
- identity re-anchoring
- behavioral examples
- authority boundaries
- persistent character
- agent identity design

🔗 https://github.com/Twynzen/soul-md

---

## Robin Bril Soul MD

A compact personality designed around software engineering work.

Notable themes include:

- proactive behavior
- verification
- pushback
- independent judgment
- avoiding automatic agreement
- concise communication

A useful example of achieving personality without a massive prompt.

🔗 https://github.com/robinbril/soul-md

---

# 🧬 Persona Distillation

Persona distillation attempts to reconstruct a personality from evidence.

Instead of writing:

```text
You are confident, clever and direct.
```

a distillation system might ask:

```text
How does this person make decisions?
What do they prioritize?
What do they consistently reject?
How do they behave when information is incomplete?
What mental shortcuts do they use?
How do they communicate disagreement?
```

---

## 🧬 Nuwa Persona Distillation

A particularly interesting personality-distillation project.

The original project name references **Nuwa**, a creator figure from Chinese mythology. Here we use an English description so newcomers do not need cultural context to understand the project.

The system attempts to create an executable model of a person's:

- cognition
- mental models
- decision heuristics
- expression patterns
- values
- boundaries
- recurring behaviors

The important distinction is between reproducing **what somebody said** and reconstructing **how they tend to think**.

🔗 https://github.com/alchaincyf/nuwa-skill

---

## 🌌 God Skill

A deeper personality-reconstruction workflow.

It explores multiple dimensions of a person, including:

- cognition
- values
- influences
- decision patterns
- communication style
- motivations
- blind spots
- recurring themes
- personal boundaries

It is interesting as an example of **multi-dimensional personality modeling** rather than simple role prompting.

🔗 https://github.com/fattly/god-skill

---

## 🧑 Human Distillation Skills

A collection exploring how different human relationships and identities can be represented as agents.

Examples include conceptual personas based on:

- colleagues
- managers
- mentors
- relationships
- personal identity
- digital identity

It also explores the opposite problem: deciding which parts of a person's knowledge or identity **should not** be distilled into an agent.

🔗 https://github.com/misshiding/human-distillation-skills

---

## 🧠 DistillAI

Explores creating persistent personas from personal information such as:

- chat history
- documents
- voice
- recurring phrases
- behavior
- memories

Especially interesting because personality and long-term memory are treated as connected problems.

🔗 https://github.com/6ss6com/distill-ai

---

# 🎭 Character and Evolving Personas

Fictional characters are surprisingly useful research targets.

Unlike a vague human personality description, fictional characters often have large amounts of source material and relatively well-defined behavioral patterns.

This makes them useful for experimenting with persona consistency.

---

## 🎭 Arknights Persona Distillation

A systematic character-distillation methodology based on characters from the game **Arknights**.

You do not need to know the game to understand the technique.

The persona is decomposed into dimensions such as:

- internal motivations
- values
- personal boundaries
- behavioral modes
- speech patterns
- relationships
- important life events
- worldview

It also pays attention to **evidence quality**, separating strongly supported character traits from uncertain assumptions.

🔗 https://github.com/JNGKZbird/Arknights-Persona-Distill

---

## 🧬 ACGN Character Skill

A large methodology for reconstructing fictional characters from source material.

**ACGN** is an East Asian umbrella term for animation, comics, games, and novels.

The project is especially interesting because personas are designed to **evolve when new information becomes available**.

This moves personality from:

```text
static prompt
```

toward:

```text
identity model
+
new evidence
+
controlled evolution
```

🔗 https://github.com/AusertDream/ACGN-character-skill

---

# 🪞 Cognitive Clones

A cognitive clone attempts to reproduce someone's **reasoning style and decision process**, not merely their tone of voice.

A useful distinction:

```text
Voice clone
"What would this person sound like?"

Persona
"How would this person behave?"

Cognitive clone
"How would this person think about this problem?"
```

Projects such as **Nuwa Persona Distillation**, **God Skill**, and **DistillAI** overlap strongly with this area.

---

# 👥 Multi-Agent Personas

Personality can also be used as an engineering tool.

Instead of creating characters for roleplay, different personas can provide genuinely different approaches to a problem.

---

## 🎬 DirectorAgents

A collection of director-inspired cognitive personas.

Agents can participate in workflows such as:

- sequential analysis
- expert panels
- debate
- voting
- critique
- alternative interpretations

This demonstrates an important idea:

> A persona can be a cognitive lens, not just a character.

🔗 https://github.com/momozi1996/DirectorAgents

---

## 🌐 Tianya Community Personas

Personas based on notable writers from **Tianya Club**, a historically influential Chinese online discussion community.

The project combines different intellectual perspectives into multi-agent workflows.

Interesting as an example of turning a community's diverse viewpoints into a set of reusable reasoning agents.

🔗 https://github.com/momozi1996/tianya-skills

---

# 🌏 Chinese Agent Ecosystem

A significant amount of experimentation with AI personas is happening in the Chinese developer ecosystem.

Several recurring concepts appear across these projects.

For accessibility, this repository uses **English terminology throughout**, while preserving links to the original projects.

### 🧬 Personality Distillation

Reconstructing a person's behavioral and cognitive patterns from evidence.

### 🪞 Digital Double

Creating an AI representation of a particular person.

### 🌱 Digital Life

Treating an agent as a persistent identity that accumulates memory and develops over time.

### 🎭 Character Distillation

Reconstructing a fictional character from source material.

### 🧠 Agent Personality

Designing stable behavioral characteristics that remain consistent across tasks.

### 🏗️ Building a Person

An informal concept used by some communities for constructing a detailed artificial identity rather than writing a simple system prompt.

A recurring architecture looks roughly like:

```text
Values
  +
Cognition
  +
Decision heuristics
  +
Communication
  +
Memory
  +
Relationships
  +
Boundaries
  =
Persistent Agent Identity
```

---

# 🧰 Specifications and Tooling

## Soul Spec

Attempts to formalize soul files using structured metadata, schemas, validation, and developer tooling.

Useful for thinking about whether agent identity files could become machine-readable rather than being purely free-form Markdown.

🔗 https://github.com/AntonioTF5/soul-spec

---

## Soul.md Open Convention

An attempt to establish a reusable convention around describing:

- character
- values
- communication style
- identity
- behavioral boundaries

🔗 https://github.com/totalmarkdown/soul.md

---

# 📚 Collections

## Awesome AI Persona Skills

A large collection of persona and personality-distillation projects.

It includes:

- historical figures
- writers
- fictional characters
- professional roles
- emotional agents
- internet personalities
- multi-agent teams
- personality-distillation experiments

One of the best places to continue exploring the broader ecosystem.

🔗 https://github.com/momozi1996/awesome-ai-persona-skills

---

## Awesome Agent Souls

A collection focused more directly on agent soul files.

🔗 https://github.com/opena2a-standards/awesome-agent-souls

---

## Awesome Soul Files

Another collection of reusable soul and identity files.

🔗 https://github.com/AntonioTF5/awesome-soul-files

---

# 💡 Design Patterns

Several ideas repeatedly appear across the projects in this list.

## 1. 🧠 Identity is not the same as instructions

A useful separation is:

```text
SOUL.md
Who am I?

AGENTS.md
How do I work in this project?

SKILL.md
What specialized capability do I have?

Task
What should I do right now?
```

Mixing all four together makes an agent harder to understand and maintain.

---

## 2. 🧬 Distill cognition, not vocabulary

Weak personas copy phrases, slang, tone, and catchphrases.

Strong personas attempt to model priorities, trade-offs, decision heuristics, beliefs, uncertainty handling, and recurring reasoning patterns.

---

## 3. 🚧 Give personas boundaries

A personality becomes more convincing when it defines things the agent disagrees with, challenges, refuses, questions, or considers outside its expertise.

A persona that agrees with everything eventually collapses into generic assistant behavior.

---

## 4. 💬 Examples are powerful identity anchors

Instead of writing:

```text
Be direct.
```

show representative behavior:

```text
User:
Can we skip the tests? It is only a small change.

Agent:
No. The change is small, but the affected behavior is not obvious.
Run the focused test first.
```

Examples make abstract personality rules concrete.

---

## 5. 🧭 Preserve independent judgment

Useful personas should not automatically mirror the user.

They should be able to challenge assumptions, surface uncertainty, suggest alternatives, explain disagreement, and change their mind when evidence changes.

---

## 6. 🌱 Identity can evolve

A persona does not necessarily have to remain frozen forever.

A more advanced model might separate:

```text
Core identity
Stable

Preferences
Slowly changing

Relationships
Evolving

Memory
Continuously changing

Current mood or context
Temporary
```

---

## 7. 👥 Personas can be cognitive tools

Different identities can provide different ways of reasoning about the same problem.

For example:

```text
Builder
How can we make this work?

Reviewer
How can this fail?

Operator
What happens in production?

User
Is this actually understandable?

Security specialist
How could this be abused?
```

The value comes from **different cognitive perspectives**, not theatrical roleplay.

---

## 8. 🧪 Persona quality should be evaluated

Interesting evaluation questions include:

- Does the persona remain consistent across long conversations?
- Does it survive context compaction?
- Does it preserve preferences across different tasks?
- Does it disagree when expected?
- Does it become generic over time?
- Can users distinguish two personas in blind tests?
- Does additional memory improve or damage identity?
- How much identity survives a model change?

This is still an open research area.

---

# 🏷️ Suggested Categories

`SOUL.md` · `identity` · `persona-distillation` · `cognitive-clone` · `character` · `evolving-persona` · `memory` · `multi-agent` · `evaluation` · `research` · `tooling` · `production`

---

# ✅ What Belongs Here?

Good additions should introduce an interesting idea related to:

- AI agent personality
- persistent identity
- SOUL.md
- persona distillation
- cognitive cloning
- character reconstruction
- personality consistency
- behavioral boundaries
- persona drift
- memory and identity
- multi-agent perspectives
- persona evaluation
- evolving agent identities

---

# ❌ What Does Not Belong Here?

This repository intentionally avoids:

- huge generic prompt dumps
- thousands of automatically generated personas
- thin “You are an expert in X” prompts
- duplicated collections
- prompt spam
- projects with no meaningful personality or identity component

**Quality is more important than quantity.**

---

# 📚 Resources

- 🤝 [Contribution Guidelines](CONTRIBUTING.md) — what belongs in the list and how to submit it.
- 🧾 [Pull Request Template](.github/PULL_REQUEST_TEMPLATE.md) — checklist for new entries.
- 💬 [Issues](https://github.com/artttj/awesome-agent-personas/issues) — suggest a persona, report a broken link, or discuss the list.
- 🌟 [Awesome Manifesto](https://github.com/sindresorhus/awesome/blob/main/awesome.md) — background on the broader awesome-list convention.

---

# 🤝 Contributing

Please read the [Contribution Guidelines](CONTRIBUTING.md) before opening a pull request.

Found something unusual?

Pull requests are welcome.

Especially interesting:

- 🧠 original `SOUL.md` implementations
- 🧬 persona-distillation systems
- 🌏 projects from non-English developer communities
- 📚 academic research
- 🧪 persona-evaluation techniques
- 🪞 cognitive clones
- 🌱 evolving personalities
- 👥 multi-agent persona systems
- 💥 experiments that failed and explain why

For non-English projects, please provide an **English title and English explanation** so the collection remains accessible to everyone.

---

## ⭐ Philosophy

The interesting question is not:

> How do we make an AI pretend to be someone?

It is:

> **How do we give an agent a coherent way of thinking and behaving that remains recognizable over time?**

That is what this list is about.
