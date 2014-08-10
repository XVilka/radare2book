## Compilation and portability

Currently the core of radare2 can be compiled on many systems and architectures but the main development is done on GNU/Linux and GCC and OSX with clang. But it is also known to compile with TCC and SunStudio.

People usually wants to use radare as a debugger for reverse engineering, and this is a bit more restrictive portability issue, so if the debugger is not ported to your favorite platform, please, notify it to me or just disable the debugger layer with --without-debugger in the ./configure stage.

Nowadays the debugger layer can be used on Windows, GNU/Linux (intel32, intel64, mips, arm), FreeBSD, NetBSD, OpenBSD (intel32, intel64) and there are plans for Solaris and OSX. And there are some IO plugins to use gdb, gdbremote or wine as backends.

For example, to install in BSD:

    $ ./configure --prefix=/usr
    $ gmake
    $ sudo gmake install
    
But there is a simple script to do that automatically:

    $ sys/install.sh
