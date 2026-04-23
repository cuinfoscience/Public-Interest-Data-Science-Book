# Editorial Voice Guide

This file is the contract future contributors and automated assistants sign when they edit this book. Read it before you open a pull request. Read it again before you submit one.

## What this book is

*Public Interest Data Science* is a 22-chapter Quarto textbook that teaches data science as a public-interest practice. It organizes its argument around five parts: **Pressures**, **Values**, **Lineages**, **Adjacent Conversations**, and **Genres**. It is the companion volume to the INFO 46XX course at the University of Colorado Boulder and builds on the framework laid out in Keegan (2026), "Public interest data infrastructuring."

The book is opinionated. It takes a position on what "public interest" means (linkability, interpretability, continuity, safe scrutiny, authority, remedy — the installed base) and uses that position as a diagnostic throughout. Chapters do not reproduce the paper. They extend it, test it against particular cases, and, in Part V, translate it into practice.

## Voice

**Second person, formal but approachable.** Address the reader as "you." Avoid "we" when giving instructions; "we" implies complicity in a decision the reader has not yet made. Use "we" sparingly, and only when genuinely inviting the reader into a shared act of interpretation.

**No em-dashes as a stylistic tic.** This is the single most common pattern to watch for. Use commas, periods, colons, or parentheses instead. If you are reaching for `—` because the sentence is trying to do too much, rewrite the sentence. A book that lives on em-dashes reads like a draft.

**Dry humor, sparingly.** A wry observation once per chapter is fine; a joke every other paragraph is not. The subject matter is serious. The voice is not grim. There is room for amused frustration with bad library defaults and genteel contempt for audit-washing. There is no room for cute.

**Concrete over abstract.** When introducing a concept, anchor it to a specific case: a named dataset, a dated court filing, a particular API endpoint. Abstract concepts that never touch an example are for other books.

## Structure of each chapter

Each chapter is approximately 3,000 words (2,700–3,300 is the tolerance; Chapter 16 runs toward the upper bound by design). The structure is not rigid, but every chapter contains:

1. **An opening conceptual frame.** Two to four paragraphs that introduce the chapter's question. Draw on the paper's framework. Name the stakes.
2. **A transition into a technical problem.** The concept makes a particular failure mode visible. Name it.
3. **A tutorial.** Runnable Python code, with expected output as comments. Length varies by topic.
4. **Interpretive reflection.** What did the tutorial demonstrate about the concept?
5. **Callouts.** At least one "Missing Manual" (`::: {.callout-tip title="The Missing Manual"}`) and at least one "In the Public Interest" (`::: {.callout-note title="In the Public Interest"}`). See below.
6. **4–5 graduated exercises.** From guided ("follow these steps") to open-ended ("design a pipeline that…"). At least one must be runnable on a student laptop against real public data.
7. **A closing reflection** that points forward to the next chapter or part.
8. **Further Reading and Resources** — a curated bulleted list of 5–10 external links.

The 50/50 theory-technique balance is not enforced by line count. It is enforced by feel: a reader should never be reading three straight pages of either code or prose without the other checking in.

## Callouts

The two callout conventions are load-bearing. Do not skip them.

**The Missing Manual** (`::: {.callout-tip title="The Missing Manual"}`) flags things most textbooks omit: a library's surprising default, a real-world API friction that breaks the tidy example, the politics of a "simple" choice, the gap between what documentation says and what the service actually does. Every chapter needs at least one.

**In the Public Interest** (`::: {.callout-note title="In the Public Interest"}`) explicitly ties the technical material back to openness, oversight, or ownership as defined in Chapters 5–8. Every chapter must reference at least one of these three values, by name, with a specific claim about how the chapter's work advances or complicates it. Do not hand-wave.

A chapter may have more of either kind. It may not have fewer.

## Code conventions

Code blocks are non-executing globally, set in the chapter YAML:

```yaml
execute:
  eval: false
```

Runnable examples are illustrative, not part of the build. Include expected output as comments (`# => 42`) where it clarifies. Use `pandas`, `requests`, `sqlite3`, `geopandas`, `fairlearn`, `internetarchive`, and the Zenodo REST API as the default toolkit. Avoid proprietary tools and paid services unless the chapter is specifically about them.

Prefer the smallest example that makes the point. A 400-line notebook is not a virtue.

## Cross-references and citations

**Chapter anchors** are declared at the top of each chapter using `# Chapter Title {#sec-ch-NN-slug}` where `NN` is the zero-padded chapter number and `slug` matches the filename after `ch-NN-`. Reference other chapters with `@sec-ch-NN-slug`.

**Citations** use `[@keyname]` for parenthetical citations and `@keyname` for narrative ("Keegan [-@keegan2026] argues…"). All keys must resolve against `references.bib`. Do not invent citation keys.

Suggested BibTeX entries you cannot verify should go into `references.bib` with a `TODO:` note, not silently added.

## Part V convention: the artifact

Part V chapters (17–22) carry an additional convention: each must end with a real artifact the reader has produced. Not a thought experiment, not a paragraph saying what they would write if they wrote one. An actual draft op-ed, a report section they can submit, a proposal specific-aims page, a testimony statement, a public comment on a live rulemaking, or an archival deposit with a resolvable identifier.

A student who finishes the book should be able to point to six submittable artifacts they produced from these chapters. If a Part V chapter's exercise does not produce one, the chapter is not finished.

## Voice in the technical prose

Technical prose gets the same voice as conceptual prose. "The function returns a `Response` object, not the response body, which surprises roughly everyone their first time" is acceptable. "The function returns a `Response` object" is also acceptable. "The intricate dance of HTTP semantics bestows upon us a `Response` object" is not acceptable under any circumstances.

When a library's behavior is surprising, name the surprise. Do not pretend it is obvious. This is what "Missing Manual" callouts are for.

## How to propose a change

- **Typos and small fixes:** open a pull request directly. No issue required.
- **Rewriting a section or replacing an example:** open an issue first, explain the change, and wait for a maintainer response before drafting.
- **New chapter or substantial reorganization:** open an issue with a one-page proposal. Do not draft the chapter until the proposal is accepted. The book's five-part structure is stable; proposed new material will usually extend an existing chapter rather than add one.

## Build environment

Quarto 1.4+. Python 3.11+. Run `quarto preview` for live editing and `quarto render --to html` to build the book. The book also builds to PDF and EPUB, but HTML is the canonical form.

Before opening a pull request:

- [ ] Run `quarto render --to html` and confirm a clean build.
- [ ] Run `wc -w ch-*.qmd` and confirm your chapter is 2,700–3,300 words.
- [ ] Confirm at least one "Missing Manual" and one "In the Public Interest" callout.
- [ ] Confirm cross-references resolve.
- [ ] Confirm no em-dashes have crept in.

## What not to do

- Do not rewrite Keegan (2026). Cite it.
- Do not conflate op-eds, reports, and testimony. Part V's pedagogical value comes from treating each genre as distinct.
- Do not invent datasets, citations, or URLs. Flag gaps with `TODO:` comments.
- Do not add decorative prose to pad word count. Cut a paragraph before adding one.
- Do not introduce em-dashes. You were warned.

## A note to future assistants

If an automated assistant is drafting a chapter, its output should pass every check in this document unchanged. If it does not, the prompt needs rewriting, not the output rewriting after the fact. The point of this file is to make the editorial contract legible to humans and machines alike.

Welcome.
