M4 = m4

SASS = sassc
SASSFLAGS =

all: dist/index.html dist/main.css

clean:
	$(RM) -r dist

dist:
	mkdir -p $@

dist/%.html: pages/%.html.m4 templates/main.html.m4 | dist
	$(M4) $< >$@

dist/main.css: sass/main.sass $(wildcard sass/*.sass)
	$(SASS) $(SASSFLAGS) --style compressed $< $@
