## The path and common arguments
SVG2MOD_ARGS = --format pretty --precision 1.0
FACTOR ?= 0.39

## The pattern rule to turn any SVG into a KiCAD footprint.
%.kicad_mod: %.svg Makefile
	svg2mod $(SVG2MOD_ARGS) --factor $(FACTOR) \
		-i $< -o $@ --name $(*F) --value $(*F)

# Graphics assets
mozilla-lizard-star-logo.kicad_mod: mozilla-lizard-star-logo.svg

all: badge.pretty/mozilla-lizard-star-logo.kicad_mod

