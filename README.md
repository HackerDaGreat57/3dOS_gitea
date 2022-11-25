# Hex-Zip (aka HZ)
Hex-Zip is an experimental file compression program that aims to work with all types of data. It will be fast and memory-efficient, processing just 1KiB (1024 bytes) of data at a time. Its compression algorithm (explained below) is designed in such a way that it can compress already-compressed files, resulting in infinite storage space reductions at the cost of CPU time. We call this method of compression "multi-layer compression".

This program's source code is hosted here because it will be included with 3dOS. All programs that will be included with 3dOS pre-installed will be hosted in this repository in their own orphan branches.
## How it Works
This section is being used for planning the program. I already have a clear gist about how it should work in my head, this is the place to write it all down.
1. Input file is split into 1KB blocks. If the size of the input file in bytes is not a multiple of 1024, the "last" block is filled with zeroes. See image below or [click here](./assets/readme/hzdms1.svg) for more understanding.  
<img src="./assets/readme/hzdms1.svg">