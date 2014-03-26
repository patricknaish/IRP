report.pdf: .FORCE
	pdflatex report.tex
	bibtex report
	pdflatex report.tex
	pdflatex report.tex
	rm report.aux report.log report.bbl report.blg
.PHONY: .FORCE

.FORCE:

clean:
	rm report.aux report.log report.bbl report.blg report.pdf
