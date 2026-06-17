# Overleaf Setup Guide — LaTeX CV

This guide walks you through compiling your CV in Overleaf in under 5 minutes.

---

## What's in this zip

| File | Purpose |
|---|---|
| `main.tex` | Your CV source code |
| `logo_*.png` | Company / institution logos |
| `OVERLEAF_SETUP.md` | This guide |

---

## Step 1 — Create a new Overleaf project

1. Go to [overleaf.com](https://www.overleaf.com) and sign in (free account is fine)
2. Click **New Project → Blank Project**
3. Give it a name (e.g. "My CV")

---

## Step 2 — Upload your files

In the left sidebar of the Overleaf editor:

1. Click the **Upload** button (file icon with an upward arrow)
2. Select **all files from this zip** — `main.tex` and every `logo_*.png`
3. When asked about replacing `main.tex`, click **Yes**

All files must be at the **root level** of the project (not inside any subfolder).

---

## Step 3 — Switch the compiler to XeLaTeX

> ⚠️ This step is mandatory. The CV uses the `fontspec` package which requires XeLaTeX. It will not compile with pdfLaTeX.

1. Click **Menu** (top-left hamburger icon)
2. Under **Settings → Compiler**, select **XeLaTeX**
3. Close the menu

---

## Step 4 — Compile

Click the green **Recompile** button. Your CV should appear in the preview pane on the right.

If you see any errors, the most common causes are:

| Error | Fix |
|---|---|
| `fontspec error` | You forgot to switch to XeLaTeX (Step 3) |
| `File 'logo_X.png' not found` | The logo file wasn't uploaded, or the filename doesn't match |
| Output is 2 pages | Content is too long — shorten some bullets or the summary |

---

## Step 5 — Download your PDF

Once it compiles successfully:

1. Click the **Download PDF** button (arrow-down icon above the preview)
2. Your CV is ready to send

---

## Updating your CV

To edit content, click on `main.tex` in the left sidebar. The file is structured with clear section comments like `% ── WORK EXPERIENCE`. Make your changes and click **Recompile**.

**Tip**: Each time you update a URL, you need to check that the `\href{...}` links in the relevant `\jobheader` or `\recogentry` calls are correct.

---

## Replacing placeholder logos

If any logos are placeholders (green circles with initials), replace them:

1. Find the real company logo online (PNG with transparent background works best)
2. In Overleaf, click the upload button and upload the new PNG
3. Name it exactly as the placeholder was named (e.g. `logo_companyname.png`)
4. Recompile — the new logo will appear automatically

---

## Tips for best results

- **Keep it one page.** If content overflows, trim older bullet points first.
- **Action verbs.** Start every bullet with a strong verb: Architected, Delivered, Built, Led, Reduced…
- **Hard numbers.** At least one metric per bullet (%, ×, time saved, scale) scores much better on ATS systems.
- **ATS compatibility.** The section headers in this template are specifically formatted to pass ATS parsing. Do not change `\cvsection` formatting.
