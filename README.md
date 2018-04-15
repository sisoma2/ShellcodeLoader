# ShellcodeLoader

ShellcodeLoader has been built with the purpose to quickly debug a shellcode extracted in malware analysis in a context of an executable.
What ShelcodeLoader does is read a bynary file from disk to memory and jump to the base or an especified entry point to execute the file.
It autodetects if it's being debugged and asks the user if he/she wants to set a breakpoint before the execution of the shellcode.
Works in x86 and x64 systems.

## Releases

Go to the Releases tab and download the compiled executables.

## Usage

The file is required. The other arguments are optional.
```
ShellcodeLoader.exe [-e --entrypoint ENTRYPOINT] [-a --address ADDRESS] [-r --run] [-b --break] FILE
```

Loads the file and executes the code at a specified offset
```
ShellcodeLoader.exe -e 1000 shellcodex86.bin
```

Reads the file and tries to allocate memory at the specified address and copy the shellcode to this region and execute it
```
ShellcodeLoader.exe -a 30000 shellcodex86.bin
```

Runs the shellcode without stopping or breaking. __Warning:__ The shellcode will be executed in your machine.
```
ShellcodeLoader.exe -r shellcodex86.bin
```

Tries to copy the shellcode at the specified region and sets a breakpoint before jumping to the specified entrypoint
```
ShellcodeLoader.exe -a 30000 -e 1000 -b shellcodex86.bin
```

## Building 
__Requirements__
 - Download and install Microsoft Visual C++ Build Tools or Visual Studio 

__Build Steps__
 - Clone the repo and navigate to the directory
 - Open the SLN file to open the project to Visual Studio
 - Select the platform in which you will be compiling the binary (x32 or x64)
 - Go to Compile->Compile Solution to generate the EXE file
 
## Shellcode Samples 

The files shellcodex86.bin and shellcodex64.bin are shellcodes compiled with NASM that execute a calc.exe via WinExec Windows API for the purpose to test the software.

## Feedback

Any questions, comments or requests you can find me on twitter: [@sisoma2](https://twitter.com/sisoma2)
Pull requests welcome! 
