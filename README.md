<!---
{
  "id": "fc36b61a-a948-4971-87b1-dcf98a1c5d80",
  "teaches": "Creating Tables in LaTeX",
  "depends_on": ["00650b50-14de-471d-a347-246f47ffadde"],
  "author": "Stephan Bökelmann",
  "first_used": "2025-06-02",
  "keywords": ["LaTeX", "tables", "tabular", "vim", "compilation"]
}
--->

# Creating Tables in LaTeX

> In this exercise you will learn how to create and format basic tables using the `tabular` environment in LaTeX. Furthermore we will explore column alignment, borders, and simple styling options.

### Introduction

Tables are essential for presenting structured data clearly and compactly. In LaTeX, tables are created using the `tabular` environment, which gives you full control over column alignment, borders, and spacing. Unlike word processors that allow you to draw tables visually, LaTeX requires you to define the structure and content explicitly in code.

The `tabular` environment is initiated with `\begin{tabular}{...}` where the argument specifies column formatting. Each column is defined by a character:

* `l` for left-aligned
* `c` for centered
* `r` for right-aligned
* `|` to insert vertical lines

Rows are separated by `\\` and columns by `&`. Horizontal lines can be added using `\hline`. This approach allows precise, repeatable, and predictable table layouts that integrate well with LaTeX's overall philosophy of content-presentation separation.

Although LaTeX tables may seem verbose at first, their explicit structure becomes very powerful when creating professional documents that require consistent formatting. Mastering tables now will prepare you for more advanced topics such as floating tables, longtables, multirow, multicolumn, and tables in academic journal templates.

In this exercise, you will build several tables of increasing complexity to become comfortable with this crucial feature of LaTeX.

### Further Readings and Other Sources

* [Overleaf: Tables](https://www.overleaf.com/learn/latex/Tables)
* [LaTeX Wikibook - Tables](https://en.wikibooks.org/wiki/LaTeX/Tables)
* [LaTeX Tables YouTube Tutorial](https://www.youtube.com/watch?v=oA2H4yrKcjs)
* [The LaTeX Companion (Book)](https://doi.org/10.1007/978-3-319-27232-5)

---

## Tasks

### Task 0: Create a New LaTeX File

Open Vim and create a new file:

```bash
vim tables.tex
```

Insert the following base structure:

```latex
\documentclass{article}
\begin{document}

Your content goes here.

\end{document}
```

Save and exit Vim.

### Task 1: Create a Simple Table Without Borders

Replace `Your content goes here.` with:

```latex
\section{Simple Table}

\begin{tabular}{lcr}
Name & Age & Country \\
Alice & 30 & USA \\
Bob & 25 & Canada \\
Charlie & 35 & UK \\
\end{tabular}
```

Compile with:

```bash
pdflatex tables.tex
```

Observe how the data is aligned based on the column specifiers: left (`l`), center (`c`), and right (`r`).

### Task 2: Add Borders to the Table

Modify the table to include vertical and horizontal lines:

```latex
\section{Table with Borders}

\begin{tabular}{|l|c|r|}
\hline
Name & Age & Country \\
\hline
Alice & 30 & USA \\
Bob & 25 & Canada \\
Charlie & 35 & UK \\
\hline
\end{tabular}
```

Recompile and verify that the borders are displayed.

### Task 3: Add a Caption and Centering

Tables are often centered and given captions to improve readability.

```latex
\section{Formatted Table}

\begin{center}
\begin{tabular}{|l|c|r|}
\hline
Name & Age & Country \\
\hline
Alice & 30 & USA \\
Bob & 25 & Canada \\
Charlie & 35 & UK \\
\hline
\end{tabular}
\end{center}
```

Alternatively, you can also use the `table` environment for better placement control (will be covered in future exercises).

### Task 4: Create a Table with Multiline Headers

```latex
\section{Advanced Table}

\begin{tabular}{|l|c|r|}
\hline
\textbf{Name} & \textbf{Age} & \textbf{Country} \\
\hline
Alice & 30 & USA \\
Bob & 25 & Canada \\
Charlie & 35 & UK \\
\hline
\end{tabular}
```

Compile and verify that headers are bold.

---

## Questions

1. What does the argument to the `tabular` environment specify?
2. How does LaTeX distinguish between columns and rows?
3. How can you add horizontal and vertical lines in a table?
4. Why might you want to use the `table` environment instead of just `tabular`?

---

## Advice

Learning to create tables in LaTeX may initially feel like extra work compared to graphical tools. However, the precision and reproducibility you gain are invaluable for professional documents. Focus on understanding how column alignment, lines, and formatting work together. Once you master these basics, more advanced packages like `booktabs`, `longtable`, and `tabularx` will allow you to create highly customized and elegant tables. Patience with the syntax now will pay off as your documents grow in complexity.
