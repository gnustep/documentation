# Using the GNUstep MSVC toolchain

## 1 Hello World (From the command line)

A simple way to compile an Objective-C program with the toolchain is by using the MSYS2 shell.

Install MSYS2 using Chocolatey:
```sh
choco install msys2
```

Open a MSYS2 shell (Windows + R -> msys2.exe), and run the following commands:
```sh
# We need to export the path to the LLVM binaries and GNUstep binaries
export PATH=$PATH:/c/Program\ Files/LLVM/bin:/c/GNUstep/x64/Debug/bin

# Source the GNUstep environment
source /c/GNUstep/x64/Debug/share/GNUstep/Makefiles/GNUstep.sh

# Create a directory for our project
mkdir hello && cd hello

touch main.m
```

You can now edit `main.m` with your favourite text editor, and add the following code:
```objc
#import <Foundation/Foundation.h>

int main(int argc, const char * argv[]) {
	@autoreleasepool {
		NSLog(@"Hello, World!");
	}
	return 0;
}
```

Now we can compile the program:
```sh
clang -o hello `gnustep-config --objc-flags` `gnustep-config --base-libs` main.m
```

Or alternatively in two stages:
```sh
# --objc-flags: output the flags needed to compile Objective-C code
clang -c `gnustep-config --objc-flags` main.m
# --base-libs: output the flags needed to link with the base library
clang -o hello main.o `gnustep-config --base-libs`
```

For more information you can run `gnustep-config --help`.
If everything went well, you can now run the program:
```sh
./hello
# 2023-10-22 00:33:36.049 hello[5916:12508] Hello, World!
```

# 2 Using the toolchain without MSYS2

Using a POSIX shell is great for developers accustomed to UNIX-based systems, but not natural in the Windows world.
If you want to integrate GNUstep into a Visual Studio, or other build system, the best way is to specify the flags manually.

For more information on how to use the toolchain in Visual Studio, see [Using the toolchain in Visual Studio](https://github.com/gnustep/tools-windows-msvc#using-the-toolchain-in-visual-studio) in the projects GitHub readme.