SOURCE = main
PDFMAKER = pdflatex
BIBMAKER = biber

doc:
	$(PDFMAKER) $(SOURCE).tex
	$(BIBMAKER) $(SOURCE)
	$(PDFMAKER) $(SOURCE).tex

.PHONY: clean

clean:
	rm -f *.aux *.bbl *.blg *.dvi *.lof *.log *.bcf
	rm -f *.lot *.lox *.toc *.out *.ps  *.cb
	rm -f *.cb2 *.snm *.nav *.vrb
	rm -f *-blx.bib *.run.xml
	rm -f *.fdb_latexmk *.synctex.gz
	rm -f *_handout.tex
	rm -f *~