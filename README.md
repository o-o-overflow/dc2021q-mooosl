# DEFCON 2021 Quals mooosl

## Design

It's a heap exploitation challenge. Unlike traditional heap games, it is
built on top of the latest musl-libc's mallocng heap.

In order to push players to learn and hack the new system, I tried to
simplify and mitigate the attack surface in the main binary. Players have
to exploit the `free()` in the internal heap implementaion to get a useful
memory corruption primitive.

## Exploit

In [exploit.py](interaction/exploit.py) I have provided a solution to
gaining arbitrary memory write by leaking the context secret and crafting
meta area.
