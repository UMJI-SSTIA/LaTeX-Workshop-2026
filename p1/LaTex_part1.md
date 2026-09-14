
# LaTeX Workshop Worksheet1

## 0) Quick Start Checklist

- ✅ Have either local or online LaTex compling environment.
- ✅ Create a new project / folder and ensure you can **compile** to PDF.

---

## 1) What is LaTeX (and why use it)?

LaTeX (usually pronounced `LAY teck`,sometimes `LAH teck`, and never `LAY tex`) is a mathematics typesetting program that is the standard for most professional mathematics writing. It is based on the typesetting program `TeX` created by Donald Knuth of Stanford University (his first version appeared in 1978). Leslie Lamport was responsible for creating `LaTeX`, a more user friendly version of `TeX`. A team of `LaTeX` programmers created the current version,  `LATEX 2ε`.

**Why LaTeX?**
- **Consistency & automation**: automatic numbering, cross-references, 
- **Complex documents**: sections, figures, tables, footnotes.
- **Separation of content/style**: focus on writing; change styles later.
- **Portable plain text**: version-control friendly.
- **High-quality typography**: great defaults for kerning, hyphenation, spacing.

> **Exercise 1.1 (2–3 min)**  
> Decide: use **Overleaf** (no install) or a **local** setup (TeX Live / MiKTeX + editor). Create a project named `LaTeX Workshop`.

---

## 2) The Basic Document Skeleton

```latex
\documentclass[12pt]{article}
\usepackage{graphicx}   % images
\usepackage{xcolor}     % colors (used later)
\usepackage{hyperref}   % clickable refs/links (used later)

\title{My First LaTeX Document}
\author{Your Name}
\date{\today}

\begin{document}
\maketitle

Hello, LaTeX world!

\end{document}
```

**Key parts**
- `\documentclass{article}`: choose the class (`article`, `report`, `book`, `letter`, `beamer`, …).
  - `[12pt]` sets the font size
- **Preamble** (before `\begin{document}`): load packages, define commands, set metadata.
- **Body** (between `\begin{document}` and `\end{document}`): your content.
- `\maketitle`: prints title/author/date defined in the preamble.
**Remember to add `\maketitle`!**

> **Exercise 2.1 (3–4 min)**  
> Paste the skeleton, replace `Your Name`, change the title, **compile** and confirm you get a PDF.

---

## 3) Paragraphs, Line Breaks, and Text Emphasis

**Paragraphs**: leave a **blank line** between paragraphs to start a new one.  
**Line break** (avoid overuse): `\\` or `\newline`.  
**Comments**: `%` starts a comment to end of line.

Difference:
A new paragraph will auto indent, but line break don't have indentation.

**Inline emphasis**
- **Bold**: bold text in LaTeX is typeset using the `\textbf{...}` command.
- *Italics*: italicised text is produced using the `\textit{...}` command.
- <ins>Underline</ins>: to underline text use the `\underline{...}` command.
  
``` LaTex
% Codes for copy:
\textbf{bold}
\textit{italic} 
\underline{underline} 
\texttt{monospace} 
\textsc{Small Caps}
\emph{emphasis that toggles within italic contexts}
```

**Special characters (escape when needed)**: `# $ % ^ & _ { } ~ \`  
Example: `50\%`, `\{Special characterscurly\}`, `\_underscore\_`, `\textbackslash{}`.

> **Exercise 3.1 (2 min)**  
> Copy and type the following text:
> 
> SSTIA provides students with opportunities to learn **new technologies**, explore *scientific innovation*, and communicate with others.
> There is a 100% possibility that you can improve your skills through continuous learning.
> 
> **Requirements:**
> Make `new technologies` bold.
> Make `scientific innovation` italic.
> Write the percentage sign using `\%`.

---

## 4) Sectioning (Headings) and Table of Contents

Common sectioning commands in `article`:
```latex
\section{Title}
\subsection{Subtitle}
\subsubsection{Subsubtitle}
\paragraph{Run-in heading} Text...
```

**Starred versions** skip numbering: `\section*{Unnumbered}`.  
**Table of contents**: add `\tableofcontents` (after `\maketitle`); compile twice.

> **Exercise 4.1 (2 min)**  
> 1. Create the following structure:
> ``` latex
> \section{Introduction}
> LaTeX is widely used for academic papers and reports.
> \subsection{Motivation}
> Learning LaTeX helps students create professional documents.
> ```
> 2. Add `\tableofcontents` under the title and compile twice.

---

## 5) Lists: itemize, enumerate, description

```latex
\begin{itemize}
  \item Unordered list item
  \item Another point
