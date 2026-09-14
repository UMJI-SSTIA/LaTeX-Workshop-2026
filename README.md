# 📚 SSTIA LaTeX & Beamer Workshop

Welcome to the official repository for the **SJTU Global College SSTIA LaTeX Workshop**. This repository provides a quick reference and tutorial for setting up LaTeX, typesetting technical documents, formatting mathematics, using VS Code tools, and building Beamer presentation slides.

---

## 🚀 Quickstart

Clone this repository to get started with template files and examples:

```bash
git clone https://github.com/UMJI-SSTIA/LaTeX-Workshop-2026.git
cd LaTeX-Workshop-2026
```

---

## 🛠️ 1. LaTeX Intro & Setup

### Online: SJTU Cloud Overleaf
For zero-setup collaboration, use the SJTU cloud-based Overleaf instance:
* **URL:** [https://latex.sjtu.edu.cn/](https://latex.sjtu.edu.cn/)
* **Login:** Authenticate via SJTU **jAccount**.

### Local TeX Distributions
To compile locally on your machine, install a TeX distribution:

| OS | Distribution | Recommended Installation |
| :--- | :--- | :--- |
| **Windows / Linux / macOS** | **TeX Live** | Standard full installation (~7 GB) |
| **macOS** | **MacTeX** | Full Mac distribution based on TeX Live |
| **Windows** | **MiKTeX** | Lightweight alternative (downloads packages on-demand) |

---

## 📝 2. Basic Text, Figures & Tables

### Basic Document Structure

```latex
\documentclass[12pt, a4paper]{article}
\usepackage[utf8]{utf8}
\usepackage{amsmath, amssymb}
\usepackage{graphicx}
\usepackage{hyperref}

\title{SJTU SSTIA Research Report}
\author{Your Name}
\date{\today}

\begin{document}
\maketitle

\section{Introduction}
This is a basic paragraph in \LaTeX.

\end{document}
```

### Figures & Tables

```latex
% Including a Figure
\begin{figure}[htbp]
  \centering
  \includegraphics[width=0.7\linewidth]{figures/topology.png}
  \caption{Network Topology Overview}
  \label{fig:topology}
\end{figure}

% Creating a Table
\begin{table}[htbp]
  \centering
  \caption{Performance Benchmark}
  \label{tab:benchmark}
  \begin{tabular}{|l|c|r|}
    \hline
    \textbf{Method} & \textbf{Latency (ms)} & \textbf{Throughput} \\
    \hline
    Baseline & 12.4 & 10,000 \\
    Proposed & 4.2 & 32,500 \\
    \hline
  \end{tabular}
\end{table}
```

### Cross-Referencing & Bibliography
* **Reference targets:** Use `\ref{fig:topology}` or `\ref{tab:benchmark}`.
* **Citations:** Use `\cite{citation_key}` linked to a `.bib` reference file.

---

## 🔢 3. Math Syntax

LaTeX is the industry standard for mathematical notation.

### Inline vs. Display Math
* **Inline Math:** Enclose in `$ ... $` (e.g., $E = mc^2$).
* **Display Math:** Enclose in `$$ ... $$` or `\[ ... \]`:

$$
f(x) = \int_{-\infty}^{\infty} \hat{f}(\xi) e^{2\pi i x \xi} d\xi
$$

### Essential Formulas & Alignment

```latex
% Aligned Equations (amsmath)
\begin{align}
  \nabla \cdot \mathbf{E} &= \frac{\rho}{\varepsilon_0} \\
  \nabla \times \mathbf{E} &= -\frac{\partial \mathbf{B}}{\partial t}
\end{align}

% Matrices
\mathbf{A} = \begin{bmatrix}
  a_{11} & a_{12} \\
  a_{21} & a_{22}
\end{bmatrix}
```

---

## 🔌 4. Useful Tools & VS Code Extensions

- ### VS Code Setup
1. **LaTeX Workshop** (`James-Yu.latex-workshop`): Provides build recipes, auto-compilation on save, SyncTeX (jump between source and PDF), and PDF previewing.
2. **LaTeX Utilities** (`tecosaur.latex-utilities`): Offers word counts, live previews, and formatted text insertion.

- ### Key Shortcuts in VS Code

- ### Productivity Tools
  - Zotero + Better BibTeX

  - Detexify

  - Mathpix Snipping Tool

---

## 📊 5. Beamer

### Presentation Slides with Beamer

Create presentation slides using LaTeX Beamer syntax:

Complete Template ->`LaTeX-Workshop-2026/p3/temp`

---

*Hosted by SJTU Global College Student Science & Technology Innovation Association (SSTIA).*
