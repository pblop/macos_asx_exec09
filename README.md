# macos_asx_exec09

ASxxxx (https://shop-pdp.net/ashtml/asxxxx.php) and exec09 (https://github.com/bcd/exec09) binaries for macOS.

I installed autoreconf, automake, readline, libtool, and gcc via homebrew.

And I then executed

```
$ glibtoolize --force          410ms
$ aclocal
$ autoheader
$ automake --force-missing --add-missing
$ autoconf
$ ./configure CC=gcc-11
$ make CC=gcc-11
```

(I got this from a stackoverflow post, I think. I added the CC=gcc-11 to tell configure and make to use gcc instead of clang, because clang was erroring out).

NOTE: I built this on macOS 12.1 with XCode 13.2.1.
