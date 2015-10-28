PDFLATEX:=pdflatex -halt-on-error
BIBTEX:=bibtex
TARGET:=main

default:
	$(PDFLATEX) $(TARGET).tex
	$(BIBTEX) $(TARGET)
	$(PDFLATEX) $(TARGET).tex

.PHONY: clean
clean:
	rm -v *.aux *.toc *.log *.out *.bbl *.bcf *.blg *.lof *.lot *.nav *.run.xml *.snm main.pdf
