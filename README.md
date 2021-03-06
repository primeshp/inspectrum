# inspectrum
inspectrum is a tool for analysing captured signals, primarily from software-defined radio receivers.

![inspectrum screenshot](/screenshot.jpg)

## Try it
### Prerequisites

 * qt5
 * fftw 3.x
 * cmake
 * pkg-config

### Building on Debian-based distros

    sudo apt-get install qt5-default libfftw3-dev cmake pkg-config
    mkdir build
    cd build
    cmake ..
    make
    sudo make install


## Building on OSX

    brew install qt5 fftw cmake pkg-config
    mkdir build
    cd build
    CMAKE_PREFIX_PATH=$(brew --prefix qt5)/lib/cmake cmake ..
    make install


### Run

    ./inspectrum

Currently inspectrum can only read files with interleaved (complex) 32-bit floats, such as those produced by GNURadio or osmocom_fft.

## Features
 * Spectrogram with zoom/pan
 * Large (multi-gigabyte) file support

## Goals
 * Be fast and light
 * Make as many settings as possible work in realtime. I want this to be a useful tool for visually learning about DSP by tweaking around with things like FFT settings, filter widths or clock synchronisation.
 * Support large files - as large as possible, but at least several GBs.
 * Future features: filtering, demodulation, clock sync. Probably based on GNURadio.
 
## Contact
 * #inspectrum on freenode IRC
