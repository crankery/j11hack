GALASM := GALasm/galasm

PLDS := $(wildcard *.pld)
JEDS := $(PLDS:.pld=.jed)

.PHONY: all clean galasm

all: $(JEDS)

galasm:
	$(MAKE) -C GALasm

$(GALASM):
	$(MAKE) -C GALasm

%.jed: %.pld $(GALASM)
	$(GALASM) $<

clean:
	rm -f *.jed *.fus *.pin *.chp

