# Internship report

> This project representes my 2021 summer intership report. I wrote it in french using Latex. In this README.md file I am going to highlight the commands and packages used to write this wonderful document. If you would like to take a sight on the final result of this code you can avail yourself of this wonderful website: [overleaf](https://www.overleaf.com/).

## Packages

First of all, this is a report a4paper type document. It has 13pt headhieght, 3cm top margin and 2cm bottom and 1cm on left and right. The packages used in this project are:

* fontenc: encoding package. I used T1 standard text encoding, which encodes fonts that can render most European languages.
* biolinum: in this project I used biolinum font package. You can find more infos about it [here](https://tug.org/FontCatalogue/biolinum/).
* babel: this package manages culturally-determined typographical (and other) rules for a wide range of languages. I used french in my document.
* setspace: this package containes many spacing commands which were required inn my document.
* tabularx: I used tabularx to create tables and mange them easily.
* graphicx: the use of graphicx allowed me to include images in my document.
* wrapfig: I used wrapfig to wrap the used images into rectangle.
* float: It is used with the graphicx package to decclare floating space for my images.
* geometry: I used this package to define the margins of pages.
* fancyhdr: It allowed me to make fancy style for my headers and footers.
* hyperref: I used this package to create links and also to style my table of contents.

Along side the previous packages I renewed the command of `\headrulewidth` and `\footrulewidth`, to set them to 1pt. As well as I included **ENSIAS, number of page, and Année universitaire: 2020/2021** in my footer.

Brief:,

```latex
\documentclass[a4paper]{report}
\usepackage[T1]{fontenc}
\usepackage[sfdefault]{biolinum}
\usepackage[french]{babel}
\usepackage{setspace}
\usepackage{tabularx}
\usepackage{graphicx}
\usepackage{wrapfig}
\usepackage{float}
\usepackage[headheight=13pt,top=3cm, bottom=2cm, left=1cm, right=1cm]{geometry}
\usepackage{fancyhdr}
\pagestyle{fancy}
\usepackage{hyperref}
\hypersetup{
    colorlinks=true,
    linkcolor=black,
    citecolor=black,
    filecolor=black,
    urlcolor=black,
}
\renewcommand{\headrulewidth}{1pt}
\renewcommand{\footrulewidth}{1pt}
\fancyfoot[L]{ENSIAS}
\fancyfoot[C]{\textbf{\thepage}}
\fancyfoot[R]{Année universitaire: 2020/2021}
```

## Keep-in-mind commands

* To declare the start and the end of the document:
```latex
\begin{document}
\end{document}
```
* To declare the start and the end of the title page:
```latex
\begin{titlepage}
\end{titlepage}
```
* To declare the start and the end of the centered element:
```latex
\begin{center}
\end{center}
```
* To declare the type of the page numbering:
```latex
\pagenumbering{roman} \setcounter{page}{1}  % i ii iii iv ...
\pagenumbering{arabic} \setcounter{page}{1} % 1 2 3 4 5 ...
\pagenumbering{alph} \setcounter{page}{1}   % a b c d f e ...
```
* To declare the start and the end of the double space text form:
```latex
\begin{doublespace}
\end{doublespace}
```
* To declare the start and the end of *italic text*:
```latex
\textit{}
```
* To add this chapter to content table and give it the title "Title":
```latex
\addcontentsline{toc}{chapter}{Title}
```
* To declare the table of content, figures, and tables:
```latex
\newpage

\fancyhead[R]{\textbf{Table des matières}}
\fancyhead[L]{\hspace*{5cm}}
\tableofcontents

\newpage
\listoffigures

\newpage
\renewcommand{\listtablename}{Table des tableaux} % I renamed liste of tables because it is a french document and table des tableaux is better.
\listoftables

\newpage
```
* To declare the start and the end of list of items:
```latex
\begin{itemize}
	\item[•] 
\end{itemize}
```
* To declare chapter, section, subsection, subsubsection with the title Title:
```latex
\chapter{Title}
\section{Title}
\subsection{Title}
\subsubsection{Title}
```
* To declare a centered figure, wraped in a box, with the scale 0.5, and the title Title:
```latex
\begin{figure}[H] % declare figure
	\begin{center} % center it
		\fbox{\includegraphics[scale=0.5]{image.png}} % wrap it and display it
		\caption{Title} % give it a beautiful meaningful title
	\end{center}
\end{figure}
```
* To declare a table with title Title, the width 17.5cm:
```latex
	\begin{table}[H]
		\begin{center}
			\begin{tabularx}{17.5cm}{|p{3cm}|p{3cm}|X|} % p{3cm}means that the with of that column is 3cm, X takes automaticly the remaining space
				\hline
				\textbf{title1} & \textbf{title2} & \textbf{title3} \\
				\hline
				row2column1 data      & row2column2 data       & row2column3 data \\
				\hline
			\end{tabularx}
			\caption{Title}
		\end{center}
	\end{table}
```
* To declare the appendix section:
```latex
\appendix
```