\end{itemize}

\begin{enumerate}
  \item First
  \item Second
\end{enumerate}

\begin{description}
  \item[Term] Definition text
  \item[LaTeX] A typesetting system
\end{description}
```

Lists can be **nested** by placing one environment inside an `\item`.

> **Exercise 5.1 (3 min)**  
> Create a nested list (an `itemize` inside an `enumerate`).
> The final list should like this:
> ``` latex
> Learning Plan
> 1. Basic Syntax
>    • Text formatting
>    • Sections
> 2. Advanced Features
>    • Figures
>    • Tables
> ```

---

## 6) Figures (Images)

1) Load package in preamble: `\usepackage{graphicx}`  
2) Put your image file in the project.  
3) Use a **float** with caption + label:

```latex
\begin{figure}[ht]
  \centering
  \includegraphics[width=0.65\textwidth]{mesh} % images/Your_Image.jpg
  \caption{A helpful caption.}
  \label{fig:sample}
\end{figure}

As shown in Figure~\ref{fig:sample}, ...
```

- Placement hints:
  
| Parameter | Position |
| :---------: | :--------: |
| `[h]` | here (not exactly at the spot) |
| `[t]` | top |
| `[b]` | bottom |
| `[p]` | float page |
| `[H]` ( Requires the float package) | here (exactly at the spot)|

- combine like `[ht]` is available
- Use `\centering` and set width relative to `\textwidth`.
- Reference with `Figure~\ref{...}`.

> **Exercise 6.1 (3 min)**  
> Add an image (You can use `JoinSSTIA.jpg`). 
> Add a caption and label.
> Reference it in text with `Figure~\ref{...}`.

***Multiple Images**

1) Load package in preamble:
``` latex
\usepackage{subcaption}
\usepackage{graphicx}
```

1) Put your image file in the project. 
2) In body:
  
``` latex
   \begin{figure}[htbp]
    \centering
    
    \begin{subfigure}{0.45\linewidth}
        \centering
        \includegraphics[width=\linewidth]{image1.png}
        \caption{Image 1}
    \end{subfigure}
    \hfill
    \begin{subfigure}{0.45\linewidth}
        \centering
        \includegraphics[width=\linewidth]{image2.png}
        \caption{Image 2}
    \end{subfigure}

    \caption{Two images in one row}
\end{figure}
```

---

## 7) Tables (tabular + table)

```latex
\begin{table}[h]
  \centering
  \begin{tabular}{l|c|r}
    \hline
    Item & Description & Price (USD) \\ \hline
    Widget A & Basic widget & 19.99 \\
    Widget B & Advanced widget & 29.50 \\
    Widget C & Premium widget & 45.00 \\ \hline
  \end{tabular}
  \caption{Sample widget prices}
  \label{tab:prices}
\end{table}

