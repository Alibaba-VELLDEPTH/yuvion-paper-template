# Alibaba / Yuvion Paper Template

**English** | [简体中文](README.zh-CN.md)

A single-column paper and technical report template for Yuvion Team, Alibaba
Group. The first page features large Alibaba Group and Yuvion logos, orange
title rules, a rounded abstract frame, and an author-contribution footer.

**[Download Overleaf ZIP](https://github.com/Alibaba-VELLDEPTH/yuvion-paper-template/raw/refs/heads/main/overleaf.zip)**
· **[View the 6-page PDF](preview.pdf)** · **[Formatting details and sources](FORMAT.md)**

![First-page preview](preview.png)

## Overleaf

1. Download the ZIP above and choose **New Project → Upload Project** in Overleaf.
2. Set `main.tex` as the main document and select **XeLaTeX** as the compiler.
3. Edit the title, authors, affiliations, email, project links, and author contributions in `metadata.tex`.
4. Replace the sample content in `sections/` and the lead figure in `figures/teaser.tex`.
5. Maintain your bibliography in `references.bib`.

## Local build

```bash
latexmk -xelatex main.tex
```

You can also run `tectonic main.tex`. All logos and heading fonts are included.

## Contents and structure

```text
main.tex                Main document
README.md               English guide (default)
README.zh-CN.md         Simplified Chinese guide
metadata.tex            Title, authors, affiliations, contributions, links, and draft switch
alibaba-report.sty      Shared formatting settings
sections/               Abstract, main text, appendix, and examples
figures/teaser.tex       Vector placeholder for the first-page lead figure
logos/                  Alibaba Group and Yuvion logos
fonts/                  Heading and author fonts bundled with the reference paper source
references.bib          Sample bibliography
FORMAT.md               Formatting details, sources, and differences
preview.pdf             6-page PDF compiled from the same source
overleaf.zip            Complete project ready to upload to Overleaf
```

Examples cover three heading levels, run-in headings, lists, equations, aligned
equations, a proposition and proof, three-rule tables, subfigures, algorithms,
code, footnotes, numeric citations, supplementary contents, and appendices.
Dashes (`--`) in tables are placeholders, not experimental measurements.

```latex
\citep{vaswani2017attention}     % Numeric citation
\citet{vaswani2017attention}     % Author name with numeric citation
Figure~\ref{fig:teaser}          % Figure cross-reference
Equation~\eqref{eq:objective}    % Equation cross-reference
\includegraphics[width=\linewidth]{figures/your-figure.pdf}
\todo{Text to revise}            % Controlled by the draft switch in metadata.tex
```

The manuscript uses US Letter paper, a single column, 10pt body text, 12pt
baseline spacing, and 25mm side margins. An explicit page break starts the
main text on page two. See [FORMAT.md](FORMAT.md) for the full specification.

## Author-contribution footer

The first-page footer displays **Author contributions**, listing each author's
work. Later pages display only the page number. Edit `\authorcontributions` in
`metadata.tex`. Replace the bracketed examples with actual contributions, such
as research design, methodology, implementation, experiments, analysis,
validation, supervision, or manuscript revision. To omit the contribution
footer, set `\renewcommand{\authorcontributions}{}`.

## Replacing the previous templates

The main branch now contains only this template. The previous `double-column/`
(CVPR-style) and `single-column/` (NeurIPS-style) versions have been retired.
They remain available in the
[Git history](https://github.com/Alibaba-VELLDEPTH/yuvion-paper-template/commits/main/).

## Sources

- Alibaba Group logo: [official media resources](https://home.alibabagroup.com/en-US/resource-logos).
- Yuvion logo: the original team branding assets in this repository.
- Heading and author fonts: JD LangZhengTi2 bundled with the reference paper source; body text uses the related Latin Modern family.

This is a customized team paper template, not a centrally issued official
Alibaba Group template. Fonts and branding assets retain their respective
ownership; this repository does not grant additional rights to third-party
materials. For conference or journal submissions, follow the venue's official
author kit.

## Validation

The source has been compiled with Tectonic / XeTeX, and all six PDF pages have
been visually checked. The example has no undefined references, missing
glyphs, or text extending beyond the margins.
