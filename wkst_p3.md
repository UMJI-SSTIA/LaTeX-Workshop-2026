# <center>📚 LaTeX Tools & Beamer Presentation Tutorial</center>

## <center>*SSTIA LaTeX Workshop 2026*</center>


## <span style="color: #2E86AB;">📦 Part 1: LaTeX Tools & VS Code Plugin Recommendations</span>

### <span style="color: #A23B72;">🔧 1.1 Essential LaTeX Distributions</span>

<table>
<tr>
<td width="33%" bgcolor="#E8F4F8">

#### **🐧 TeX Live** 
<span style="color: #06A77D;">✅ Recommended</span>

**Purpose**: Complete LaTeX distribution with all packages included

**Usage**: 
- 🔗 Download: https://www.tug.org/texlive/
- Install via command line or GUI installer
- Includes `pdflatex`, `xelatex`, `lualatex`

**✅ Pros**: 
- Comprehensive & cross-platform
- Regularly updated

**📦 Size**: ~7GB full installation

</td>
<td width="33%" bgcolor="#FFF4E6">

#### **🪟 MiKTeX**
<span style="color: #F18F01;">Windows-focused</span>

**Purpose**: Lightweight LaTeX with on-demand package installation

**Usage**:
- 🔗 Download: https://miktex.org/
- Auto-installs missing packages
- MiKTeX Console for management

**✅ Pros**: 
- Smaller initial download
- Windows-optimized

**⚠️ Cons**: Package installs can interrupt workflow

</td>
<td width="33%" bgcolor="#F0F8F0">

#### **☁️ SJTU Overleaf**
<span style="color: #5B9BD5;">Online Alternative</span>

**Purpose**: Cloud-based LaTeX editor (no local install)

**Usage**: 
- 🔗 Visit: https://latex.sjtu.edu.cn/project
- jAccount login & start writing

**✅ Pros**: 
- No setup required
- Real-time collaboration
- Version history

**⚠️ Cons**: Requires internet, not convenient to see real-time modification (must recomplie again and takes long)

</td>
</tr>
</table>

---

### <span style="color: #A23B72;">🔌 1.2 VS Code LaTeX Extensions</span>

<div style="background: linear-gradient(135deg, #6c87ff 0%, #e4c8ff 100%); padding: 20px; border-radius: 10px; color: white; margin: 20px 0;">

#### **⭐ LaTeX Workshop** <span style="background-color: #FFD700; color: #000; padding: 3px 8px; border-radius: 5px; font-size: 0.8em;">ESSENTIAL</span>

**Extension ID**: `James-Yu.latex-workshop`  
**Purpose**: Complete LaTeX development environment in VS Code

</div>

**🎯 Key Features**:

<table>
<tr>
<td bgcolor="#E8F5E9" width="50%">

**🔄 Auto-compilation**  
Compiles on save automatically

</td>
<td bgcolor="#E3F2FD" width="50%">

**📄 PDF Preview**  
Built-in preview with SyncTeX support

</td>
</tr>
<tr>
<td bgcolor="#FFF3E0">

**🎨 Syntax Highlighting**  
Color-coded LaTeX commands

</td>
<td bgcolor="#F3E5F5">

**💡 IntelliSense**  
Auto-completion for commands, citations

</td>
</tr>
<tr>
<td bgcolor="#FCE4EC" colspan="2">

**⚡ Snippet Support**  
Quick insertion of common structures

</td>
</tr>
</table>

**⚙️ Setup & Configuration**:

<div style="background-color: #263238; color: #AEDD94; padding: 15px; border-radius: 8px; border-left: 5px solid #4CAF50;">

```json
// Add to settings.json (Ctrl+Shift+P → "Open User Settings (JSON)")
{
  "latex-workshop.latex.autoBuild.run": "onSave",
  "latex-workshop.view.pdf.viewer": "tab",
  "latex-workshop.latex.recipe.default": "latexmk (xelatex)",
  "latex-workshop.synctex.afterBuild.enabled": true
}
```

</div>

**📋 Common Commands** (Access via Ctrl+Shift+P):

<table style="border-collapse: collapse; width: 100%;">
<tr style="background-color: #4A90E2; color: white;">
<td style="padding: 10px;"><strong>Command</strong></td>
<td style="padding: 10px;"><strong>Description</strong></td>
</tr>
<tr style="background-color: #E8F4F8;">
<td style="padding: 8px;">🔨 <code>LaTeX Workshop: Build LaTeX project</code></td>
<td style="padding: 8px;">Manual compilation</td>
</tr>
<tr style="background-color: #F5F5F5;">
<td style="padding: 8px;">👁️ <code>LaTeX Workshop: View LaTeX PDF</code></td>
<td style="padding: 8px;">Open preview</td>
</tr>
<tr style="background-color: #E8F4F8;">
<td style="padding: 8px;">🔗 <code>LaTeX Workshop: SyncTeX from cursor</code></td>
<td style="padding: 8px;">Jump to PDF location</td>
</tr>
<tr style="background-color: #F5F5F5;">
<td style="padding: 8px;">🧹 <code>LaTeX Workshop: Clean up auxiliary files</code></td>
<td style="padding: 8px;">Remove .aux, .log files</td>
</tr>
</table>

**⌨️ Useful Shortcuts**:

<div style="background: linear-gradient(to right, #FFC371, #FF5F6D); padding: 15px; border-radius: 8px; color: white;">

