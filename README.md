# recap-template

A simple markdown-template for (lecture) notes and recaps.

## About this repository

While studying, I've mainly learned by writing my own recap of the whole lecture. Although I really like using LaTeX for writing, it can be quite cumbersome for notes with a lot boilerplate for enumerations, itemizations etc.

That's why I started using markdown in combimation with pandoc to simplify note-taking with the simple syntax of markdown and generating goodlooking TeX-like documents.

I've put this up as a repo, because maybe someone will find this template useful, too :)

## Getting started

So, basically this is just markdown. Clone it and use one of the numerous ways of compiling it. However, I opted for using `pandoc` and vscode.

For this, you have to install [Pandoc](https://pandoc.org/) and [Visual Studio Code](https://code.visualstudio.com/) if you don't have it already.

### IDE

I'm using vscode to write the recaps, mainly because there are a lot of great extensions which really ease working with markdown. The packages I'm currently using:

- [Markdown All in One](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one): Great tools, commands and shortcuts around writing markdown.
- [Markdown Paste](https://marketplace.visualstudio.com/items?itemName=telesoho.vscode-markdown-paste-image): Makes adding images to your recap a breeze. You can easily add paste images directly from the clipboard into the markdown and give it a title/caption. The image will automatically be put in a specified directory.
- [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint) because, well... linting your code is always a good idea :)

Also, I have added a custom task for compiling all `.md`-files under the `src`-directory that can be triggered with `ctrl + shift + b`. This will just wildcard the filenames, so simply order your markdown files by preceding them with the section-number. Also, this will generate a TOC and print the document in the two-column layout, as I personally found this easier to use for learning. However, this command can easily be adjusted.

There is also a config for markdownlint, as I decided to exclude the following rules:

- MD025: Because when using pandoc and a yaml-Header, a document-title is already specified. Thus, the top-level headings can be used multiple times.
- MD013: Because it makes writing (and reading) a lot of text very cumbersome when you manually break the lines to stay in the limit.

### Markdown / TeX

Using pandoc for compiling markdown has the advantage that you're able to use latex in your document. I added a yaml-header for setting different variables such as title, author etc. in the `src/00_intro.md`-file. There are also latex-headers for `lstlisting` so source-code can be rendered nicely with the two-column layout using markdown-syntax (fenced code in backticks, stating the language on top).

As long equations can make problems (especially in two-columns), I also added the `breqn`-Package that allows to handle long equations differently. Either use `\begin{dmath*} yourlongequation \end{dmath*}` (leave the `*` out if you want numbered eq) manually for selected long equations or uncomment the two `renewcommand`-options in the header to set EVERY equation using `breqn` (which might line-break equations a bit too eagerly).

Currently, there is a problem using tables inside the two-column layout with pandoc. I'm still to find a proper solution for this...
