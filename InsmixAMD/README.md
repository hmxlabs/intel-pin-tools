# InsmixAMD
This tool helps to find instructions on Intel CPUs with divergent numerical results on AMD CPUs.

This has been created and tested against Pin v3.31 on Linux (Ubuntu 20.04). Your results on other versions of Pin or other operating systems may vary.

Copy this directory to:

```
<pin_root>/source/tools/InsmixAMD
```

build the tool using the provided Makefile:

```
cd <pin_root>/source/tools/InsmixAMD
make
```

It can then be used with Pin as follows:

```
cd <pin_root>
./pin -t source/tools/InsmixAMD/obj-intel64/insmixamd.so -- <your_application>
```

This will produce output similar to the default Insmix tool. If you wish to restrict output to only those instructions that have a divergent numerical result between Intel and AMD CPUs use the `-divergent` flag.

```
./pin -t source/tools/InsmixAMD/obj-intel64/insmixamd.so -divergent 1 -- <your_application>
```