- `Ctrl+Alt+B` - 🔨 Build LaTeX project
- `Ctrl+Alt+V` - 👁️ View PDF
- `Ctrl+Alt+J` - 🔗 SyncTeX from cursor (source → PDF)
- `Ctrl+Click` in PDF - ↩️ SyncTeX reverse (PDF → source)

</div>

---

<div style="background-color: #F0F8FF; padding: 15px; border-radius: 10px; border-left: 5px solid #4169E1;">

#### **🛠️ LaTeX Utilities** <span style="background-color: #FFD700; color: #000; padding: 3px 8px; border-radius: 5px; font-size: 0.8em;">Enhanced Features</span>

- **Extension ID**: `tecosaur.latex-utilities`
- **Purpose**: Additional tools for LaTeX editing

**Features**:
- 📊 Live word count in status bar
- 📋 Formatted paste (converts plain text to LaTeX)
- 📚 Zotero citation integration
- 🎨 TikZ preview support

</div>

---

<div style="background-color: #FFE4E1; padding: 15px; border-radius: 10px; border-left: 5px solid #DC143C;">

#### **📄 PDF Preview** <span style="background-color: #E0E0E0; color: #000; padding: 3px 8px; border-radius: 5px; font-size: 0.8em;">Alternative Viewer</span>

- **Extension ID**: `tomoki1207.pdf`
- **Purpose**: Simple PDF viewer for VS Code
- **Usage**: Click PDF files in Explorer to view in VS Code tab
- **Note**: LaTeX Workshop has built-in viewer, but this is useful for general PDF viewing

</div>

---

### <span style="color: #A23B72;">🛠️ 1.3 Additional Useful Tools</span>

<table>
<tr>
<td width="50%" bgcolor="#E8F5E9" style="padding: 15px;">

#### **📚 Zotero + Better BibTeX**

**Purpose**: Reference management and `.bib` file generation

**Usage**: 
- 📥 Install Zotero desktop app
- 🔌 Install Better BibTeX plugin
- 📤 Export collections as `.bib` files
- ✍️ Use `\cite{}` commands with auto-completion in VS Code

</td>
<td width="50%" bgcolor="#E3F2FD" style="padding: 15px;">

#### **✏️ Detexify**

**Purpose**: Find LaTeX symbols by drawing

**Usage**: 
- 🌐 Visit http://detexify.kirelabs.org/classify.html
- ✏️ Draw symbol → Get LaTeX command

<span style="font-size: 2em;">∫ ∑ ∞ ≈ ≠ ≤</span>

</td>
</tr>
<tr>
<td bgcolor="#FFF3E0" style="padding: 15px;">

#### **📊 TeXCount**

**Purpose**: Word count for LaTeX documents

**Usage**: 
- 💻 Command line tool, or use LaTeX Utilities extension
- 🔢 Counts actual words, ignoring commands

</td>
<td bgcolor="#F3E5F5" style="padding: 15px;">

#### **🎨 Inkscape with TexText**

**Purpose**: Create complex diagrams with LaTeX labels

**Usage**: 
- 🖼️ Draw in Inkscape
- 🔤 Add LaTeX formulas via TexText plugin

</td>
</tr>
</table>

---

## <span style="color: #2E86AB;">🎬 Part 2: Beamer Presentation Tutorial</span>

### <span style="color: #D62828;">📖 2.1 What is Beamer?</span>

<div style="background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%); padding: 25px; border-radius: 15px; color: white; margin: 20px 0;">

**Beamer** is a LaTeX document class for creating presentations (slides). It produces PDF presentations that work on any platform without PowerPoint.

</div>

<table>
<tr>
<td width="50%" bgcolor="#D4EDDA" style="padding: 20px;">

### **✅ Advantages**

- 📐 Professional typesetting (especially for math)
- 🎯 Consistent formatting
- 🔄 Version control friendly (plain text)
- 💰 No licensing costs
- 🎛️ Precise control over layout

</td>
<td width="50%" bgcolor="#CCE5FF" style="padding: 20px;">

### **📌 When to use Beamer**

- 🔬 Academic presentations with equations
- 💻 Technical talks with code
- 🎓 Consistent multi-presenter conferences
- 📋 Reproducible presentation templates

</td>
</tr>
</table>

---

### <span style="color: #D62828;">📝 2.2 Basic Beamer Structure</span>

#### **💡 Minimal Example**

<div style="background-color: #263238; color: #AEDD94; padding: 15px; border-radius: 8px; border-left: 5px solid #FF6B6B;">

```latex
\documentclass{beamer}

% Theme selection
\usetheme{Madrid}
\usecolortheme{default}

% Title information
\title{Your Presentation Title}
\author{Your Name}
\institute{Your Institution}
\date{\today}

\begin{document}

% Title frame
\frame{\titlepage}

% Content frame
\begin{frame}
\frametitle{First Slide}
This is your first slide content.
\end{frame}

\end{document}
```

</div>

---

### <span style="color: #D62828;">🧩 2.3 Understanding Beamer Components</span>

#### **⚙️ Document Class Options**

<div style="background-color: #FFF9E6; padding: 15px; border-radius: 8px; border-left: 5px solid #FFB800;">

