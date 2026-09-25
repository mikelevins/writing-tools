# The outline and the derivation of beats

How the story's skeleton is written, keyed, kept in sync, and derived beat by beat. Entry format is described in `../README.md`.

---

### The two-layer outline

**What.** The outline is split into a writer's document (action only) and an auxiliary layer (everything else), joined by identical heading lines.

**When.** Any project that drafts from an outline.

**How.** `outline.md` holds every beat in story order, headed

```
## <event>/<beat> <slug> — <what happens> [status]
```

followed by one paragraph of what happens and nothing else: no derivations, dates, provenance, or cross-references. The author drafts from this. `notes/` holds one file per event, each beat's section headed with the same line minus the event prefix (`## 2 grail-interview — ...`), carrying derivation, canon and provenance, genre and fun notes, reread payoffs, seams to neighboring beats, and open decisions. A long event may span several notes files (`02`, `02.3`, `02.6`). Non-beat sections in a notes file use a heading without a leading digit. The heading line itself is a compressed summary of the beat's contents (its quoted lines, its turns), which is what makes `grep -n '^## ' outline.md` a usable table of contents.

**Origin.** Kestrel Book 4, ratified August 28 2026.

**Scope.** General.

**See also.** *Drift control*, *Dewey coordinates*, below.

---

### Dewey coordinates

**What.** Events and beats carry decimal keys read as values, not counts. A key is assigned once and never renumbered.

**When.** Any outline that will be reorganized, which is every outline.

**How.** A new event or beat at the end takes the next integer. An insertion takes the shortest midpoint between its neighbors (`12.5`, then `12.25` or `12.75`; a batch gets spread). Ugly keys like `12.515` are acceptable. No trailing zeros; the integer part is zero-padded to two digits in filenames only. A beat's global coordinate is `event/beat` (`04/2 grail-interview`); the slug is its name and never changes. Physical order is story order, and keys should agree with it: reordering means moving the block and giving it a new key between its new neighbors. A beat that crosses events takes the new event's prefix, the one case a key changes. Files claim events, never chapters.

**Origin.** Kestrel Book 4, August 28 2026, replacing letter-coded beat IDs.

**Scope.** General.

---

### Status vocabulary

**What.** A bracketed status in every beat heading, with an optional second bracket for prose progress.

**When.** Every beat.

**How.** `[stub]` (triage cargo only) → `[rostered]` (named, geometry-tested, not yet derived) → `[derived]` (full spec) → `[ratified]` (author signed off). Prose progress is a second bracket: `[drafted]`, `[revised]`. A beat whose ending can carry a chapter break is marked *curtain-grade* in the heading. The first `[stub]` or `[rostered]` heading in the outline is the beat frontier. Chapter boundaries themselves emerge from the prose; specs never assert them.

**Origin.** Kestrel Book 4, August 28 2026.

**Scope.** General.

---

### Drift control

**What.** Any change to a beat is made in the outline first and in the notes file in the same sitting; a one-line check confirms the two layers agree.

**When.** At the close of every session and after any reorganization.

**How.** The sync check prints nothing when the layers are in sync:

```
diff <(grep -E '^## [0-9]' outline.md | sed -E 's|^## [0-9.]+/|## |') \
     <(for f in notes/[0-9]*.md; do grep -E '^## [0-9]' "$f"; done)
```

Navigation: `grep -n '^## ' outline.md` is the table of contents; `ls notes/` orders the notes files. (On a machine whose `grep` is ugrep, multi-file results print out of order; loop per file.)

**Origin.** Kestrel Book 4, August 28 2026.

**Scope.** General.

---

### Beat paragraphs are compressions, not stage directions

**What.** A beat paragraph says what happens and what the beat must teach. It is a compression of the narrative, not an instruction to the prose.

**When.** Writing beats; reviewing prose against beats.

**How.** Staging, tone, and count prescriptions ("gripes the whole way across", "one beat", "optionally", "on the page") are stripped from outline paragraphs. The prose is not bound by a summary's staging. Prose feedback checks what a beat must carry (canon facts, setups later beats need, the beat's *freight*) and not how the summary staged it. For drafted beats, reason from the manuscript, not the outline, and re-sync the outline to the prose when rulings land; the outline paragraph may then say "(as drafted; the prose supersedes)".

