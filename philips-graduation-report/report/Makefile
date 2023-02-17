FILES =		conclusion.tex defs.tex evaluation.tex hi_voorblad.tex \
		intro.tex personal.tex preface.tex project.tex report.tex \
		summary.tex samenvatting.tex
ASPELL =	aspell

report.pdf: $(FILES)
		pdflatex report.tex
		bibtex report
		makeindex report
		pdflatex report.tex
		pdflatex report.tex

clean:
		rm -f report.pdf *.aux *.log *.dvi *.idx *.ilg *.bb *.ind *.toc *.bbl *.blg *.out

proper:		clean
		rm -f *.tex~ Makefile~ *.bak

spell:		$(FILES)
		for i in $(FILES); do \
			$(ASPELL) -c "$$i"; \
		done