```latex
\documentclass[
  aspectratio=169,    % 16:9 ratio (default is 4:3)
  10pt,               % Font size: 8pt, 9pt, 10pt, 11pt, 12pt, 14pt, 17pt, 20pt
  handout,            % Removes overlays for handout printing
  t                   % Align frame content to top (default: c=center, b=bottom)
]{beamer}
```

</div>

<table style="width: 100%; border-collapse: collapse;">
<tr style="background-color: #4A90E2; color: white;">
<td style="padding: 10px;"><strong>Option</strong></td>
<td style="padding: 10px;"><strong>Purpose</strong></td>
</tr>
<tr style="background-color: #E8F4F8;">
<td style="padding: 8px;"><code>aspectratio=169</code></td>
<td style="padding: 8px;">🖥️ Modern widescreen format</td>
</tr>
<tr style="background-color: #F5F5F5;">
<td style="padding: 8px;"><code>10pt</code></td>
<td style="padding: 8px;">📏 Readable font size (11pt or 12pt for larger rooms)</td>
</tr>
<tr style="background-color: #E8F4F8;">
<td style="padding: 8px;"><code>handout</code></td>
<td style="padding: 8px;">🖨️ Creates printer-friendly version</td>
</tr>
<tr style="background-color: #F5F5F5;">
<td style="padding: 8px;"><code>t</code></td>
<td style="padding: 8px;">⬆️ Top alignment keeps content position consistent</td>
</tr>
</table>

---

#### **🎨 Themes and Appearance**

<div style="background: linear-gradient(to right, #fa709a 0%, #fee140 100%); padding: 20px; border-radius: 10px; color: white; margin: 20px 0;">

**Theme Types: Customize Your Presentation Look**

</div>

<table>
<tr>
<td width="33%" bgcolor="#FFE4E1" style="padding: 15px;">

**1️⃣ Presentation Themes** (overall look)

<div style="background-color: #263238; color: #AEDD94; padding: 10px; border-radius: 5px; margin-top: 10px;">

```latex
\usetheme{Madrid}
\usetheme{Berlin}
\usetheme{Copenhagen}
\usetheme{Singapore}
\usetheme{default}
```

</div>

📍 Navigation bar at top  
📂 Sidebar navigation  
🔵 Blue header with navigation  
✨ Minimal theme  
⚪ Plain theme

</td>
<td width="33%" bgcolor="#E0F2F7" style="padding: 15px;">

**2️⃣ Color Themes** (color scheme)

<div style="background-color: #263238; color: #AEDD94; padding: 10px; border-radius: 5px; margin-top: 10px;">

```latex
\usecolortheme{default}
\usecolortheme{dolphin}
\usecolortheme{rose}
\usecolortheme{beaver}
```

</div>

🎨 Default colors  
🐬 Blue tones  
🌹 Pink/red tones  
🦫 Gray and red


</td>
</tr>
</table>

<div style="background-color: #D4EDDA; padding: 15px; border-radius: 8px; border-left: 5px solid #28A745; margin-top: 15px;">

**💡 Popular Combination:**

```latex
\usetheme{Madrid}
\usecolortheme{whale}
```
Combination matrix (default mode): https://hartwork.org/beamer-theme-matrix/

**Purpose**: 
- **Presentation themes**: Define overall layout and navigation
- **Color themes**: Apply consistent color palette
- **Inner/Outer themes**: Customize specific elements

</div>

---

#### **📋 Title Frame Configuration**

<div style="background-color: #263238; color: #AEDD94; padding: 15px; border-radius: 8px; border-left: 5px solid #9C27B0;">

```latex
\title[Short Title]{Full Presentation Title That Can Be Long}
\subtitle{Optional Subtitle}
\author[Short Name]{Full Name \inst{1,2}}
\institute[University]{
  \inst{1} Department of Computer Science \\
  University Name \\
  \inst{2} Research Institute
}
\date[CONF 2026]{Conference Name, September 2026}
```

</div>

<table style="width: 100%; border-collapse: collapse; margin-top: 15px;">
<tr style="background-color: #7B1FA2; color: white;">
<td style="padding: 10px;"><strong>Short forms (in brackets)</strong></td>
<td style="padding: 10px;"><strong>Purpose</strong></td>
</tr>
<tr style="background-color: #F3E5F5;">
<td style="padding: 8px;">📌 Appear in footer/header</td>
<td style="padding: 8px;">Throughout presentation</td>
</tr>
<tr style="background-color: #E1BEE7;">
<td style="padding: 8px;">✨ Keep navigation bar uncluttered</td>
<td style="padding: 8px;">Better readability</td>
</tr>
<tr style="background-color: #F3E5F5;">
<td style="padding: 8px;">📄 Long versions</td>
<td style="padding: 8px;">Appear only on title slide</td>
</tr>
</table>

<div style="background-color: #E8F5E9; padding: 15px; border-radius: 8px; margin-top: 15px;">

**Creating title slide**:
```latex
\begin{frame}
  \titlepage
\end{frame}
```

</div>

---

### <span style="color: #D62828;">🎯 2.4 Creating Content Frames</span>

#### **📐 Basic Frame Structure**

<div style="background-color: #FFF3E0; padding: 15px; border-radius: 8px; border-left: 5px solid #FF9800;">

<div style="background-color: #263238; color: #AEDD94; padding: 10px; border-radius: 5px;">

```latex
\begin{frame}
  \frametitle{Frame Title}
  \framesubtitle{Optional Subtitle}
  
  Your content here.
\end{frame}
```

