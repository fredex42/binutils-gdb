## How to compile and build

```bash
./configure --target=i386-elf-silly --prefix=/opt/cross --disable-nls --disable-gdb --disable-libdecnumber --disable-sim
make
make install
```

## Outstanding issues

Install phase is currently failing: 
```
/bin/bash ./../mkinstalldirs /opt/cross/i386-elf-silly/lib/ldscripts
for f in ldscripts/* ; do \
  /usr/bin/install -c -m 644 $f /opt/cross/i386-elf-silly/lib/$f ; \
done
/usr/bin/install: cannot stat 'ldscripts/*': No such file or directory
```

looks like a setup step is missed :(
        