LATEX       = pdflatex
CHECK_RERUN = grep Rerun $*.log

all: bentobox.pdf

%.pdf: %.tex
	${LATEX} $<
	( ${CHECK_RERUN} && ${LATEX} $< ) || echo "Done."
	( ${CHECK_RERUN} && ${LATEX} $< ) || echo "Done."
