# Public Interest Data Science

A Quarto textbook by Brian C. Keegan (University of Colorado Boulder, Department of Information Science).

This book teaches data science for public-interest ends. It has five parts:

1. **Pressures and Values**. The installed base and its predecessors, then three paired chapters: enclosure and openness, exemption and oversight, erosion and ownership.
2. **Lineages**. What data scientists can inherit from journalism, law, accounting, planning, and engineering.
3. **Adjacent Conversations**. Public interest technology, data for good, GovTech, civic tech, critical data studies, and refusal.
4. **Genres**. How to actually do the work: op-eds, reports, research proposals, testimony, public comments, and archival deposits.
5. **Closing**. The limits of the framework.

Chapters are written to be read out of order. Lineages and genres each have a natural level of government (journalism and op-eds at the city; planning and public comments at the county; law and testimony at the state; accounting, engineering, and reports at the nation).

The book is the companion to INFO 4871/5871 *Public Interest Data Science* at CU Boulder (course materials: [cuinfoscience/pids-Spring2027](https://github.com/cuinfoscience/pids-Spring2027)), which assigns its chapters out of order. It builds on the framework laid out in Keegan (2026), "Public interest data infrastructuring."

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
- Every Part IV chapter ends with a submittable artifact.

## License

The text, figures, and exercise prompts are licensed under [Creative Commons Attribution 4.0 International](https://creativecommons.org/licenses/by/4.0/). The code (including examples and the book's build infrastructure) is licensed under the MIT License in [LICENSE](LICENSE).

## Acknowledgments

Draft zero was produced with assistance from Claude (Anthropic). See [appendix-ai-disclosure.qmd](appendix-ai-disclosure.qmd) for the disclosure statement. Students, collaborators, and reviewers who shaped the final text are named in the index.
