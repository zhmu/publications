ASPELL =	c:/bin/aspell/bin/aspell
EBB =		ebb
FILES =		pva.tex inleiding.tex bedrijf.tex project.tex samenvatting.tex \
		conclusie.tex planning.tex beheersaspecten.tex commplan.tex \
		achtergrond.tex
IMAGES =	delem_logo.jpg organisatie.jpg proces.jpg pers1.jpg pers2.jpg \
		hsb.jpg planning.jpg

pva.pdf:	pva.dvi
		dvipdfm pva.dvi

pva.dvi:	images $(FILES)
		latex pva.tex
		latex pva.tex
		makeindex pva
		latex pva.tex

spell:		$(FILES)
		for i in $(FILES); do \
			$(ASPELL) --lang=nl -c "$$i"; \
		done

images:		$(IMAGES)
		for i in $(IMAGES); do \
			$(EBB) "$$i"; \
		done

clean:
		rm -f pva.pdf *.aux *.log *.dvi *.idx *.ilg *.bb *.ind *.toc

proper:		clean
		rm -f *.tex~ Makefile~ *.bak

.jpg.bb:
		ebb $!
