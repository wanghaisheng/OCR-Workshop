# written 2015-04-14, US
# usage: make 

PDFS = $(patsubst %.md,%.pdf,$(wildcard *.md))
VPATH = pdfs

all: $(PDFS)

%.pdf: %.md
	pandoc $< \
	    --slide-level 2 \
	    --bibliography=include/ocropus.bib \
	    --latex-engine=xelatex \
	    -t beamer \
	    -H include/beamer-header.tex \
	    -o pdfs/$@

.PHONY: clean
clean:
	$(RM) pdfs/*.pdf
