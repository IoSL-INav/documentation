TARGET = main
BIBTEX = bibtex
PDFOPT = -file-line-error -interaction=nonstopmode
RERUN = "Rerun to get (cross-references|the bars|outlines) right"
RERUNBIB = "No file.*\.bbl|Citation.*undefined"

master:
	pdflatex $(PDFOPT) $(TARGET).tex
	make bib TARGET=$(TARGET)
	make rerun TARGET=$(TARGET)
	egrep -i "(Reference|Citation).*undefined" $(TARGET).log ; true

bib:
	egrep -c $(RERUNBIB) $(TARGET).log && bibtex $(TARGET).aux ; true

rerun:
	egrep $(RERUN) $(TARGET).log && pdflatex $(PDFOPT) $(TARGET).tex ; true
	egrep $(RERUN) $(TARGET).log && make rerun TARGET=$(TARGET) ; true

.PHONY: clean

clean:
	rm -f *.aux *.bbl *.blg *.dvi *.lof *.log *.bcf
	rm -f *.lot *.lox *.toc *.out *.ps  *.cb
	rm -f *.cb2 *.snm *.nav *.vrb
	rm -f *-blx.bib *.run.xml
	rm -f *.fdb_latexmk *.synctex.gz
	rm -f *_handout.tex
	rm -f *~