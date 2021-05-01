JADE = jadejs
JADEFLAGS = --path .

SASS = sassc
SASSFLAGS =

all: dist/index.html dist/main.css

clean:
	$(RM) -r dist

dist:
	mkdir -p $@

dist/%.html: pages/%.jade templates/main.jade | dist
	$(JADE) $(JADEFLAGS) <$< >$@

dist/main.css: sass/main.sass $(wildcard sass/*.sass)
	$(SASS) $(SASSFLAGS) --style compressed $< $@
