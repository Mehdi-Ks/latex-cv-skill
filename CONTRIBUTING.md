# Contributing to latex-cv-skill

Thanks for your interest. This skill was built through real-world ATS testing and iterative refinement — contributions that come from the same kind of hands-on experience are the most valuable.

---

## What we're looking for

### 1. ATS test results
The current scores come from one tool ([ats-screener.vercel.app](https://ats-screener.vercel.app/scanner)) and one CV. That's a sample of one. If you compile the demo CV and run it through a different ATS tool — or through the same tool with your own CV — open an issue using the **ATS Test Result** template and share what you got. Positive or negative, it's useful data.

### 2. Bug reports
Something doesn't compile? A logo renders wrong? A section spills to page 2? Open a **Bug Report** issue with your Overleaf compiler log and we'll work it out.

### 3. Improvement suggestions
Things we know are open questions:
- **Non-Latin names and text** — Arabic, CJK, accented characters: untested
- **Academic CV variant** — publications, conferences, thesis sections not covered
- **Two-column layout** — some recruiters prefer it; would it break ATS?
- **Colour schemes** — the green is opinionated; alternatives would be welcome
- **Font fallbacks** — what happens if TeX Gyre fonts aren't available on a local TeX installation?
- **Windows vs Mac Overleaf behaviour** — any differences in rendering?

If you have a solution to any of these, open a **Suggestion** issue or submit a PR directly against `skill/references/base_template.tex`.

---

## How to submit a PR

1. Fork the repo
2. Edit the files in `skill/` (the `.skill` file is generated from these)
3. Test your change by compiling `example/main_demo.tex` in Overleaf with XeLaTeX
4. If you changed the skill instructions, also test by running the skill in Claude Cowork against a sample CV
5. Submit a PR describing what you changed and why

---

## What not to submit

- Changes that improve visual design but break ATS scores — run the screener before and after
- PRs that add dependencies beyond a standard Overleaf XeLaTeX environment
- Unverified claims about ATS compatibility

---

## Questions?

Open a **Suggestion** issue — no need to have a fix ready, a well-described problem is a valid contribution.