</div>

**Alternative syntax** (with automatic title):

<div style="background-color: #263238; color: #AEDD94; padding: 10px; border-radius: 5px; margin-top: 10px;">

```latex
\begin{frame}{Frame Title}{Optional Subtitle}
  Content here.
\end{frame}
```

</div>

</div>

---

#### **🔒 Fragile Frames** (for verbatim content)

<div style="background-color: #FFEBEE; padding: 15px; border-radius: 8px; border-left: 5px solid #F44336;">

<div style="background-color: #263238; color: #AEDD94; padding: 10px; border-radius: 5px;">

```latex
\begin{frame}[fragile]
  \frametitle{Code Example}
  
  \begin{verbatim}
    def hello_world():
        print("Hello, World!")
  \end{verbatim}
\end{frame}
```

</div>

**⚠️ Purpose**: `[fragile]` option required when frame contains:
- ✅ `\verb` or `verbatim` environments
- 💻 Code listings
- 🔤 Special characters that need literal interpretation

**❌ Without `[fragile]`**: LaTeX compilation errors occur

</div>

---

#### **🎬 Plain Frames** (no header/footer)

<div style="background-color: #E8EAF6; padding: 15px; border-radius: 8px; border-left: 5px solid #3F51B5;">

<div style="background-color: #263238; color: #AEDD94; padding: 10px; border-radius: 5px;">

```latex
\begin{frame}[plain]
  \centering
  \Huge Thank You!
\end{frame}
```

</div>

**🎯 Purpose**: Full-screen content without theme decorations  
**📌 Use cases**: Title slides, image-only slides, thank you slides

</div>

---

### <span style="color: #D62828;">📊 2.5 Structuring Content</span>

#### **📝 Lists**

<div style="background-color: #F1F8E9; padding: 15px; border-radius: 8px; border-left: 5px solid #8BC34A;">

<div style="background-color: #263238; color: #AEDD94; padding: 10px; border-radius: 5px;">

```latex
\begin{frame}{Lists Example}
  
  \textbf{Itemize (bullets):}
  \begin{itemize}
    \item First point
    \item Second point
      \begin{itemize}
        \item Nested point
      \end{itemize}
  \end{itemize}
  
  \textbf{Enumerate (numbers):}
  \begin{enumerate}
    \item First step
    \item Second step
  \end{enumerate}
  
\end{frame}
```

</div>

**🎨 Customizing bullets**:

<div style="background-color: #263238; color: #AEDD94; padding: 10px; border-radius: 5px; margin-top: 10px;">

```latex
\setbeamertemplate{itemize items}[circle]  % or [square], [triangle]
\setbeamertemplate{enumerate items}[default]  % or [circle], [square]
```

</div>

</div>

---

#### **📐 Columns Layout**

<div style="background-color: #E1F5FE; padding: 15px; border-radius: 8px; border-left: 5px solid #03A9F4;">

<div style="background-color: #263238; color: #AEDD94; padding: 10px; border-radius: 5px;">

```latex
\begin{frame}{Two-Column Layout}
  
  \begin{columns}
    \begin{column}{0.5\textwidth}
      Left column content:
      \begin{itemize}
        \item Point 1
        \item Point 2
      \end{itemize}
    \end{column}
    
    \begin{column}{0.5\textwidth}
      Right column content:
      \includegraphics[width=\textwidth]{image.png}
    \end{column}
  \end{columns}
  
\end{frame}
```

</div>

<table style="width: 100%; margin-top: 15px;">
<tr>
<td width="50%" bgcolor="#B3E5FC" style="padding: 15px;">

**🎯 Purpose**: 
- Side-by-side content presentation
- Compare/contrast layouts
- Image alongside text

</td>
<td width="50%" bgcolor="#81D4FA" style="padding: 15px;">

**⚙️ Options**:
- `0.5\textwidth` = 50% width per column
- `[T]` = Top align columns
- `[c]` = Center align (default)

</td>
</tr>
</table>

</div>

---

#### **📦 Blocks** (Highlighted Sections)

<div style="background-color: #FFF8E1; padding: 15px; border-radius: 8px; border-left: 5px solid #FFC107;">

<div style="background-color: #263238; color: #AEDD94; padding: 10px; border-radius: 5px;">

```latex
\begin{frame}{Block Examples}
  
  \begin{block}{Block Title}
    Standard block with theme colors.
  \end{block}
  
  \begin{alertblock}{Warning}
    Important alert (usually red).
  \end{alertblock}
  
  \begin{exampleblock}{Example}
    Example block (usually green).
  \end{exampleblock}
  
\end{frame}
```

</div>

<table style="width: 100%; margin-top: 15px;">
<tr>
<td width="33%" bgcolor="#E3F2FD" style="padding: 10px; text-align: center;">

**📘 block**  
Standard block

</td>
<td width="33%" bgcolor="#FFEBEE" style="padding: 10px; text-align: center;">

**⚠️ alertblock**  
Warning (red)

</td>
<td width="33%" bgcolor="#E8F5E9" style="padding: 10px; text-align: center;">

**✅ exampleblock**  
Example (green)

</td>
</tr>
</table>

**🎨 Customization**:

<div style="background-color: #263238; color: #AEDD94; padding: 10px; border-radius: 5px; margin-top: 10px;">

```latex
\setbeamercolor{block title}{bg=blue!20, fg=black}
\setbeamercolor{block body}{bg=blue!5}
```

