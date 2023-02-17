FILES =		voorblad.tex

verslag.pdf:	$(FILES)
		pdflatex voorblad.tex

clean:
		rm -f voorblad.pdf *.aux *.log *.dvi *.idx *.ilg *.ind *.toc

proper:		clean
		rm -f *.tex~ Makefile~ *.bak

# vim:set ts=8:
