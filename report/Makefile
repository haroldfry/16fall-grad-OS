.PHONY: clean

NAME = proposal

# Graphs required by tex
# GRAPHS = sample.pdf

all: $(NAME).pdf

$(NAME).pdf: $(NAME).tex ${GRAPHS}
	pdflatex $(NAME)
	# bibtex $(NAME)
	pdflatex $(NAME)
	pdflatex $(NAME)

%.pdf: %.eps
	epstopdf $< --outfile=$@

%.eps: %.svg
	convert $< $@

clean:
	@rm *.aux *.pdf *.log *.out *.bbl *.eps *.blg
