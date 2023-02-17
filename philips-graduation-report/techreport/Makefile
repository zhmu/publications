FILES =		defs.tex limefs.tex intro.tex io.tex preface.tex summary.tex \
		techreport.tex impl.tex bib.bib
ASPELL =	aspell

techreport.pdf: $(FILES)
		pdflatex techreport.tex
		bibtex techreport
		makeindex techreport
		pdflatex techreport.tex
		pdflatex techreport.tex

clean:
		rm -f techreport.pdf *.aux *.log *.dvi *.idx *.ilg *.bb *.ind *.toc

proper:		clean
		rm -f *.tex~ Makefile~ *.bak

spell:		$(FILES)
		for i in $(FILES); do \
			$(ASPELL) -c "$$i"; \
		done
