---
title: Recap-Title
author: Author-Name
date: Lecture-Date
papersize: a4
secnumdepth: 3
lang: en
includes: 
  - assets/figure_placement.tex
header-includes:
  - \usepackage{breqn}
  # - \renewcommand{\[}{\begin{dmath*}}
  # - \renewcommand{\]}{\end{dmath*}}
  - \lstset{breaklines=true}
  - \lstset{basicstyle=\small\ttfamily}
  - \lstset{extendedchars=true}
  - \lstset{tabsize=2}
  - \lstset{columns=fixed}
  - \lstset{showstringspaces=false}
  - \lstset{frame=trbl}
  - \lstset{postbreak=\raisebox{0ex}[0ex][0ex]{\ensuremath{\color{red}\hookrightarrow\space}}}
---
\newpage{}
<!--
  Using pandoc, this set of documents can be compiled into one PDF using
  `pandoc -o ./recap.pdf ./src/*.md -N --toc --variable classoption=twocolumn --listings`

  Long equations can make problems, when they're set in $$mathgoeshere$$. For this case, the package `breqn` is loaded.
  Use either manually \begin{dmath*} yourlongequation \end{dmath*} (leave the * out if you want numbered eq) for selected long equations,
  or uncomment the two `renewcommand`-options above to set EVERY equation using `breqn` which might line-break equations a bit too eagerly.

  There is still a problem using tables in the twocolumn-layout... maybe I'll find a nice solution for this someday.
  
  I'd advise to split the material into different numbered .md-files, as this makes managing them more easily.
-->

# Introduction

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc venenatis, ante et feugiat molestie, orci sem consectetur enim, vel feugiat odio enim sed elit. Nam bibendum a nisl nec gravida. Aenean arcu leo, molestie eget tortor vel, fermentum consequat nunc. Vestibulum consequat consequat auctor. Vivamus congue dui in sagittis tempor. Sed fermentum elit metus, in consectetur lorem vehicula a. Cras in dolor tempor orci tincidunt lacinia a id magna. Curabitur ac varius risus, eget finibus urna. Sed non vehicula lacus. Sed aliquet in ligula quis condimentum. Cras blandit turpis quis nisl facilisis congue.
