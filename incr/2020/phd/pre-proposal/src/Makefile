all: preproposalTemplate.pdf

OPTIONS=-interaction nonstopmode -halt-on-error -file-line-error

deps=preproposalTemplate.tex preproposal.bib

%.pdf:  %.tex *.bib $(deps)
	pdflatex $(OPTIONS) $<
	- bibtex $*
	pdflatex $(OPTIONS) $<
	pdflatex $(OPTIONS) $<

clean:
	$(RM) *.log *.aux \
	*.cfg *.glo *.idx *.toc \
	*.ilg *.ind *.out *.lof \
	*.lot *.bbl *.blg *.gls *.cut *.hd \
	*.dvi *.ps *.thm *.tgz *.zip *.rpi *.pdf
