latex-template
==============

This is a simple template useful for starting LaTeX documents. All package includes and additional commands are defined in `customizations.sty`. Reading through it will help you write more efficiently. A lot of the custom commands are aimed at mathematcal writing, but they can be easily changed to suit different needs. Please make sure to copy `customizations.sty` along with any documents derived from this template.

Both `template.tex` and `customizations.sty` include auctex-specific footers.
```
%%% Local Variables: 
%%% mode: latex
%%% TeX-master: "template"
%%% End: 
```
In order to make sure emacs and auctex correctly handle the document, change `TeX-master` to reflect the root of your document. 

To compile the document from a terminal, run
```
latexmk -pdf template.tex
```
This command automatically figures out the number of calls to `pdflatex` and `bibtex` which have to be made. If [latexmk](http://users.phys.psu.edu/~collins/software/latexmk-jcc/) is not available, the following sequence of invocations should also do the trick.
```
pdflatex template.tex
pdflatex template.tex
bibtex template
pdflatex template.tex
```
If not using a bibliography, the first two commands suffice.
