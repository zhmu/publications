RUBBER?=	rubber -d
CONVERT?=	convert
INCLUDES=	generalnotes.tex gridsize.tex introtheory.tex \
		leaderelection.tex nodecoords.tex operation.tex overview.tex \
		showtime.tex intro.tex axioms.tex timed.tex complete.tex \
		abstract.tex acknowledgements.tex closing.tex generic.sty \
		proofs.tex source.tex bib.bib

report.pdf:	report.tex $(INCLUDES)
		$(RUBBER) report.tex

spell:
		for i in $(INCLUDES); do \
			aspell -c $$i; \
		done

clean:
		$(RUBBER) --clean report.tex
