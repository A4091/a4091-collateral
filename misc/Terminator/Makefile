OPENSCAD = /Applications/OpenSCAD.app/Contents/MacOS/OpenSCAD
SRC = A4091_terminator.scad
DEPS = $(SRC) ../YAPP_Box/YAPPgenerator_v3.scad

all: A4091_terminator_base.stl A4091_terminator_lid.stl

A4091_terminator_base.stl: $(DEPS)
	$(OPENSCAD) -o $@ -D 'printBaseShell=true' -D 'printLidShell=false' $(SRC)

A4091_terminator_lid.stl: $(DEPS)
	$(OPENSCAD) -o $@ -D 'printBaseShell=false' -D 'printLidShell=true' $(SRC)

clean:
	rm -f A4091_terminator_base.stl A4091_terminator_lid.stl

.PHONY: all clean
