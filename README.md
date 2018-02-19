# Docker Hyperion compilation
Provides images to compile Hyperion inside a Docker container.
Images are available at https://hub.docker.com/r/hyperionorg/hyperion-ci/

Tag explanation: Compile Hyperion on/for
 - `dockertag` OS and/or hardware (Arch)
 - `ubuntu1604` Ubuntu 16.04 (x64)
 - `cross-qemu-rpistretch` Raspberry Pi (Raspbian Stretch) (armv6) as cross compilation through qemu

You can run these compiled binaries always on newer OS versions or comparable linux distributions, but never on older ones

TODO:
 - `cross-rpistretch` Use cmake cross Toolchain instead qemu (speed!).
 - `rpistretch` Native builds executed on a Pi
