# ShellcodeLoader

ShellcodeLoader has been built with the purpose to quickly debug a shellcode extracted in malware analysis in a context of an executable.
What ShelcodeLoader does is read a bynary file from disk to memory and jump to the base or an especified entry point to execute the file.

## Releases

I will add a release for x86 and x64 platforms soon.

## Usage

[WORKING]

## Building 
__Requirements__
 - Download and install Microsoft Visual C++ Build Tools or Visual Studio 

__Build Steps__
 - Clone the repo and navigate to the directory
 - Open the SLN file to open the project to Visual Studio
 - Select the platform in which you will be compiling the binary (x32 or x64)
 - Go to Compile->Compile Solution to generate the EXE file
 
## Shellcode Samples 

The file example.exe it's a shellcode embedded into a PE file but it acts as a shellcode.
It traverses the PEB and searches the function MessageBoxA to show a HelloWorld message.
It only works in x86.

## Feedback

Any questions, comments or requests you can find us on twitter: @sisoma2
Pull requests welcome! 
