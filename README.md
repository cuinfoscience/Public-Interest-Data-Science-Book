# Public Interest Data Science

A Quarto textbook by Brian C. Keegan (University of Colorado Boulder, Department of Information Science).

This book teaches data science for public-interest ends. It has six parts. The four middle parts are modules that each pair a professional lineage with a level of government and end in a portfolio piece:

1. **Foundations**. The contested public interest; the framework of pressures (enclosure, exemption, erosion), values (openness, oversight, ownership), and the installed base; and neighboring fields.
2. **Journalism: The City**. Enclosure → openness. Reproduce an investigation, publish city data, write an op-ed.
3. **Law: The County**. Exemption → oversight. Request county records under CORA, build an exemptions and remedy ledger, write testimony.
4. **Assurance: The State**. Accounting and engineering. Audit-washing → oversight. Run and test a disaggregated audit, write a report for a state body.
5. **Planning: The Nation**. Erosion → ownership. Audit a federal dataset's decay, design stewardship or refusal, write a public comment on a federal rulemaking.
6. **Beyond the Portfolio**. Research proposals, archival deposits, and the limits of the framework.

The book is the companion to INFO 4871/5871 *Public Interest Data Science* at CU Boulder (course materials: [cuinfoscience/pids-Spring2027](https://github.com/cuinfoscience/pids-Spring2027)). It builds on the framework laid out in Keegan (2026), "Public interest data infrastructuring."

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
- Every module ends with a genre chapter whose last exercise is a submittable portfolio piece.

## License

The text, figures, and exercise prompts are licensed under [Creative Commons Attribution 4.0 International](https://creativecommons.org/licenses/by/4.0/). The code (including examples and the book's build infrastructure) is licensed under the MIT License in [LICENSE](LICENSE).

## Acknowledgments

Draft zero was produced with assistance from Claude (Anthropic). See [appendix-ai-disclosure.qmd](appendix-ai-disclosure.qmd) for the disclosure statement. Students, collaborators, and reviewers who shaped the final text are named in the index.
