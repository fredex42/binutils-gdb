## How to compile and build

It's recommended to use the Docker environment as this has the correct versions of the relevant build tools available.

First, `cd` to the `ld` directory and run `automake`. This ensures that the Makefile is up-to-date with the changes from Makefile.am.

Then, go back to the root and:

```bash
./configure --target=i386-elf-silly --prefix=/opt/cross --disable-nls --disable-gdb --disable-libdecnumber --disable-sim
make
make install
```

This should output the binutils into the `/opt/cross/i386-elf-silly` directory.
