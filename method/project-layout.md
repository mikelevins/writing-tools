# Project layout and document discipline

Where things live in a novel project, which document wins, and how superseded material is kept without keeping its authority. Entry format is described in `../README.md`.

---

### The constitution

**What.** One governing document per book: the story's fork (its deepest canon), theme, character geometry, and craft principles. Authoritative over every other document.

**When.** Every project. Write it first, amend it continuously.

**How.** When two documents disagree, the constitution wins. When the constitution is silent, ask the author. Working principles specific to the book (its thematic invariants, its genre calibrations, its magic budget) live here, each dated and attributed, so a later session can see who ruled what and why. A constitution states invariants as constraints, not as specifications.

**Origin.** Kestrel Book 4, August 24 2026 (the reset session). Reptile House has the equivalent split across `CLAUDE.md` (principles) and the story bible.

**Scope.** General.

**See also.** *Document precedence*, below; *The canon ledger* in `sessions-and-rulings.md`.

---

### Four kinds of work, four homes

**What.** A directory layout in which the top level holds only process files, the outline, and the manuscript, and everything else lives in a directory named for its kind of work.

**When.** Any project past the first few documents.

**How.**

```
Book/
├── CLAUDE.md          conventions (this layout, naming, working principles)
├── HANDOFF.md         session handoff: current state, next work, canon ledger. Read first.
├── REVIEW.md          prose review queue (see prose-review.md)
├── outline.md         every beat in story order, action only
├── <manuscript>       the current draft
├── notes/             the outline's auxiliary layer, one file per event
├── reference/         canon and planning: what is true (constitution, setting, cast, triage, derived rules, art)
├── drafts/            superseded prose, dated in the filename
├── publication/       cover, blurb, query, front and back matter
└── attic/             superseded planning material, mirroring the live tree
```

Reptile House uses an older variant: per-book working directories (`47-details/`) holding act files and a per-book `reference/`, a series-level `reference/`, and `experiments/` for non-canon design. The principle is the same: each kind of work has one home, and the home tells you the document's authority.

**Origin.** Kestrel Book 4, ratified August 28 2026, after a reorganization sitting.

**Scope.** General.

---

### The attic

**What.** One top-level directory holding documents that are no longer active participants in the work. Readable on demand, carrying no authority.

**When.** Whenever a document stops being active. Move it rather than deleting it.

**How.** One attic, at the top level, mirroring the live tree: a file retired from `reference/x.md` goes to `attic/reference/x.md`. Never an attic inside a subdirectory. Superseded prose is the one exception and goes to `drafts/`. Anything drawn from the attic must re-earn its place against the constitution. A cut beat goes to the attic as a block, and the live notes file keeps a one-line record saying where it went and why, so the cut is known to be deliberate.

**Origin.** Kestrel Book 4, August 28 2026. Reptile House has used an attic since 2025 with a naming note for renamed characters ("if you encounter the old name in attic documents, read as the new one").

**Scope.** General.

---

### Document precedence

**What.** An explicit statement, in the conventions file, of which document wins on which question.

**When.** Any project with more than one layer of planning, and especially any project with a reset, a POV change, or a rebuilt outline behind it.

**How.** State precedence by question, not by file age. Reptile House's rule: the act files are authoritative for any event they contain a full entry for; the series reference is authoritative on world, character, metaphysics, and tone but not on Book 1 plot; the first-draft files are source material only, never authoritative over current files; everything in the attic is superseded. Kestrel's rule is simpler because the constitution exists: the constitution wins, then the beat series where staging conflicts with older triage, then the reference files. A superseded document gets a header saying so and what replaced it.

**Origin.** Reptile House, March 2026 (the Blair-POV to Avery-POV transition made it necessary).

**Scope.** General.

---

### Project-root-relative paths

**What.** Every path in every document is written relative to the project root, whatever directory the referring document lives in.

**When.** Always.

**How.** `reference/constitution.md`, never `../reference/constitution.md`. A bare event key in backticks is shorthand for that event's notes file. Filenames carry no redundant prefix (every file is already in the project) and put the distinctive part of the name first.

**Origin.** Kestrel Book 4, August 28 2026.

**Scope.** General.

---

### Decisions are folded in as they are made

**What.** Every ruling goes into the document that owns it during the sitting in which it is made. Nothing is left only in chat.

**When.** Always. This is the rule most often broken and most expensive to break.

**How.** The session-close checklist (see `sessions-and-rulings.md`) enforces it. A canon fact goes to its reference file, a beat change to the outline and its notes file together, a review ruling to the review queue. The lesson came from one sitting in which documentation debt was allowed to accumulate; repaying it cost a full session.

**Origin.** Kestrel Book 4, April 2026 (the debt), rule stated August 2026.

**Scope.** General.

---

### Tracking-file hygiene

