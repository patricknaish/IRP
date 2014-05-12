poster.pdf: .FORCE
	pdflatex poster.tex
	bibtex poster
	pdflatex poster.tex
	pdflatex poster.tex
	rm poster.aux poster.log poster.bbl poster.blg
.PHONY: .FORCE

.FORCE:

clean:
	rm poster.aux poster.log poster.bbl poster.blg poster.pdf
