OBJECTS = src/fxstudio.o src/sys/os.o src/sys/rom.o src/qoidecode.o src/project.o src/assets.o
.SUFFIXES: .o .asm .jkl

all: fxstudio.fxf

fxstudio.fxf: $(OBJECTS)
	target=fox32 $(XRLINK) link $@ $(OBJECTS) $(RTLLIB)
.jkl.asm:
	$(JKL) target=fox32 $< $@
.asm.o:
	$(XRASM) target=fox32 $< $@

clean:
	rm -f $(OBJECTS)

.PHONY: clean
