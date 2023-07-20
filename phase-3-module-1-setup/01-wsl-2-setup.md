# Windows WSL 2 Setup

Welcome Windows users! Your operating system comes from a different lineage than
most operating systems. Windows has its roots in MS-DOS and Windows NT, while
macOS and Linux both are "Unix" style operating systems.  We will be using the
Unix command line in this course so everyone in class is using the same command
line tools and programs.  Windows does not include a unix style system by
default, so we are going to use an add-on piece of Microsoft Technology called
"Windows Subsystem for Linux" (WSL).

## WSL

Windows Subsystem for Linux (WSL) is a Linux Virtual Computer that you run on
your PC.  It gives you all the same tools and command line utilities that your
mac and Linux-using classmates use.

To install WSL 2 you must have a specific version of Windows 10 or Windows 11.

> For x64 systems: Version 1903 or higher, with Build 18362 or higher.

If you do not have this version or cannot update to this version, please
contact an instructor.

## Installing WSL

Future versions of Windows will include an automatic installer for WSL, but
for now you will have to use the manual install instructions:

[Windows Subsystem for Linux Installation Guide for Windows 10]

Follow this guide to install WSL 2 and Ubuntu Linux.

## Tips for using WSL

You will launch the __Ubuntu terminal__ when the instructions in our curriculum
tell you to open a Terminal.

__You should always store your code files in your Ubuntu home directory, and not
in your Windows users home directory on your C: drive.__ Many of the tools we
use will perform better and be more stable if the files exist on the Ubuntu
filesystem.

If you need to access the files in your Ubuntu home directory from Windows
Explorer you can type `Windows + R` to bring up the run command dialog. Then
type `\\wsl$\home\<your-user>` replacing `your-user` with your Ubuntu user name
(you can find this out by typing `whoami` at your Ubuntu terminal prompt.)

If you want to access your Windows hard drive from Ubuntu you can use the path
`/mnt/c` inside of the Ubuntu virtual machine. You should open project files in your
Ubuntu files, not from your Windows files. Move project files from your Windows file
system to your Ubuntu file system before opening and changing project files.

If you ever need to restart the Ubuntu virtual machine, you need to open a
Powershell window and run the following command:

```shell
wsl --shutdown
```

Next time you open the Ubuntu terminal it will start the virtual machine back
up.


[Windows Subsystem for Linux Installation Guide for Windows 10]: https://docs.microsoft.com/en-us/windows/wsl/install-win10#manual-installation-steps
