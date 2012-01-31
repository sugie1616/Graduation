# tex makefile

TARGET = ./0844070
ENCODE = sjis

.PHONY: all
all:
	extractbb image/*.pdf
	platex   -kanji=$(ENCODE) $(TARGET).tex
	jbibtex -kanji=$(ENCODE) $(TARGET)
	platex   -kanji=$(ENCODE) $(TARGET).tex
	platex   -kanji=$(ENCODE) $(TARGET).tex
	dvipdfmx  $(TARGET).dvi

.PHONY: clean
clean:
	rm -rf $(TARGET).{bbl,dvi,log,toc,aux,blg,lof}