See Table~\ref{tab:prices} for details.
```

- `tabular` column specifiers: `l` (left), `c` (center), `r` (right), `|` vertical lines.  
- Cells separated by `&`, rows end with `\\`, lines via `\hline`.  
- Wrap in `table` for floating, caption, and labels.

> **Exercise 7.1 (4 min)**  
> 1. Create the following table:
> 
> | Student | Department | Score |
> | :---------: | :--------: | :--------: |
> | Alice | Computer Science | 95 |
> | Bob	| Engineering	| 88 |
> | Cindy	| Physics	| 92 |
>
> - No vertical lines
> - All columns should be `centering`
> - Only retain top, middle and bottom three horizontal lines (like the sample).
>
> 2. Add a caption `Student scores` and label `tab:score`.
> 3. Reference it in text with `See Table~\ref{...}`.

***Pro tip**: For beautiful rules, use `\usepackage{booktabs}` and replace `\hline` with `\toprule`, `\midrule`, `\bottomrule`.

---
 
## 8) *Cross-References (labels + ref/pageref) 

Attach a `\label{key}` to the thing you want to reference:

- After section: `\section{Method}` `\label{sec:method}`
- Inside `figure`/`table`: usually after `\caption{...}` `\label{...}`

Then reference it:
```latex
See Section~\ref{sec:method} on page~\pageref{sec:method}.
```

> **Exercise 8.1 (3 min)**  
> Add labels to one section, one figure, and one table. Add sentences referencing each. Compile **twice** to resolve `??`.

---

## 9) *Hyperlinks (URLs and clickable refs)

Enable in preamble:
```latex
\usepackage[hidelinks]{hyperref} 
% [hidelinks]: The link color and border are not displayed. (official report)
% You can also write:
\usepackage[colorlinks]{hyperref}
% This will distinguish hyperlink from other texts.
```

Add links:
```latex
\href{https://www.latex-project.org}{LaTeX Project}
\url{https://ctan.org}
```

This also makes `\ref` and `\cite` clickable.

> **Exercise 10.1 (2 min)**  
> Add a link to an external site and confirm it’s clickable in the PDF.

---

## 10) *Page Layout, Fonts, and Spacing (quick tour)

**Margins/layout** (preamble):
```latex
\usepackage[a4paper,margin=1in]{geometry}
```

**Line spacing**:
```latex
\usepackage{setspace}
\doublespacing   % or \onehalfspacing
```

**Fonts** (modern approach with XeLaTeX/LuaLaTeX):
```latex
% Compile with XeLaTeX or LuaLaTeX
\usepackage{fontspec}
\setmainfont{Times New Roman} % or another installed font
```

**Headers/footers**:
```latex
\usepackage{fancyhdr}
\pagestyle{fancy}
\fancyhead{} \fancyfoot{} % Clear original headers/footers style
\fancyhead[L]{My Title} % Display "My Title" on the left side of the header
\fancyhead[R]{\thepage} % Display the current page number on the right of the header
```

> **Exercise 11.1 (3 min)**  
> Change page margins to 1 inch. Add a custom header with document title and page number. Re-compile.

---

## 11) *Using Packages (Like Extensions)

Basic Syntax Format:
```latex
\usepackage[options]{packagename}
```

Common picks:

- `graphicx` – images
- `xcolor` – colors
- `hyperref` – links & PDF metadata
- `geometry` – page layout
- `booktabs` – beautiful tables
- `fancyhdr` – headers/footers
- `enumitem` – control list spacing/labels
- `caption` – caption formatting
- `csquotes` – smart quotes
- `babel`/`polyglossia` – languages
- `minted`/`listings` – code formatting (requires shell-escape for `minted`)

> **Exercise 12.1 (2–3 min)**  
> Identify one feature you want (e.g., colored text, nicer tables, custom headers). Search the function and command of that package (feel free to use AI or search engines). Add the corresponding package and use one command from it.

---

## 12) *Defining Your Own Commands (Macros)

Avoid repetition and add semantic meaning.

**No-argument macro:**
```latex
\newcommand{\ProductName}{SuperWidget}
Our \ProductName{} is great!
```

**With arguments:**
```latex
\newcommand{\bt}[1]{\textbf{#1}} 
% {\bt}: new command name
% [1]: accept 1 parameter
% {\textbf{#1}}: {\textbf} = {\bt}
% {#1}: the first parameter
\bt{Important}
```

**Advanced example (requires xcolor):**
```latex
\newcommand{\bluetext}[1]{\textcolor{blue}{#1}}
This is \bluetext{blue text}.
```

> **Exercise 13.1 (3 min)**  
> Define a `\highlight{...}` macro that uses color or `\textbf{}`. Use it twice in your text.

---

## 13) Troubleshooting Tips

- **Common errors**: unmatched braces, missing `\end{...}`, unknown command (typo or missing package), special characters not escaped.
- **References show `??`**: compile **twice** (or enable “auto” on Overleaf).
- **Image not found**: check filename, path, and that you omitted the extension in `\includegraphics{...}` (LaTeX picks the right one).
- **Table overruns page**: consider `tabularx`, `longtable`, or reduce column width / wrapping with `p{<width>}` columns.
- **Use the community**: TeX StackExchange, CTAN, Overleaf docs.
- **Make Smart Use of AI!**

---

## 14) *Multiple Files

LaTeX does not require the main file to be named `main.tex`. `main.tex` is simply a common convention for identifying the root document of a project.
**However, considering the readibility of your project, it's highly recommended to keep your roor document name as `main.tex`.**

For example, a big project which has the file structure as follow:

```text
LaTeX Project
│
├── main.tex          ← Root document
├── sections/
│   ├── intro.tex
│   ├── method.tex
│   └── results.tex
│
├── figures/
│   └── figure1.png
│
└── references.bib
```

Then in `main.tex`, you should include other files:

```latex
\documentclass{article}

\begin{document}

\input{intro}
\input{method}
\input{results}

\end{document}
```

## Appendix A: Starter Template (copy–paste)

```latex
\documentclass[12pt]{article}
\usepackage[utf8]{inputenc}
\usepackage{graphicx}
\usepackage{xcolor}
\usepackage[hidelinks]{hyperref}
\usepackage[a4paper,margin=1in]{geometry}
\usepackage{booktabs}
\usepackage{fancyhdr}
\pagestyle{fancy}
\fancyhead{} \fancyfoot{}
\fancyhead[L]{LaTeX Workshop} \fancyhead[R]{\thepage}

\title{LaTeX Workshop: No-Math Essentials}
\author{Your Name}
\date{\today}

\begin{document}
\maketitle
\tableofcontents

\section{Introduction}
Welcome to LaTeX! This handout covers non-math essentials for professional documents.

\section{Lists}
\subsection{Unordered}
\begin{itemize}
  \item Point A
  \item Point B
\end{itemize}

\subsection{Ordered}
\begin{enumerate}
  \item Step 1
  \item Step 2
\end{enumerate}

\section{Figures}
As shown in Figure~\ref{fig:sample}, images are first-class in \LaTeX.
\begin{figure}[h]
  \centering
  \includegraphics[width=0.6\textwidth]{example-image}
  \caption{An example image.}
  \label{fig:sample}
\end{figure}

\section{Tables}
See Table~\ref{tab:demo} for an example.
\begin{table}[h]
  \centering
  \begin{tabular}{lcr}
    \toprule
    Name & Desc & Value \\\midrule
    A & Alpha & 1.23 \\
    B & Beta  & 4.56 \\
    C & Gamma & 7.89 \\\bottomrule
  \end{tabular}
  \caption{A neat table.}
  \label{tab:demo}
\end{table}

\section{Footnotes and Links}
This is a footnote\footnote{Footnotes live at the bottom of the page.}. Visit the
\href{https://www.latex-project.org}{LaTeX Project} for more.

\end{document}
```

For more templates, you can find at https://www.overleaf.com/latex/templates.

---

## Appendix B: Handy Reference

- **Classes**: `article`, `report`, `book`, `letter`, `beamer`
- **Headings**: `\section`, `\subsection`, `\subsubsection`, `\paragraph`
- **Text**: `\textbf`, `\textit`, `\underline`, `\texttt`, `\textsc`, `\emph`
- **Lists**: `itemize`, `enumerate`, `description`
- **Figures**: `figure` + `\includegraphics`
- **Tables**: `table` + `tabular` (or `booktabs`)
- **Cross-refs**: `\label`, `\ref`, `\pageref`
- **Footnotes**: `\footnote{...}`
- **Links**: `\href{URL}{Text}`, `\url{URL}`
- **Layout**: `geometry`, `fancyhdr`, `setspace`
- **Fonts** (XeLaTeX/LuaLaTeX): `fontspec`
- **Color**: `xcolor`
- **Code**: `listings` or `minted`

---

### End of Worksheet — Happy TeXing!
