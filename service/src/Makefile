# apt-get install musl-tools
.PHONY: all clean

CFLAGS = -fPIC -pie
# CFLAGS += -ggdb3

all: release

release: mooosl /lib/x86_64-linux-musl/libc.so
	cp $^ ../

mooosl: service
	cp $< $@
	strip $@

service: service.c
	musl-gcc $(CFLAGS) $< -o $@

h: h.c
	gcc -O3 h.c -o h

clean:
	rm service mooosl
