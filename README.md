# osnotes

Notes on OS development.

# Why not use GCC?

https://news.ycombinator.com/item?id=12891271

Always wasn't always always; that sad story is the source of your OCaml problems,
among many others. Linux on x86 originally used 4-byte alignment, and 4-byte alignment
is what you see if you RTFM[1]. Later, gcc decided that they were in control, and
unilaterally switched to 16-byte alignment. Backwards compatibility? Screw you.
Other tools? Screw you.[2]

[1] https://refspecs.linuxfoundation.org/
[2] https://gcc.gnu.org/bugzilla/show_bug.cgi?id=38496