**Origin.** Kestrel Book 4, August 30 2026 (the author's call while drafting the first beat).

**Scope.** General.

---

### Plain language, no shorthand

**What.** Every outline heading and beat paragraph is readable by someone holding only the outline.

**When.** Writing a beat in; revising one; summarizing beats to the author.

**How.** No coined labels, planning shorthand, abbreviations, or references that need the notes file or the conversation to decode. Name things plainly, and explain a setting term (a part of a ship, an institution, a device) the first time it appears. Before a beat is written in, reread its heading and paragraph as a stranger would and strip every piece of shorthand; that reread is part of closing the beat. Examples caught in practice: *the watch* (for how the guard was posted), *the wall* (for the display showing a caller), *the door* (for the offer to leave), *the feed* (for the flow of instructions), *Team Yaug* (for a character's loyalty). Shorthand slows the work and buys nothing. The moment trove's writing rule is the same standard applied to its entries.

**Origin.** Kestrel Book 4, September 25 2026. The author had to stop and ask what an outline line meant.

**Scope.** General.

---

### The event format

**What.** Each event in an act file is a compressed narrative summary in running prose, followed by a fixed set of tracking bullets.

**When.** Projects that outline at event granularity rather than beat granularity (Reptile House). The two-layer outline is the beat-granularity successor; the tracking bullets transfer to either.

**How.** The summary runs a few hundred words: the shape of the scene, key moments, dialogue fragments, how it ends. Then the bullets, one per axis the book tracks. Reptile House Book 1 tracks five: **Motivation** (why each person does what they do), **Plot** (what the event sets up, pays off, and hands to the next event), **Funny**, **Creepy**, and **Membrane** (the book's thesis axis: how far the strangeness has come and where it now lives). The general form: Motivation, Plot, then the registers of the rubric the book cares to track per event (see `../craft/rubric.md`; Funny and Creepy are its comedy and creepy registers), then the book's own thesis axis, stated as a question every event has to answer. Kestrel's equivalent per beat is the derivation bundle (below), with Western and fun notes in place of the register bullets.

**Origin.** Reptile House, early 2026.

**Scope.** General; the specific bullets are per book.

---

### Beat drafts stay in the summary register

**What.** Event and beat drafts are not prose. Final prose is the author's domain.

**When.** Whenever the workshop partner drafts a beat.

**How.** If the draft has paragraph-level sensory detail, extended dialogue, or polished voice, it has drifted into prose; pull back to summary. The workshop partner delivers beat specs, catechisms, and modification lists; the author writes the sentences.

**Origin.** Reptile House, March 2026; restated in Kestrel as a method ruling.

**Scope.** General to this collaboration.

---

### The pipeline

**What.** Act files (or the outline) go directly to prose. There is no intermediate synopsis step.

**When.** Always. A synopsis step was tried and retired.

**How.** The outline paragraph is the last planning artifact before the sentence. **Order of work (Kestrel, September 10 2026):** prose needs beats to guide it; beats need a completed moment-trove audit, because blessed moments put beats out of date; so the trove is audited to completion first, then every beat is written start to finish, then the beats are audited for continuity and against the rubric, and only when all work those stages occasion is done does the prose begin. When a beat is large (a conference with a dozen turns), a chapter drafting outline can be written as a notes file: the beat's internal turns, action only, in order. That is still summary, not synopsis.

**Origin.** Reptile House (the synopsis workflow retired to the attic, 2026); the chapter drafting outline from Kestrel, September 6 2026.

**Scope.** General.

---

### Triage before rebuilding

**What.** Before a skeleton is rebuilt, every event in the prior skeleton gets a verdict and a spec stated in the constitution's terms.

**When.** A reset, a rebuild, or an inherited outline.

**How.** Verdicts: **keep** (re-derives cleanly), **re-derive** (the function is load-bearing, the form is inherited), **expend** (the function is reassigned or retired). Each verdict comes with the event's function stated in the constitution's terms, so every event knows why it is there. Mark *pivot plants*: opportunities that serve the ending's requirement. A verdict can be reopened by later derivation; record the reopening and the reason. A vignette survives triage only if it can name the character-geometry entry it serves and the later work it grounds.

**Origin.** Kestrel Book 4, August 24 2026.

**Scope.** General.

---

### Motivation first

**What.** Cast a scene by asking what each person wants and why they would be in the room. Character motivation drives plot mechanics, never the reverse.

**When.** Every derivation; every cast ruling.

**How.** A moment that cannot be justified in mechanical or motivational terms is a defect, disqualified unless it can be rebuilt. Every event is driven by a character's motivated choice or by dominoes knocked over by earlier motivated choices. The protagonist drives; they do not receive exposition passively. When a question comes up, propose the whole sequence that best serves the story, not an isolated decision.

**Origin.** Both projects. Reptile House states it as two principles (Active Protagonist; Character Knowledge Constrains Behavior). Kestrel applies it as the gate on every moment and cast ruling.

**Scope.** General.

---

### The derivation bundle

**What.** What a fully derived beat carries, and where.

**When.** Every beat taken from `[rostered]` to `[derived]`.

**How.** In the outline: the action paragraph. In the notes file: a per-actor catechism (what each wants, knows, and does); genre and fun notes (where the beat's fun lives; which genre overtone is allowed); reread payoffs; curtain-grade marks; seams to neighboring beats (what this beat must hand forward and receive); open decisions. Flip the status in both headings. Fixed seams between beats are stated in the handoff's next-work block so derivation order respects them.

**Origin.** Kestrel Book 4, August 2026.

**Scope.** General.

---

### Narrator tracking and the presence audit

**What.** Every beat states where the point-of-view character is and how they witness the beat. A beat that narrates something the narrator cannot see is a defect.

**When.** Every derivation; a full audit after any reconstruction and at the close of any session that changed beats.

**How.** The audit is a table over every beat with a verdict: `OK`; `OK-IF` (works only if the prose stages the narrator there; add them to the beat); `OFFSTAGE` (the narrator cannot see it; must become inference, later report, retrospective narration, or be cut); `CONTRADICTION` (the beat places someone where the story has already put them elsewhere). The audit begins by fixing the narrator's whereabouts through the whole book from the beats. One staging decision often resolves several findings at once (Kestrel's ride-along resolved five). Reconstructions trigger further audits; that loop is the method, not a failure of it. The audit is the companion to the sync check.

**Origin.** Kestrel Book 4, September 7 2026, after the moment trove turned up a beat that put the narrator on a train the story had already taken him off.

**Scope.** General for any fixed-POV book.

---

### Fair play for knowledge

**What.** Any "how did she know that" must trace to an act done in the open or a person who told her.

**When.** Every beat in which a character acts on information.

**How.** Work out the mechanism before using the knowledge. If the world's rules make the mechanism impossible (private channels, identification systems, no eavesdropping), the moment is disqualified unless it can be rebuilt on a lawful mechanism. Track what each character knows in every scene; a character acts on what they know, not on what the reader knows or what would be convenient. A knowledge map (who knows what, as of which event) is the instrument when the cast is large or the secret is structural.

**Origin.** Reptile House (Character Knowledge Constrains Behavior, March 2026; universe topology as the knowledge map for Book 1); Kestrel (the mechanism test, September 2026).

**Scope.** General.

---

### Ground nonhuman behavior in real-world references

**What.** When a nonhuman character's behavior is specified, the specification cites a real-world ethology or practice, not the fiction's own prior inventions.

**When.** Any nonhuman, uplifted, or constructed character with a body.

**How.** Name the source in the notes (the dog dominance ethogram; calming signals; a named study). Improvise only where the fiction exceeds what the real world can show, and say in the notes where that line is.

**Origin.** Kestrel Book 4, September 9 2026 (the Canine greeting).

**Scope.** Fiction.

---

### The rhythm of a sequence is named

**What.** A multi-beat sequence is designed to a stated rhythm, written at the top of its notes file.

**When.** Openings especially; any sequence that has to land a specific feeling.

**How.** State the rhythm as a sequence of registers (Kestrel's opening: easygoing warmth → BAM → frantic chase → WHAM → deadpan anticlimax, "the deadpan closes the ring with the problem inside it"). Each beat then knows which register it serves and the sequence can be checked against the rhythm when prose arrives.

**Origin.** Kestrel Book 4, August 25 2026.

**Scope.** General.

---

### Cutting a beat means closing its freight

**What.** When a beat is cut, the cut is not finished until **everything parked on that beat has been re-homed or closed.** A cut beat leaves orphaned freight — plants, payoffs, lines held for it, "available at X" notes elsewhere in the notes — pointing at a coordinate that no longer exists.

**When.** Every time a beat is cut, folded, or retired. Immediately, in the same sitting.

**How.** Before the cut is logged, grep the live tree for the beat's key and walk every hit. Each one gets one of three dispositions, written down where it sits:

- **Re-homed** — it moves to a live beat, and that beat's notes say so.
- **Delivered** — some other scene already pays it; say which, and close it.
- **Dropped** — a deliberate loss, with the reason, so it is chosen rather than mislaid.

Then record the cut itself in the owning notes file, as the project already does. **The check is mechanical and takes a minute:** `grep -rn "<key>" --include=*.md .` over the live tree (excluding the attic, which is the historical record and keeps the old pointers on purpose).

**Why it matters more than it looks.** Orphaned freight does not sit inert; it **actively misinforms**. A pointer at a dead beat reads as live design to anyone — author or collaborator — who meets it later, and it will be built on. **The worked case:** Kestrel Book 4's `02/1 polite-man-at-hatch` was cut on 9/6 and correctly logged as cut in its own notes file — but a neighbouring file still parked two pieces of live freight there ("available at `02/1`, where the same demand is made courteously"). Six days later that orphan was read as current and produced a confidently wrong statement in a chapter plan — a scene premise built on a beat that had not existed for a week. It was caught only because the author knew the book. The freight itself turned out to have been **delivered** in a different chapter entirely, so the correct disposition cost one line; the cost of not doing it was a wrong plan and an argument.

**Related failure, same root:** a **spec that the prose has superseded** is orphaned freight of another kind. When prose supersedes a beat, the beat's instructions want retiring in the same sitting, or a later pass reads them as outstanding.

**Origin.** Kestrel Book 4, September 2026 — three stale pointers in one week (`02/1`'s freight; a heading still carrying a retired mechanism at `02/2.5`; a superseded instruction to cut a portrait that the entry-portrait ruling had already overridden).

**Scope.** General.

**See also.** *Drift control (the sync check)*, above; *Decisions are folded in as they are made*, `project-layout.md`; *Prose supersedes beats*.

---

### The viewer pass

**What.** Once a beat set is complete, it is watched as a season of prestige television by a viewer who does not know the story, and assessed episode by episode: what pulls the viewer to the next hour, where it drags, what a first-time viewer cannot follow, and where the rubric can be raised. Then the findings are applied and the pass is rerun, until nothing structural remains.

**When.** After the outline is complete and every proposal is ruled; before the prose. Rerun after each batch of corrections.

**How.** Cut the beats into episodes and name each hour's curtain; a curtain that does not pull is a finding. Hold the naive perspective strictly: a name the viewer has never heard is a finding even if the returning reader knows it; a mechanism the viewer has not seen work is a finding even if the notes explain it. List drag (sequences with no antagonist action, sit-down revelations in a row, a curtain call after the climax), unfollowable references, and raises per register. Deliver as assessment only; the author accepts findings in bulk or with guidance, and the corrections are applied to the beats and the notes the same sitting. Save each pass as a dated file so the trajectory is visible. Kestrel's outline took five passes to clean; the fifth found nothing structural.

**Origin.** Kestrel Book 4, September 11 2026 (the author's exercise).

**Scope.** Fiction.

---

### The ownership audit

**What.** Every action in every beat is checked for who owns it: the agent with the standing (office, ownership, jurisdiction) and the motive to do it, and whose consent it silently assumes.

**When.** After a reconstruction or a large batch of beat changes; before the prose; whenever a beat reads as plot-driven.

**How.** For each action: who does it; is it theirs to do; would this person do it; whose consent does it require and is that consent on the page. Findings are usually wording (a ship "has already begun" a revival that is the master's to order; a subordinate "sends" a superior; guests moved on someone else's ground without the host's word) and are corrected in place; a substantive finding (an act wrongly owned by a character whose constitution forbids it) goes to the author for ruling and often improves the mechanism (Kestrel: an arms shipment re-owned from a commander's introductions to a host's treaty clearance). Companion to the presence audit; the two are run together.

**Origin.** Kestrel Book 4, September 11 2026 (the author's instruction after the first viewer pass).

**Scope.** General.
