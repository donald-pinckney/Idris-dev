IDRIS ?= idris
PKG := base

build:
	$(IDRIS) --build ${PKG}.ipkg

install:
	$(IDRIS) --install ${PKG}.ipkg
	${IDRIS} --installdoc ${PKG}.ipkg

clean:
	$(IDRIS) --clean ${PKG}.ipkg

rebuild: clean build

doc:
	${IDRIS} --mkdoc ${PKG}.ipkg

doc_clean:
	rm -rf ${PKG}_doc

linecount:
	find . -name '*.idr' | xargs wc -l

.PHONY: build install clean rebuild linecount doc doc_clean
