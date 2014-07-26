all: 
	make Bioc2014.html

setvars:
ifeq (${R_HOME},)
R_HOME= $(shell R-stable RHOME)
endif

.PHONY: clean allclean all

Bioc2014.html: Bioc2014.Rmd
	"$(R_HOME)/bin/Rscript" -e "library('knitr'); knit2html('Bioc2014.Rmd')"

clean:	
	rm -f .Rhistory
	rm -f *~
	rm -rf output*xml

allclean: clean 
	rm -f Bioc2014.md Bioc2014.html
	rm -rf cache figure