**What.** The status line at the top of a handoff file is a single-line statement of the most recent update, replaced each time, never an accumulating history.

**When.** Every tracking file.

**How.** Session history belongs in an append-only session-notes file that is not loaded at session start. If a status block grows large enough to impede reading or editing, it is too large: compress it or move the history out. A handoff file's dated closing paragraphs ("amended at the close of the September 3 sitting: ...") are the compromise Kestrel adopted; they work but are the first thing to trim.

**Origin.** Reptile House, March 2026.

**Scope.** General.

---

### The handoff file

**What.** The one document a session reads first. It holds where things stand, the next work in order, the canon ledger, standing warnings, and the session-close checklist.

**When.** Every project.

**How.** Sections that have proved their worth: a *Where things stand* block (replaced, not appended); *Next work, in order*; a *Read first, in order* list naming the documents and what each carries; *Major new canon blocks* since the last full rewrite, each pointing to the owning file; the *canon ledger* (see `sessions-and-rulings.md`); *Standing warnings* (corrections that must not regress: dead images, superseded names, stale claims in shared setting notes); the *drawer* (see below); and the *session-close checklist*. Rewrite it wholesale when it gets long; the closing line says "replaces all prior handoffs" and is dated.

**Origin.** Both projects. Kestrel's current form dates from August 28 2026.

**Scope.** General.

---

### The drawer

**What.** A list of reserves the story could use but has not authorized: deep-history inventions, sealed backstory, unspent characters, ideas that would change the book's shape.

**When.** Whenever a good idea arrives that the current book does not need.

**How.** Record it in one line in the handoff file under a heading that says it opens only by the author's word. Nothing in the drawer is canon; nothing in it is planted; a session that wants one of them asks. The drawer keeps the stingy-history and stingy-magic disciplines honest (see `../craft/magic-and-metaphysics.md`) by giving unspent inventions somewhere to go other than the page.

**Origin.** Kestrel Book 4, August 2026. Reptile House's "Redcap: saved for later" section is the same instrument.

**Scope.** General.

---

### The experiments folder

**What.** A home for non-canon design work: alternative shapes, format experiments, synopses written to be examined rather than adopted.

**When.** Whenever the work is "what would this look like if" rather than "what is true."

**How.** Each experiment file opens with its parameters, a non-canon label, and an invention flag listing every character, event, or fact it made up, so nothing leaks back into canon without being noticed. Superseded runs are kept and labeled superseded, not deleted, because a later synthesis often needs to compare them. When an experiment produces something the project adopts, the adopted part is transcribed into the reference layer with provenance; the experiment file stays where it is.

**Origin.** Reptile House, September 2026 (six TV-season experiments, two series designs, the routes file).

**Scope.** General.

---

### Provenance notes

**What.** A note at the end of a reference document saying which of its points are the author's and which are the workshop partner's derivations accepted without objection.

**When.** Any document that consolidates a design conversation.

**How.** Two lists, by section: "Mikel's: ..." and "Claude's derivations, accepted in conversation without objection: ...". Also mark, inline, which numbers and facts were generated by a tool (an image generator, a name generator) rather than ruled, so a generated figure is never later promoted to canon by accident. The Esgar height error in Kestrel came from exactly that promotion.

**Origin.** Reptile House, September 9 2026 (the rug-pull discipline's provenance note); Kestrel, September 5 2026 (the generator-lettered number).

**Scope.** General.

---

### The shared setting repository

**What.** For a series or a shared world, a separate repository holding facts that hold system-wide, with per-book reference files carrying pointers to it.

**When.** Any fact that would be true in the next book too.

**How.** When a book's worldbuilding produces a system-wide fact, write it to the shared repository as its own numbered file and leave a pointer in the book's setting file. Shared notes go stale; the handoff's standing warnings list the stale claims not to re-import. Read the shared repository on demand; it is large.

**Origin.** Kestrel (the-fabric-setting repository), 2026.

**Scope.** Series.

---

### Renumbering is a deliberate act

**What.** Keys, IDs, and coordinates are never renumbered as routine. A one-off cleanup renumbering is a deliberate act with a concordance table from old to new.

**When.** Whenever a numbering scheme changes.

**How.** Put the concordance at the end of the document that owns the old scheme's derivation, so old references remain resolvable. See *Dewey coordinates* in `outline-and-beats.md` for the scheme that makes renumbering unnecessary.

**Origin.** Kestrel Book 4, August 28 2026.

**Scope.** General.

---

### Commit at the close of every sitting

**What.** The project is a git repository; each sitting ends with a commit and push.

**When.** Always, including sittings that only changed planning files.

**How.** Last item on the session-close checklist. Forecloses the loss of a sitting's rulings and gives the attic a second layer.

**Origin.** Both projects.

**Scope.** General.
