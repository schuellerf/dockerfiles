# arm64-crosscompile

This image provides the tools necessary to compile an arm64 Linux kernel or u-boot on an x86 system.

Usage:

    docker run -ti markusk/arm64-crosscompile

Optionally, you can add a volume for your build environment like so:

    docker run -ti -v /path/to/existing/files/:/srv/myfiles/ markusk/arm64-crosscompile
