.PHONY: open clean problems open_problems

PROJECT		= bylaw1

MAIN_TEX	= ${PROJECT}.tex

PDF     = ${PROJECT}.pdf

FIGURES =

TEX     = pdflatex
TEXOPTS = -halt-on-error

open: ${PDF}
	open $< || gnome-open $<

${PDF}: ${MAIN_TEX} ${FIGURES}

%.pdf:	%.tex
	${TEX} ${TEXOPTS} $< 
	${TEX} ${TEXOPTS} $<

open_problems: ${PROBLEMS}
	open $< || gnome-open $<

clean:
	rm -f *.log *.aux *.dvi ${PDF}
