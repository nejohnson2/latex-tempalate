# Latex Template

Best source  of info is at the [Latex Wiki](https://en.wikibooks.org/wiki/LaTeX)

## Basic layout

```latex
\documentclass{article}

\title{Amazing Title}
\author{You}

\begin{document}
\maketitle

\begin{abstract}
Amazing abstract
\end{abstract}

\section{Literature Review}
Lots of text

\end{document}
```

Compile from commandline with:

```
$ pdflatex latex-template.tex
```

## Bilbliography

Add a ```biblography.bib``` file to the repo.  Then add ```\bibliography{bibliography}``` and ```bibliographystyle{plain}``` just above the end of the file.  You need to compile everything with

```
$ pdfkatex latex-template.tex
$ bibtex latex-template.aux
$ pdfkatex latex-template.tex
$ pdfkatex latex-template.tex
```

## Images

Add ```\usepackage{graphicx}``` and include the folder path ```\graphicspath{{./figures/}}```.

```
\begin{figure}
  \centering
  \includegraphics[width=0.5\textwidth]{test}
  \caption{A picture of the same gull looking the other way!}
\end{figure}
```

Add these to the ```.gitignore``` since they are generated everytime latex compiles.

```
*.aux
*.glo
*.idx
*.log
*.toc
*.ist
*.acn
*.acr
*.alg
*.bbl
*.blg
*.dvi
*.glg
*.gls
*.ilg
*.ind
*.lof
*.lot
*.maf
*.mtc
*.mtc1
*.out
*.synctex.gz
```