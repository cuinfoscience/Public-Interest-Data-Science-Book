# Public Interest Data Science

A Quarto textbook by Brian C. Keegan (University of Colorado Boulder, Department of Information Science).

This book teaches data science for public-interest ends. It has five parts:

1. **Pressures** — enclosure, exemption, and erosion as structural forces on public knowledge.
2. **Values** — openness, oversight, and ownership as the installed base of accountability.
3. **Lineages** — what data scientists can inherit from journalism, law, accounting, planning, and engineering.
4. **Adjacent Conversations** — public interest technology, data for good, GovTech, civic tech, critical data studies, and refusal.
5. **Genres** — how to actually do the work: op-eds, reports, research proposals, testimony, public comments, and archival deposits.

The book is drafted as the companion to INFO 46XX *Public Interest Data Science*, taught at CU Boulder. It builds on the framework laid out in Keegan (2026), "Public interest data infrastructuring."

## Reading the book

The rendered HTML build lives in `_book/` after running Quarto. Online hosting is forthcoming.

## Building locally

You need [Quarto](https://quarto.org) 1.4 or newer and Python 3.11+.

```bash
git clone https://github.com/brianckeegan/Public-Interest-Data-Science-Book.git
cd Public-Interest-Data-Science-Book
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt   # (forthcoming)
quarto preview                    # live preview
quarto render --to html           # build static site
```

Code blocks are non-executing by default (`execute: eval: false` in `_quarto.yml`). Runnable examples are illustrative. See [claude.md](claude.md) for the editorial rationale.

## Contributing

Contributions are welcome: typo fixes, better examples, new case studies, additional exercises, even whole new chapters. Before you open a pull request, please read [claude.md](claude.md), which codifies the voice, structure, and citation conventions the book follows.

The short version:

- Second person ("you"), formal but approachable.
- Every chapter weaves concept and technique at roughly 50/50.
- Every chapter has at least one "Missing Manual" callout and one "In the Public Interest" callout.
- No em-dashes as a stylistic tic.
- 4–5 graduated exercises per chapter.
- Every Part V chapter ends with a submittable artifact.

## License

The text, figures, and exercise prompts are licensed under [Creative Commons Attribution 4.0 International](https://creativecommons.org/licenses/by/4.0/). The code (including examples and the book's build infrastructure) is licensed under the MIT License in [LICENSE](LICENSE).

## Acknowledgments

Draft zero was produced with assistance from Claude (Anthropic). See [appendix-ai-disclosure.qmd](appendix-ai-disclosure.qmd) for the disclosure statement. Students, collaborators, and reviewers who shaped the final text are named in the index.
