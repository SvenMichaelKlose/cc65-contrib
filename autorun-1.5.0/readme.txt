
 AutoRun 1.5.0 for C64 by Michael McIntosh

 A small program that executes itself immediately after being loaded. This
 program loads and executes a program specified by the coder. To experience to 
 auto-run behavior you must load the file using LOAD with a ",8,1" suffix. If
 you use only ",8" you must type RUN manually, as is normal with a program
 loaded into basic memory space.

 The most common use of a program like this would be to make it the first file
 on a disk and instruct end-users to load it using LOAD "*",8,1. The end-user
 doesn't have to type RUN after it loads, it just starts. Many professional
 games, demos and utilities used this technique to display messages and graphics
 while the main program is loading.

 There are two very simple configuration items that you can change at the top of
 the autorun.s source file that specify the program to load and the address of
 the program to execute.

 This code is public domain and you may do whatever you want with the source.

 Special Thanks To:

 MagerValp for his nice loadkoala code that is used on the demo disk image.

 Assassin of Willow for his piece of art titled "Tentacle" that is used on the
 demo disk image.
 
 Greg King for his assembly code size optimization suggestions. 

 Uz for his help in locating C64 basic error message routines and his continuing
 work on the cc65 compiler. 

 Developed using cc65 version 2.9.0.

 Code Author:
 Michael McIntosh <cc65@lifepod.com> - 2003.02.14

 "make disk" to produce "autorun.d64" (requires petcat and c1541)
