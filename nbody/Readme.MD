This will be a repository containing perfromacne benchmarks between WASM and JavaScript Implementations.

Optimized codes are taken from "The Computer Language
Benchmarks Game": https://benchmarksgame.alioth.debian.org/u64q/cpp.html and some custom modifications for the javascript versions

This repo right now only holds n-body implementations but will ahve the others as well.

# How to run

The javascript versions can simply be run from the browser. There's no build step for javascript necessary.


The C versions in the c directory can be compiled with gcc -O3 nbody.c -o nbody and gcc -O3 -fomit-frame-pointer -march=native -mfpmath=sse -msse3 nbody_fastest.c -o nbody_fastest 

The WebAsssembly version is compiled with emcc nbody.c -O3 -s WASM=1 -s SIDE_MODULE=1 -o nbody.wasm