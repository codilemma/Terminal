## NotesNcode for:

A Practical Guide to Linux Commands, Editors, and Shell Programming, Fourth Edition
queue
- By Mark G. Sobell, Matthew Helmke

### Correcting Terminal Mistakes
- 'Backspace': erases a single character
- 'Cntrl+w': deletes a word
- 'Cntrl+u': deletes a line

- 'Cntrl+z': suspends a program if you fup and hit enter with a typo
- 'Cntrl+c': terminates a program

### Repeating/Editing Commands
- use arrow keys stupid
- '!!': repeats the previous command
- 'sudo !!': repeats previous command with root privileges

### Ultimate POWER! - sudo
- 'sudo -s': spawns a new terminal with root privileges

### Exploring the System Manual Pages
- 'man' + command name: displays the manual page 
- Linux system manual pages
    1. User Commands
    2. System Calls
    3. Subroutines
    4. Devices
    5. File Formats
    6. Games
    7. Miscellaneous
    8. System Administration
    9. Kernel
    10. New
- 'man' + page# + command name: specifies wich page to look in for command.
- 'man -a' + command name: view all pages for command.
- 'man -k' + keyword: searches for commands based on a keword
- 'apropos' + keyword: searches for commands based on a keyword ('apropos make')

### System Manual Page ('man') alternatives
- 'whatis' + keywords: searches for only complete word matches 
- 'info' + command name: displays more complete and up-to-date information on GNU utilities than 'man'. displays a copy of 'man' page for non GNU utilities
    * press 'h' or '?' to list info commands
    * press SPACE to scroll
    * press '/'+ regex to search
- [TODO] explore the 'pinfo' package as an alternative to info.

### Docs from the terminal. Does not launch a pager
- command name + '--help'
- you can pipe to a pager if needed. ('ls --help | less)

### Bash Docs
- 'help' + command name: displays info about bash commands, control structures, and other features.

### Finding Help Locally
- look in the following directories (kernel source code must be installed)
    * /usr/src/linux/Docuentation
    * /usr/share/doc

### Basic utilities
- 'ls': Lists the Names of Files in the current directory
- 'cat'+ file name: Displays a Text File
- 'rm' + file name: Deletes a File
    * ALWAYS use the interactive option for safety ('rm -i' + filename)
    * You can also alias to make 'rm' = 'rm -i'
- Pagers:
    * Utilites used to display text one page at a time.
    * 'less' + file: more features
    * 'more' + file: less features
    * just remember that less is more
- 'hostname': Displays the System Name.
- Filename completion: press Tab after entering a few characters
- 'cp' + source-file + destination file: copies a file.
    * caution, cp can destroy the source file if it exists. use the -i option
- 'mv' + existing-filename + new-filename: Changes the Name of a File
    * can also destroy a file
- 'lpr' + filename: Prints a File (sends it to the print queue)
- 'lpq' or 'lpstat -o': See the jobs in the print queue
- 'lprm' + print-job#: removes print job from the print queue
- 'grep' + string: searches through one or more files for the string.
    * $ grep 'grep' README.md
    * g = global, re = regular expression, p = print
- 'head' + filename: displays the beginning of a file
    * by default the first ten lines are specified.
    * display any number of lines by using 'head -#' + filename:
    



***
### Exercises
#### Chapter 1
1. What is free software? List threee characteristics of free software.
2. why is Linux popular? why is it popular in academia?
3. What are multiuser systems? Why are they successful?
4. What is the Free Software Foundation/GNU? Wha is Linux? Which parts of the linux operaing system did eah provide? Who else has helped build and refine this operating system?
5. In which Language is Linux writen? What does the language hav eot do with the sucess of Linux?
6. What is a utility program?
7. What is a shell? How does it work with the kernel? With the user?
8. How can you use utility prorams ad a shell to create your own applications?
9. Why is the Linux filesystem referred to as hierarchical?
10. what is the difference between a multiuser and a multi-tasking system?
11. Give an example of when you would want to use a multitasking system
12. Approximately how many poeple wrote Linux? Why is this project unique
13. What are the key terms of the GNU General Public License?

#### Chapter 2
1. How would you display a list of utilites that compress files?
2. How would you repeat the second preceding command line, edit it, and then execute it?
3. Briefly, what information does the '--help' option display for the tar utility? How would you display this information one screen at a time?
4. How would you display the man page for 'shadow' in section 5 of the system manual?
5. How would you change your login shell to tcsh without using root privileges?
6. How many man pages are in the Devices subsection of the system manual? (Devices is a subsection of Special files)
7. How can you use 'man' to determine which sections of the system manual contain a manual page with a given name.
8. How would you find out which Linux utilites create and work with archive files?

#### Chapter 3


***
### References
#### Chapter 1
- http://www.gnu.org/philosophy/free-sw.html 
- History of UNIX and GNU-Linux: http://www.levenez.com/unix 
- Founder of GNU movement, Richard Stallman: http://www.stallman.org/ 
- http://www.gnu.org/gnu/initial-announcement.html 
- http://www.gnu.org/gnu/manifesto.html
- http://www.gnu.org/software/hurd/hurd.html 
- GNU runs on Free BSD: http://www.freebsd.org/ 
- And NetBSD: http://www.netbsd.org/
- http://www.gnu.org/software/hurd/microkernel/machgnumach.html
- http://www.gnu.org/software/hurd/hurd-and-linux.html
- http://www.gnu.org/philosophy/free-sw.html 
- http://www.gnu.org/gnu/linux-and-gnu.html
- free software foundation: http://www.fsf.org/ 
- GNU General Public License (GPL): http://www.gnu.org/licenses/licenses.html
ew
- http://www.ibm.com/linux 
- Xen VirtualMachineManager:http://www.cl.cam.ac.uk/research/srg/netos/xen 
- http://www.cl.cam.ac.uk/research/srg/netos/xen 
- Kernel-based Virtual Machine (KVM)
    * http://www.linux-kvm.org/ 
    * http://libvirt.org/
- Qemu: wiki.qemu.org 
- http://www.virtualbox.org/
- Desktop Managers:
    * http://www.gnome.org/
    * http://www.kde.org/

#### Chapter 2
- http://www.sudo.ws/
- menu-based hypertext:http://www.gnu.org/software/texinfo 
- Linux Documentation Project: http://www.tldp.org/

#### Chapter 3