# Docker Hyperion compilation
Provides images to compile Hyperion inside a Docker container.
Images are available at https://hub.docker.com/r/hyperionorg/hyperion-ci/

Tag explanation: Compile Hyperion ON os/hardware(arch) FOR os/hardware(arch)
 - `dockertag` ON os and/or hardware (arch) FOR os and/or hardware (arch)
 - `ubuntu1604` ON all(x86_64) FOR Ubuntu 16.04 (x86_64)
 - `cross-qemu-rpistretch` ON all(x86_64) FOR Raspberry Pi (arm, Raspbian Stretch)  as cross compilation through qemu
 - `rpistretch` ON all(arm) FOR Raspberry Pi (arm, Raspbian Stretch)

You can run these compiled binaries always on newer OS versions or comparable linux distributions, but never on older ones

TODO:
 - `cross-rpistretch` Use cmake cross Toolchain instead qemu (speed! ON x86_64 FOR Raspberry Pi (arm, Raspbian Stretch)) .
 - `cross-qemu-arm64` use qemu ( ON x86_64 FOR all(arm64, Debain Stretch)) .
 - `cross-arm64` Use cmake cross Toolchain instead qemu (speed! ON x86_64 FOR Raspberry Pi (arm64, Debain Stretch)) .
 - `arm64` ON all(arm64) FOR all(arm64).
