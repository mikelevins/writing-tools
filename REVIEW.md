# Review of the extraction

Written September 10 2026 at the end of the first extraction pass. Items for the author's ruling: corrections I could not make with confidence, overlaps, culling candidates, and process questions. Strike items as they are ruled; delete the file when it is empty.

## What I did and did not do

- I worked from the source documents in both projects, not from the two summaries. The pasted Reptile House summary had several truncated lines ("Universe topology. A held-precisely map of whied to keep character knowledge straight"; "the title-edits file is a pending polish pass to risibility"); where a summary line and a source document differed, the source won.
- Every entry's *Origin* uses the date and attribution tags in the source documents (`(mikel, 8/25)`, the provenance note at the end of the rug-pull discipline). Where a document carried no date I wrote the year or "2026"; where it carried no attribution I wrote "both projects" or gave none. Correct any of these.
- I did not touch either source project or `writing-method.md`.

## Corrections wanted

1. **Dates I guessed.** `ACT_THREE_FRAMEWORK.md` (ambient noise floor, gas leak), the ensemble inventory and tactical framework, the event format, and the Event 23 expert-ecology session are dated "2026" or "March 2026" by inference from `CLAUDE.md`'s creation date. Supply the real dates if they matter.
2. **Attribution gaps.** The weirdness gradient, the rope trap, the Kolchak moment, the foreshadowing map, the echo, and the recorder sessions are all unattributed in the Book 1 documents. If any of these are yours rather than joint, say so and I will add it.
3. ~~**The "title-edits" tool.**~~ RULED September 10 2026: extracted as *The running-motif audit* in `craft/structure-and-pacing.md` (a polish pass after the outline closes, seeding a promised motif at the moments its work naturally happens; the source is Book 1's spreadsheet behind the title, crowded out by the voice memos).
4. **"Universe topology."** I folded it into *Fair play for knowledge* as "a knowledge map (who knows what, as of which event)." If the summary meant something more specific (a map of which universe each character is in and what each knows about crossings), it is a Book 1 instrument and I would leave it out.

## Overlaps to resolve

- **Motivation** appears three times: *Motivation first* (`method/outline-and-beats.md`), *The character catechism* and *The active protagonist* (`craft/character-and-comedy.md`). I kept them separate because they answer different questions (how to derive a beat; what to record per character; what the protagonist must do), but they could be one entry.
- **The expert ecology** appears in *Experts, genuine and self-appointed* (rug-pull) and *The rules need not exist* (magic). Both uses are real; one could point at the other.
- **Three ladders.** *The three ladders* (rug-pull), *The ladder of destinations* (magic), and *The weirdness gradient* (weirdness) are kept distinct on purpose, per the discipline's own insistence that they are three objects. Confirm that is the right cut.
- **The two-audience line** sits under *Stingy history*. It is arguably a structure tool. Move it if you like.
- **Fun is always important** is in structure and referenced from character and from the derivation bundle. One home is enough; I chose structure.

## Culling candidates

Included as *Pattern* (project-specific instance, transferable shape). Cut any that do not earn their place:

- *The ensemble inventory* and the tactical framework (character-and-comedy).
- *The consequence network as story engine* (character-and-comedy).
- *Interior contact never owns a choice* (character-and-comedy). This is a thematic invariant of one book; I kept it as the example of a constitution stating one.
- *The secret-keeper's evasion is grief, not strategy* (character-and-comedy). Close to Book 1's specifics.
- *Choosing the investigator by who owns the case* (character-and-comedy). Genre-specific but general within the genre.
- *The standing review rulings* list (prose-review). Author-specific by design; kept because the point of the list is that corrections are made once.

Deliberately excluded as project-specific:

- Book 1's cast-specific pitfalls (the Horned One, Rowan, the almost-distilled, the identity abyss).
- Portal properties, signatures, and preferred field architecture.
- The Continuity briefing content and the operational survival playbook.
- The `.pages` extraction procedure and the ugrep note (the latter survives as a parenthetical).
- The voice-memo epigraph idea (marked "under consideration" in the source; not yet a tool).
- Kestrel's "avoid superlatives about the solar system" (setting-specific; the general form, "no superlatives about a setting too large to survey," did not seem worth an entry).
- The Route A–D synopses themselves. The route annotation format is extracted; the routes are examples and stay in the experiments folder.

## Ruled September 10 2026

- **The rubric.** Kestrel's five functions and five unsubtle kinds and Reptile House's Funny/Creepy bullets are replaced by one six-register rubric: surprise, comedy, tragedy, creepy, character, cool (`craft/rubric.md`, its own file since it applies to every beat and scene, not only the trove). Not yet propagated to the source projects: Kestrel's `reference/moment-trove.md` still scores by `functions: drama, ...` and tags `gasp`; the concordance in the rubric entry reads them. Update the Kestrel file when convenient, or leave it and let new entries use the new vocabulary.

## Process questions

1. **`writing-method.md`** at the writing-projects root is now superseded by `method/`. Move it to an attic here, or delete it? I left it in place.
2. ~~**Git.**~~ RULED September 10 2026: the directory is the `writing-tools` repository, committed and pushed.
3. ~~**Pointers from projects.**~~ RULED September 10 2026: a *Shared tools and methods* section is now at the top of both projects' `CLAUDE.md` files. It makes the tools directory authoritative for method, tells sessions to correct stale conventions in the same sitting and log the migration in the handoff, forbids wholesale reorganization without a ruling, and lists each project's pending migration (Kestrel: re-tag the moment trove to the rubric; Reptile House: none). This also answers question 6 for `method/`.
4. **The scope taxonomy.** *General / Fiction / Genre / Pattern / Series / Collaboration.* Is that the right set of labels, or would you rather a two-value split (general vs. this-setting-only)?
5. **Granularity.** Some entries are one paragraph; the rug-pull file reproduces most of its source. If the file is meant to be loaded on demand, that is fine; if it is meant to be read through, several entries could be halved.
6. **What the source projects should do.** Two options once this is ruled: leave the source documents as they are and let this project drift from them, or make this project authoritative for method (not for craft, which each series owns) and have the projects' `CLAUDE.md` files point here instead of restating the conventions. I lean to the second for `method/` only.
