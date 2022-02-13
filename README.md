# macos_asx_exec09

ASxxxx (https://shop-pdp.net/ashtml/asxxxx.php) and exec09 (https://github.com/nealcrook/exec09) binaries for macOS.

For exec09 to work correctly with ASxxxx I had to clone the tag https://github.com/nealcrook/exec09/releases/tag/multicomp09_mmapper_mk1.

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

(I got the autoreconf command from [this repo's README](https://github.com/nils-eilers/exec09), and the rest of them from [this installation script](https://github.com/nealcrook/exec09/blob/trunk/build.osx.sh)).

I also told make and configure to use gcc instead of clang, because clang was erroring out.

NOTE 2: I built this on macOS 12.1 with XCode 13.2.1.
