# You need calibre installed (http://calibre-ebook.com/)

STYLESHEET=/usr/share/xml/docbook/stylesheet/docbook-xsl/xhtml/docbook.xsl

all: book.mobi book.epub clean

book.epub: book.html
	ebook-convert $^ $@ \
		--level1-toc //h:h1 \
		--level2-toc //h:h2 \
		--level3-toc //h:h3 \
		--language en

book.mobi: book.html
	ebook-convert $^ $@ \
		--level1-toc //h:h1 \
		--level2-toc //h:h2 \
		--level3-toc //h:h3 \
		--language en

book.html: book.xml
	xsltproc --output $@ $(STYLESHEET) $^

clean:
	rm -f book.html

.PHONY: all

