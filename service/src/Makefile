# apt-get install musl-tools
.PHONY: all clean

CFLAGS = -fPIC -pie

all: release

release: mooosl /lib/ld-musl-x86_64.so.1 /lib/x86_64-linux-musl/libc.so
	cp $^ ../

mooosl: service
	cp $< $@
	strip $@

service: service.c
	musl-gcc $(CFLAGS) $< -o $@

clean:
	rm service mooosl
