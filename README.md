# UnZip/ZipInfo 6.0 for android arm64

## Build :

Download [Android NDK](https://developer.android.com/ndk/downloads)

Extract it in ~/NDK or look at [this commit](https://github.com/3arthur6/UnZip/commit/81833625a52bbc70c1956d0ca515f5e0c1a12805) and modify to point to the extract directory

### To use on android system :

```bash
make -f unix/Makefile linux_noasm
```

### To use on android recovery :

```bash
make -f unix/Makefile linux_noasm
sed -i "s|/system/bin/linker64\x0|/sbin/linker64\x0\x0\x0\x0\x0\x0\x0|g" unzip
```