</div>

</div>

---

### <span style="color: #D62828;">✨ 2.6 Overlays and Animations</span>

<div style="background: linear-gradient(to right, #fa709a 0%, #fee140 100%); padding: 20px; border-radius: 10px; color: white; margin: 20px 0;">

**Overlays reveal content progressively, creating animation effects in PDF.**

</div>

#### **🎬 Basic Overlay Syntax**

<div style="background-color: #F3E5F5; padding: 15px; border-radius: 8px; border-left: 5px solid #9C27B0;">

<div style="background-color: #263238; color: #AEDD94; padding: 10px; border-radius: 5px;">

```latex
\begin{frame}{Overlay Basics}
  
  \begin{itemize}
    \item<1-> Appears on slide 1 and after
    \item<2-> Appears on slide 2 and after
    \item<3-> Appears on slide 3 and after
    \item<1-2> Appears only on slides 1-2
    \item<4> Appears only on slide 4
  \end{itemize}
  
\end{frame}
```

</div>

**📋 Overlay Specifications**:

<table style="width: 100%; border-collapse: collapse; margin-top: 15px;">
<tr style="background-color: #7B1FA2; color: white;">
<td style="padding: 10px;"><strong>Syntax</strong></td>
<td style="padding: 10px;"><strong>Effect</strong></td>
</tr>
<tr style="background-color: #F3E5F5;">
<td style="padding: 8px;"><code>&lt;n&gt;</code></td>
<td style="padding: 8px;">⚫ Appears only on slide n</td>
</tr>
<tr style="background-color: #E1BEE7;">
<td style="padding: 8px;"><code>&lt;n-&gt;</code></td>
<td style="padding: 8px;">➡️ Appears from slide n onwards</td>
</tr>
<tr style="background-color: #F3E5F5;">
<td style="padding: 8px;"><code>&lt;n-m&gt;</code></td>
<td style="padding: 8px;">↔️ Appears on slides n through m</td>
</tr>
<tr style="background-color: #E1BEE7;">
<td style="padding: 8px;"><code>&lt;-n&gt;</code></td>
<td style="padding: 8px;">⬅️ Appears up to slide n</td>
</tr>
</table>

**🎯 Purpose**: Control when each element appears during presentation

</div>

---

#### **⏸️ Pause Command** (Simple Sequential Reveals)

<div style="background-color: #E8F5E9; padding: 15px; border-radius: 8px; border-left: 5px solid #4CAF50;">

<div style="background-color: #263238; color: #AEDD94; padding: 10px; border-radius: 5px;">

```latex
\begin{frame}{Using Pause}
  
  First point appears immediately.
  \pause
  
  Second point appears after click.
  \pause
  
  \begin{itemize}
    \item This list appears third
    \item All items together
  \end{itemize}
  \pause
  
  Final content.
  
\end{frame}
```

</div>

<table style="width: 100%; margin-top: 15px;">
<tr>
<td width="50%" bgcolor="#C8E6C9" style="padding: 15px;">

**✅ Purpose**: Simplest way to create step-by-step reveals

</td>
<td width="50%" bgcolor="#FFCCBC" style="padding: 15px;">

**⚠️ Limitation**: Less control than explicit overlay numbers

</td>
</tr>
</table>

</div>

---

#### **🎨 Alert and Emphasis**

<div style="background-color: #FFF3E0; padding: 15px; border-radius: 8px; border-left: 5px solid #FF9800;">

<div style="background-color: #263238; color: #AEDD94; padding: 10px; border-radius: 5px;">

```latex
\begin{frame}{Highlighting Content}
  
  \begin{itemize}
    \item<1-> Regular item
    \item<2-> \alert<2>{This is highlighted on slide 2}
    \item<3-> \textbf<3>{Bold on slide 3, normal after}
  \end{itemize}
  
  \onslide<4->{
    This paragraph appears from slide 4 onwards.
  }
  
  \only<5>{
    This text ONLY on slide 5, doesn't occupy space otherwise.
  }
  
\end{frame}
```

</div>

**📊 Differences**:

<table style="width: 100%; border-collapse: collapse; margin-top: 15px;">
<tr style="background-color: #FF9800; color: white;">
<td style="padding: 10px;"><strong>Command</strong></td>
<td style="padding: 10px;"><strong>Behavior</strong></td>
</tr>
<tr style="background-color: #FFE0B2;">
<td style="padding: 8px;"><code>\alert&lt;n&gt;{text}</code></td>
<td style="padding: 8px;">🔴 Highlights in alert color on slide n</td>
</tr>
<tr style="background-color: #FFCC80;">
<td style="padding: 8px;"><code>\onslide&lt;n-&gt;{content}</code></td>
<td style="padding: 8px;">👁️ Shows content, reserves space when hidden</td>
</tr>
<tr style="background-color: #FFE0B2;">
<td style="padding: 8px;"><code>\only&lt;n&gt;{content}</code></td>
<td style="padding: 8px;">⚡ Shows content, no space reservation when hidden</td>
</tr>
</table>

</div>

---

#### **🔬 Advanced: Overlay-Aware Commands**

<div style="background-color: #E0F2F1; padding: 15px; border-radius: 8px; border-left: 5px solid #009688;">

<div style="background-color: #263238; color: #AEDD94; padding: 10px; border-radius: 5px;">

