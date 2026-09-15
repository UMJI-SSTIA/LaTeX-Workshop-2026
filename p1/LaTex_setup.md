# LaTeX Setup Guide

There are two common ways to set up a LaTeX environment:

1. **Overleaf** — Online LaTeX environment
2. **VS Code** — Local LaTeX environment

---

## 1. Overleaf

### Configuration

Overleaf is a browser-based LaTeX editor. No local LaTeX installation is required.

#### Step 1: Create an Overleaf Account

Go to [SJTU_Overleaf](https://latex.sjtu.edu.cn/login) and use JAccount to sign in.


#### Step 2: Create a Project

After logging in:

```text
New Project → Blank Project
```

Give the project a name and create it.

#### Step 3: Edit the `.tex` File

Overleaf automatically creates a main `.tex` file. For example:

```latex
\documentclass{article}

\title{LaTex wksp}
\author{Your name}
\date{\today}

\begin{document}

\maketitle

\section{Introduction}

\end{document}
```

#### Step 4: Compile

Click **Recompile** to compile the document and generate the PDF.

The PDF preview will appear directly in the Overleaf interface.

**Note**: For Chinese character, use `XeLaTex` compiler and add `\usepackage{ctex}`

How to Select the Compiler in Overleaf:

1. Open your Overleaf project.
2. Click Menu in the top-left corner.
3. Find Compiler.
4. Change the compiler from:
`pdfLaTeX` to `XeLaTeX`
5. Close the menu and click Recompile.

``` latex
\documentclass{article}
\usepackage{ctex}

\title{中文 title}
\author{Your name }
\date{\today}

\begin{document}

\maketitle

\section{Introduction}

\end{document}
```

## 2. VS Code

### Configuration

A local LaTeX environment requires:

```text
VS Code
    +
LaTeX Workshop (Extension in VSCode)
    +
LaTeX Distribution (Download from Official website)
```

For Windows, **MiKTeX** or **TeX Live** can be used as the LaTeX distribution.

### Step 1: Install VS Code

Download and install [Visual Studio Code](https://code.visualstudio.com/).

### Step 2: Install a LaTeX Distribution

Choose one of the following:

* [MiKTeX](https://miktex.org/download) — relatively lightweight and beginner-friendly
* [TeX Live](https://www.tug.org/texlive/) — more comprehensive and includes a large collection of LaTeX packages

Install the selected distribution using its default settings unless you have specific requirements.

### Step 3: Install LaTeX Workshop

Open VS Code and go to:

```text
Extensions → Search "LaTeX Workshop"
```

Install **LaTeX Workshop** by James Yu.

### Step 4: Create a `.tex` File

Create a file named:

```text
main.tex
```

For example:

```latex
\documentclass{article}

\begin{document}

Hello, LaTeX!

\section{Introduction}

This is my first LaTeX document.

\end{document}
```

### Step 5: Compile

Open `main.tex` in VS Code and use the **Build LaTeX project** command provided by LaTeX Workshop.

The generated PDF can be viewed directly in VS Code.

---

# 3. Comparison

| Feature                   | Overleaf                                 | VS Code + Local LaTeX                                     |
| ------------------------- | ---------------------------------------- | --------------------------------------------------------- |
| **Setup difficulty**      | ⭐ Very easy                              | ⭐⭐⭐ More complicated                                      |
| **Offline work**          | ❌                                        | ✅                                                         |
| **Customization**         | Limited                                  | Highly customizable                                       |
| **Package management**    | Managed by Overleaf                      | User-managed                                              |
| **Cross-device access**   | ⭐⭐⭐⭐⭐ Excellent                          | ⭐⭐⭐ Requires environment setup                            |
| **Multiple user**   | ✅ | ❌ |

