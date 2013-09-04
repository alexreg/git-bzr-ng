SOURCES=$(wildcard *.[0-9].rst)
OUTPUT=$(patsubst %.rst, %, $(SOURCES))

.PHONY: all
all: $(OUTPUT)

.PHONY: clean
clean:
	rm -f $(OUTPUT)

%: %.rst
	rst2man $^ > $@
