target=wd_sugimoto
latex=platex
bibtex=jbibtex
enc=sjis

.PHONY: all
all:
	$(latex) --kanji=$(enc) $(target)
	$(bibtex) --kanji=$(enc) $(target)
	$(latex) --kanji=$(enc) $(target)
	$(latex) --kanji=$(enc) $(target)
	dvipdfmx $(target).dvi

.PHONY: clean
clean:
	rm -rf $(target).{aux,dvi,log,bbl,blg}
