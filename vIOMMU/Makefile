#PAPER = asplos23-paper-template
PAPER = main
# ABSTRACT = asplos22-extended-abstract-template
TEX = $(wildcard *.tex sections/*.tex)
BIB = sample-base.bib
FIGS = $(wildcard figures/*.pdf figures/*.png graphs/*.pdf graphs/*.png)

.PHONY: all clean

# all: $(PAPER).pdf $(ABSTRACT).pdf
all: $(PAPER).pdf

$(PAPER).pdf: $(TEX) $(BIB) $(FIGS)
	pdflatex -shell-escape $(PAPER)
	bibtex $(PAPER)
	pdflatex -shell-escape $(PAPER)
	pdflatex -shell-escape $(PAPER)

# $(ABSTRACT).pdf: $(TEX) $(BIB) $(FIGS) jpaper.cls
# 	pdflatex $(ABSTRACT)
# 	bibtex $(ABSTRACT)
# 	bibtex $(ABSTRACT)
# 	pdflatex $(ABSTRACT)
# 	pdflatex $(ABSTRACT)


clean:
# 	rm -f *.aux *.bbl *.blg *.log *.out $(PAPER).pdf $(ABSTRACT).pdf
	rm -f *.aux *.bbl *.blg *.log *.out $(PAPER).pdf