```latex
\begin{frame}{Table of Contents with Highlights}
  
  \tableofcontents[pausesections]  % Highlight each section progressively
  
\end{frame}

\begin{frame}{Mathematical Reveals}
  
  Consider the equation:
  \begin{align*}
    E &= mc^2 \onslide<2->{\\
      &= m \cdot (3 \times 10^8)^2} \onslide<3->{\\
      &\approx 9 \times 10^{16} m \text{ joules}}
  \end{align*}
  
\end{frame}
```

</div>

</div>

---

### <span style="color: #D62828;">🖼️ 2.7 Including Graphics and Media</span>

#### **📷 Images**

<div style="background-color: #E8EAF6; padding: 15px; border-radius: 8px; border-left: 5px solid #3F51B5;">

<div style="background-color: #263238; color: #AEDD94; padding: 10px; border-radius: 5px;">

```latex
\begin{frame}{Including Images}
  
  \begin{figure}
    \centering
    \includegraphics[width=0.6\textwidth]{figures/diagram.png}
    \caption{Image caption}
  \end{figure}
  
\end{frame}
```

</div>

**⚙️ Common options**:

<table style="width: 100%; margin-top: 15px;">
<tr>
<td width="50%" bgcolor="#C5CAE9" style="padding: 10px;">

📏 `width=0.8\textwidth` - Scale to 80% of text width  
📐 `height=5cm` - Fixed height

</td>
<td width="50%" bgcolor="#9FA8DA" style="padding: 10px;">

🔄 `scale=0.5` - Scale to 50%  
🔃 `angle=90` - Rotate 90 degrees

</td>
</tr>
</table>

**📦 Required package**:
```latex
\usepackage{graphicx}  % Usually included in beamer by default
```

</div>

---

#### **🎨 TikZ Graphics** (Vector Diagrams)

<div style="background-color: #FCE4EC; padding: 15px; border-radius: 8px; border-left: 5px solid #E91E63;">

<div style="background-color: #263238; color: #AEDD94; padding: 10px; border-radius: 5px;">

```latex
\begin{frame}{TikZ Diagram}
  
  \begin{tikzpicture}
    \node[circle, draw, fill=blue!20] (A) at (0,0) {A};
    \node[circle, draw, fill=red!20] (B) at (3,0) {B};
    \draw[->] (A) -- (B);
  \end{tikzpicture}
  
\end{frame}
```

</div>

<table style="width: 100%; margin-top: 15px;">
<tr>
<td width="50%" bgcolor="#F8BBD0" style="padding: 15px;">

**✅ Advantages**: 
- Perfect integration
- Scalable
- Editable

</td>
<td width="50%" bgcolor="#F48FB1" style="padding: 15px;">

**📦 Required package**:
```latex
\usepackage{tikz}
```

</td>
</tr>
</table>

**🎯 Purpose**: Create diagrams directly in LaTeX

</div>

---

### <span style="color: #D62828;">🧭 2.8 Table of Contents and Navigation</span>

#### **📑 Automatic Table of Contents**

<div style="background-color: #E3F2FD; padding: 15px; border-radius: 8px; border-left: 5px solid #2196F3;">

<div style="background-color: #263238; color: #AEDD94; padding: 10px; border-radius: 5px;">

```latex
\begin{frame}{Outline}
  \tableofcontents
\end{frame}
```

</div>

**🎯 Purpose**: Auto-generates from `\section` and `\subsection` commands

</div>

---

#### **📚 Using Sections**

<div style="background-color: #F3E5F5; padding: 15px; border-radius: 8px; border-left: 5px solid #9C27B0;">

<div style="background-color: #263238; color: #AEDD94; padding: 10px; border-radius: 5px;">

```latex
\section{Introduction}

\begin{frame}{Introduction Slide}
  Content here.
\end{frame}

\subsection{Background}

\begin{frame}{Background Details}
  More content.
\end{frame}

\section{Methods}
% ... more frames
```

</div>

**🎯 Purpose**: 

<table style="width: 100%; margin-top: 15px;">
<tr>
<td width="50%" bgcolor="#E1BEE7" style="padding: 10px;">

✅ Creates logical structure  
📋 Populates table of contents

</td>
<td width="50%" bgcolor="#CE93D8" style="padding: 10px;">

🧭 Appears in navigation bars  
📊 Organizes presentation hierarchy

</td>
</tr>
</table>

</div>

---

#### **🎯 Highlighted TOC Per Section**

<div style="background-color: #FFF3E0; padding: 15px; border-radius: 8px; border-left: 5px solid #FF9800;">

<div style="background-color: #263238; color: #AEDD94; padding: 10px; border-radius: 5px;">

```latex
\AtBeginSection[]{
  \begin{frame}{Outline}
    \tableofcontents[currentsection]
  \end{frame}
}
```

</div>

**🎯 Purpose**: Automatically shows TOC at start of each section, highlighting current section  
**✨ Effect**: Helps audience track presentation progress

</div>

---

### <span style="color: #D62828;">🎨 2.9 Common Customizations</span>

<table>
<tr>
<td width="50%" bgcolor="#E8F5E9" style="padding: 15px;">

#### **🚫 Removing Navigation Symbols**

<div style="background-color: #263238; color: #AEDD94; padding: 10px; border-radius: 5px; margin-top: 10px;">

```latex
\setbeamertemplate{navigation symbols}{}
```

