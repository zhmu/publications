ASPELL =	c:/bin/aspell/bin/aspell
EBB =		ebb
FILES =		verslag.tex inleiding.tex
IMAGES =	delem_logo.jpg organisatie.jpg proces.jpg pers1.jpg pers2.jpg \
                hsb.jpg planning.jpg initiele_planning.png \
                def_res.png
EPS =           waterval.eps xml.eps dataflow.eps planning.eps

verslag.pdf:	images $(FILES)
		pdflatex verslag.tex
		pdflatex verslag.tex
		makeindex verslag
		pdflatex verslag.tex

spell:		$(FILES)
		for i in $(FILES); do \
			$(ASPELL) --lang=nl -c "$$i"; \
		done

images:		$(IMAGES) $(EPS)
		for i in $(IMAGES); do \
			$(EBB) "$$i"; \
		done; \
		for i in $(EPS); do \
			epstopdf "$$i"; \
		done

clean:
		rm -f verslag.pdf *.aux *.log *.dvi *.idx *.ilg *.bb *.ind *.toc

proper:		clean
		rm -f *.tex~ Makefile~ *.bak

# vim:set ts=8:
