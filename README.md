# Introduce-PEDA
https://github.com/longld/peda
#Subject

+ Summary of peda

* How to install peda

* Point of Peda’s functions


##Summary of Peda
Enhance the display of gdb

+ colorize and display disassembly codes
+ registers, memory information during debugging
+ create pattern and shellcode for exploit
+ some utilities

Peda has many utilities for helping exploit.
Using Peda, you can decrease needless time.


##Setup


**You can download pedal using:**

` git clone https://github.com/longId/peda `

**To set it up add the following to ~/.gdbinit file**

`echo “source ~/peda/peda.py” >> ~/gdbinit`

**Making the following modification to ~/peda/lib/config.py is also recommended:**

```
-    "debug"     : ("off", "show detail error of peda commands, e.g: on|off"),
+    "debug"     : ("on", "show detail error of peda commands, e.g: on|off"),
```

##Problem

![problem](http://i.imgur.com/j5cN6EA.png)

It has a problem with gdb version.
Peda had developed by python 2.7 but Ubuntu 13.04 or later versions don’t support python 2.7.
so we can’t use peda in the latest ubuntu version.

I have some solutions for solve this problem

+ Downgrade ubuntu version 13.04 or lower versions
+ Downgrade gdb version to 7.4 
+ Download the other peda that someone change the peda can use in latest ubuntu version

Peda source had been uploaded to github so we can download the peda that someone fixed the problem.


##Downgrade Ubuntu version

Download ubuntu to following this links :

[Ubuntu 12.04 32bit](http://releases.ubuntu.com/12.04.5/ubuntu-12.04.5-desktop-i386.iso)

[Ubuntu 12.04 64bit](http://releases.ubuntu.com/12.04.5/ubuntu-12.04.5-desktop-amd64.iso)

[Ubuntu 13.04 32bit](http://old-releases.ubuntu.com/releases/13.04/ubuntu-13.04-desktop-i386.iso)

[Ubuntu 13.04 64bit](http://old-releases.ubuntu.com/releases/13.04/ubuntu-13.04-desktop-amd64.iso)


##Downgrade gdb version

**To change gdb version, we have to install Synaptic**

```
$ sudo apt-get install synaptic
$ sudo synaptic
```

```
settings -> repositories -> other software -> add
deb http://kr.archive.ubuntu.com/ubuntu/ precise main
```
and click add source

next, Reload and search gdb on Quick filter

`Select gdb -> Package -> Force version -> choose 7.4 version -> Apply`


##Download other peda

Download peda like original. just we have to change ubuntu git address.

```
git clone https://github.com/crowell/p3da.git ~/peda
git clone https://github.com/zachriggle/peda.git ~/peda
git clone https://github.com/akiym/pedal.git ~/peda
```

Finally we can use pedal on latest ubuntu version!
きもち>_<




##General usage and features

**Checksec**

+ Check for various security options of binary

![cs](http://i.imgur.com/oxdoVj5.png)




**Binary disassemble**

+ colorize and display disassembly codes

![bd](http://i.imgur.com/yAsbJAy.png)




**Context registers**

+ There are three commands to show context

![cr](http://i.imgur.com/mQ208Qd.png)

+ **context reg** for the registers and flags
+ **context code** for disassembling around the current instruction pointer
+ **context stack** for examining the stack




**trace call**

+ Peda can also infer the arguments to functions or the operands for comparisons and display them.

![tc](http://i.imgur.com/dznHVMy.png)




**Pattern create and search**

+ Creating exploit patterns and searching pattern in stack

![pc](http://i.imgur.com/gt4XG4c.png)
![ps](http://i.imgur.com/J88COQX.png)




**Find**

+ search string or address in memory or libc

![f](http://i.imgur.com/cGoOVeY.png)




**Dumprop & Ropgadget**

+ Get common ROP gadgets of binary or library

![f](http://i.imgur.com/jm3YpFe.png)




**Shellcode generate**

+  Generate or download common shellcodes.

![sg](http://i.imgur.com/4aWcbqi.png)




**Skeleton**

+ Generate python exploit code template

![sk](http://i.imgur.com/cfEd3zd.png)




#Reference

[https://github.com/longld/peda](https://github.com/longld/peda)

[https://hwchen18546.wordpress.com/2014/12/17/linux-install-gdb-peda-in-ubuntu-14-04/](https://hwchen18546.wordpress.com/2014/12/17/linux-install-gdb-peda-in-ubuntu-14-04/)

[http://ropshell.com/peda/Linux_Interactive_Exploit_Development_with_GDB_and_PEDA_Slides.pdf](http://ropshell.com/peda/Linux_Interactive_Exploit_Development_with_GDB_and_PEDA_Slides.pdf)




   
#Feedback

> wbvcos@gmail.com




### *I have some questions!*

[Issue](https://github.com/imkimchi/Introduce-PEDA/issues)