</div>

**🎯 Purpose**: Clean up footer (default navigation dots often unused)

</td>
<td width="50%" bgcolor="#E3F2FD" style="padding: 15px;">

#### **📊 Custom Footer**

<div style="background-color: #263238; color: #AEDD94; padding: 10px; border-radius: 5px; margin-top: 10px;">

```latex
\setbeamertemplate{footline}{
  \hfill\insertframenumber/\inserttotalframenumber\hspace{2mm}\vskip2mm
}
```

</div>

**🎯 Purpose**: Simple "slide X of Y" counter

</td>
</tr>
<tr>
<td bgcolor="#FFF3E0" style="padding: 15px;">

#### **🎨 Custom Colors**

<div style="background-color: #263238; color: #AEDD94; padding: 10px; border-radius: 5px; margin-top: 10px;">

```latex
\definecolor{myblue}{RGB}{0,102,204}
\setbeamercolor{structure}{fg=myblue}
\setbeamercolor{frametitle}{bg=myblue, fg=white}
```

</div>

**🎯 Purpose**: Match institutional or personal branding

</td>
<td bgcolor="#F3E5F5" style="padding: 15px;">

#### **🔤 Font Sizes**

<div style="background-color: #263238; color: #AEDD94; padding: 10px; border-radius: 5px; margin-top: 10px;">

```latex
\setbeamerfont{frametitle}{size=\Large, series=\bfseries}
\setbeamerfont{title}{size=\huge}
```

</div>

</td>
</tr>
</table>

---

### <span style="color: #D62828;">📋 2.10 Complete Example Template</span>

<div style="background: linear-gradient(135deg, #667eea 0%, #764ba2 100%); padding: 20px; border-radius: 10px; color: white; margin: 20px 0;">

**✨ Complete template attached in repo - copy and use!**

</div>

---

### <span style="color: #D62828;">⚙️ 2.11 Compiling Your Beamer Presentation</span>

<table>
<tr>
<td width="50%" bgcolor="#E8F5E9" style="padding: 20px;">

#### **🖥️ Using VS Code with LaTeX Workshop**

1. 💾 Save your `.tex` file
2. 🔄 LaTeX Workshop auto-compiles on save
3. 👁️ View PDF in side panel
4. 🔗 Use SyncTeX (Ctrl+Click) to navigate

</td>
<td width="50%" bgcolor="#E3F2FD" style="padding: 20px;">

#### **💻 Command Line**

<div style="background-color: #263238; color: #AEDD94; padding: 10px; border-radius: 5px; margin-top: 10px;">

```bash
pdflatex presentation.tex
pdflatex presentation.tex  # Run twice for TOC
```

</div>

</td>
</tr>
</table>

<div style="background-color: #FFF3E0; padding: 15px; border-radius: 8px; border-left: 5px solid #FF9800; margin-top: 15px;">

**📚 For bibliography**:

<div style="background-color: #263238; color: #AEDD94; padding: 10px; border-radius: 5px; margin-top: 10px;">

```bash
pdflatex presentation.tex
bibtex presentation
pdflatex presentation.tex
pdflatex presentation.tex
```

</div>

</div>

---

### <span style="color: #D62828;">✅ 2.12 Beamer Best Practices</span>

<table>
<tr>
<td width="50%" bgcolor="#E8F5E9" style="padding: 15px;">

**1️⃣ Keep slides simple**  
One main idea per slide

**2️⃣ Use overlays sparingly**  
Too many clicks interrupt flow

**3️⃣ Consistent theme**  
Choose one theme and stick with it

**4️⃣ Readable fonts**  
11pt or 12pt for large rooms

</td>
<td width="50%" bgcolor="#E3F2FD" style="padding: 15px;">

**5️⃣ High contrast**  
Ensure text visible from back of room

**6️⃣ Test presentation mode**  
PDF readers handle overlays differently

**7️⃣ Backup**  
Bring PDF on USB drive (works everywhere)

**8️⃣ Practice**  
Run through with actual PDF reader you'll use

</td>
</tr>
</table>

---

### <span style="color: #D62828;">🔧 2.13 Troubleshooting Common Issues</span>

<table style="width: 100%;">
<tr>
<td bgcolor="#FFEBEE" style="padding: 15px;">

**❌ Issue**: "Undefined control sequence" error

<div style="background-color: #C8E6C9; padding: 10px; border-radius: 5px; margin-top: 10px;">

**✅ Solution**: Check for typos in commands, ensure packages loaded

</div>

</td>
</tr>
<tr>
<td bgcolor="#FFF3E0" style="padding: 15px;">

**❌ Issue**: Overlays not working

<div style="background-color: #C8E6C9; padding: 10px; border-radius: 5px; margin-top: 10px;">

**✅ Solution**: 
- Verify using PDF reader that supports overlays (Adobe, Okular)
- Some viewers show all overlays at once

</div>

</td>
</tr>
<tr>
<td bgcolor="#E3F2FD" style="padding: 15px;">

**❌ Issue**: Images not appearing

<div style="background-color: #C8E6C9; padding: 10px; border-radius: 5px; margin-top: 10px;">

**✅ Solution**: 
- Check file path, use forward slashes
- Ensure image in correct directory
- Add `\graphicspath{{./figures/}}` to preamble

</div>

</td>
</tr>
<tr>
<td bgcolor="#F3E5F5" style="padding: 15px;">

