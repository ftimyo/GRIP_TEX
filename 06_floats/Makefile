SRC=new_float
SYS=$(shell uname -s)

all:
	pdflatex $(SRC)
	pdflatex $(SRC)

open: $(SRC).pdf
ifeq ($(SYS),Darwin)
	open -a preview $^
else
ifeq ($(SYS),Linux)
	evince $^
else
	@echo "Cannot find proper PDF viewer in System $(SYS)"
endif
endif

clean:
	rm -f *.log *.aux *.pdf *.dvi *.ps *.blg *.bbl
