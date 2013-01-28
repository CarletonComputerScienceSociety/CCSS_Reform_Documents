.PHONY: open clean

BYLAWS		= bylaw1 bylaw2

SOURCE	= ${addsuffix .tex,${BYLAWS}}

PDF     = ${addsuffix .pdf,${BYLAWS}}

FIGURES =

TEX     = pdflatex
TEXOPTS = -halt-on-error

open: ${PDF}
	open $< || gnome-open $<

${PDF}: ${SOURCE} ${FIGURES}

%.pdf:	%.tex
	${TEX} ${TEXOPTS} $< 
	${TEX} ${TEXOPTS} $<

clean:
	rm -f *.log *.aux *.dvi ${PDF}
