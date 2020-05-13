# Compile Dav1d decoder for arm/aarch64 androideabi.

1. Download the Android ndk and Dav1d source code.

2. Install the 'meson' and 'ninja' program.

3. In the Dav1d root dir, run 'meson --cross-file cross_file_name android_arm_build'

4. cd android_arm_build, run 'ninja' command. The 'libdav1d.so' and test 
  program 'Dav1d' will be compiled.

  


# cross-file for ARCH arm

[host_machine]
system = 'android'
cpu_family = 'arm'
cpu = 'arm'
endian = 'little'

[properties]
sys_root = path/to/android-ndk-r21/sysroot'

[binaries]
c =     'path/to/android-ndk-r21/toolchains/llvm/prebuilt/linux-x86_64/bin/armv7a-linux-androideabi28-clang'
cpp =   'path/to/android-ndk-r21/toolchains/llvm/prebuilt/linux-x86_64/bin/armv7a-linux-androideabi28-clang++'
ar =    'path/to/android-ndk-r21/toolchains/llvm/prebuilt/linux-x86_64/bin/arm-linux-androideabi-ar'
strip = 'path/to/android-ndk-r21/toolchains/llvm/prebuilt/linux-x86_64/bin/arm-linux-androideabi-strip'
pkgconfig = 'false'



# cross-file for ARCH aarch64

[host_machine]
system = 'android'
cpu_family = 'aarch64'
cpu = 'aarch64'
endian = 'little'

[properties]
sys_root = ' path/to//android-ndk-r21/sysroot'

[binaries]
c =     ' path/to/android-ndk-r21/toolchains/llvm/prebuilt/linux-x86_64/bin/aarch64-linux-android28-clang'
cpp =   ' path/to//android-ndk-r21/toolchains/llvm/prebuilt/linux-x86_64/bin/aarch64-linux-android28-clang++'
ar =    ' path/to//android-ndk-r21/toolchains/llvm/prebuilt/linux-x86_64/bin/aarch64-linux-android-ar'
strip = ' path/to/android-ndk-r21/toolchains/llvm/prebuilt/linux-x86_64/bin/aarch64-linux-android-strip'
pkgconfig = 'false'