**❌ Issue**: Frame content overflow

<div style="background-color: #C8E6C9; padding: 10px; border-radius: 5px; margin-top: 10px;">

**✅ Solution**: 
- Use `\small` or `\footnotesize` to reduce font size
- Split content across multiple frames

</div>

</td>
</tr>
<tr>
<td bgcolor="#E8F5E9" style="padding: 15px;">

**❌ Issue**: Bibliography not showing

<div style="background-color: #C8E6C9; padding: 10px; border-radius: 5px; margin-top: 10px;">

**✅ Solution**: 
- Use `\begin{frame}[allowframebreaks]{References}` for long bibliographies
- Run bibtex compilation sequence

</div>

</td>
</tr>
</table>

---

### <span style="color: #D62828;">📚 2.14 Additional Resources</span>

<table>
<tr>
<td width="50%" bgcolor="#E8F5E9" style="padding: 20px;">

**📖 Documentation & Tutorials**

- 📘 **Beamer Documentation**: `texdoc beamer` (command line)
- 🌐 **CTAN**: https://ctan.org/pkg/beamer
- 🎓 **Overleaf Tutorial**: https://www.overleaf.com/learn/latex/Beamer

</td>
<td width="50%" bgcolor="#E3F2FD" style="padding: 20px;">

**🎨 Theme Galleries & Help**

- 🖼️ **Theme Gallery**: https://deic.uab.cat/~iblanes/beamer_gallery/
- 💬 **Stack Exchange**: https://tex.stackexchange.com/
- ❓ Q&A for LaTeX issues

</td>
</tr>
</table>

---
<!--
## <span style="color: #2E86AB;">🎯 Practice Exercises</span>

<div style="background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%); padding: 20px; border-radius: 10px; color: white; margin: 20px 0;">

**Complete these exercises to master LaTeX and Beamer!**

</div>

<table>
<tr>
<td width="20%" bgcolor="#FFCDD2" style="padding: 15px; text-align: center;">

**1️⃣**

Setup Task

</td>
<td bgcolor="#FFEBEE" style="padding: 15px;">

Install TeX Live and LaTeX Workshop, create a test document

</td>
</tr>
<tr>
<td width="20%" bgcolor="#F8BBD0" style="padding: 15px; text-align: center;">

**2️⃣**

Basic Beamer

</td>
<td bgcolor="#FCE4EC" style="padding: 15px;">

Create 5-slide presentation with title, TOC, and 3 content slides

</td>
</tr>
<tr>
<td width="20%" bgcolor="#E1BEE7" style="padding: 15px; text-align: center;">

**3️⃣**

Overlays

</td>
<td bgcolor="#F3E5F5" style="padding: 15px;">

Create slide with 4 bullet points revealing sequentially

</td>
</tr>
<tr>
<td width="20%" bgcolor="#C5CAE9" style="padding: 15px; text-align: center;">

**4️⃣**

Columns

</td>
<td bgcolor="#E8EAF6" style="padding: 15px;">

Create slide with text on left, image on right

</td>
</tr>
<tr>
<td width="20%" bgcolor="#BBDEFB" style="padding: 15px; text-align: center;">

**5️⃣**

Customization

</td>
<td bgcolor="#E3F2FD" style="padding: 15px;">

Change theme colors to match your institution's branding

</td>
</tr>
</table>

---
-->
## <span style="color: #2E86AB;">📌 Quick Reference Card</span>

<div style="background: linear-gradient(to right, #56CCF2, #2F80ED); padding: 20px; border-radius: 10px; color: white; margin: 20px 0;">

### **Essential Shortcuts & Commands**

</div>

<table>
<tr>
<td width="50%" bgcolor="#E8F4F8" style="padding: 20px;">

### **⌨️ VS Code Shortcuts**

<div style="background-color: #263238; color: #AEDD94; padding: 10px; border-radius: 5px; margin-top: 10px;">

- `Ctrl+Alt+B` - 🔨 Build LaTeX
- `Ctrl+Alt+V` - 👁️ View PDF
- `Ctrl+Alt+J` - 🔗 Jump to PDF location

</div>

</td>
<td width="50%" bgcolor="#FFF9E6" style="padding: 20px;">

### **📋 Essential Beamer Commands**

<div style="background-color: #263238; color: #AEDD94; padding: 10px; border-radius: 5px; margin-top: 10px;">

```latex
\begin{frame}{Title}         % Create frame
\pause                       % Sequential reveal
\item<2->                    % Appears from slide 2
\alert<3>{text}              % Highlight on slide 3
\begin{columns}...\end{columns}  % Multi-column layout
```

</div>

</td>
</tr>
<tr>
<td bgcolor="#F0F8F0" style="padding: 20px;" colspan="2">

### **🎨 Theme Selection**

<div style="background-color: #263238; color: #AEDD94; padding: 10px; border-radius: 5px; margin-top: 10px;">

```latex
\usetheme{Madrid}            % Professional theme
\usecolortheme{whale}        % Color scheme
```

</div>

</td>
</tr>
</table>

---

<div align="center" style="background: linear-gradient(135deg, #667eea 0%, #764ba2 100%); padding: 30px; border-radius: 15px; color: white; margin: 30px 0;">

## 🎉 **The End** 🎉

**Good luck with your Beamer presentations! 🚀**

### *Welcome to SSTIA!*

</div>
