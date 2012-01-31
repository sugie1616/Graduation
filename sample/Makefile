# tex makefile

TARGET = ./sample
ENCODE = sjis

all:
	extractbb image/*.pdf
	platex   -kanji=$(ENCODE) $(TARGET).tex
	jbibtex -kanji=$(ENCODE) $(TARGET)
	platex   -kanji=$(ENCODE) $(TARGET).tex
	platex   -kanji=$(ENCODE) $(TARGET).tex
	dvipdfmx  $(TARGET).dvi

clean:
	rm -rf $(TARGET).{bbl,dvi,log,toc,aux,blg,lof}
