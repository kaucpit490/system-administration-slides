---
layout: center
hideInToc: true
---

# Table of Contents

<Toc columns="2" maxDepth="1" mode="all" class="toc-list"/>

---

## Course Website

[https://cpit490.gitlab.io/ ↗️](https://cpit490.gitlab.io/)

- Check the course website every day! (I'm serious)
- To make it easy for you to track topics and schedule:
  - Go to the calendar
  - Always do the readings before the class
  - The current/active week is highlighted differently
- Lecture slides are also listed on the course website
  - The slides are rendered directly in the browser
  - They are just web pages, so no special software is needed.

---
layout: full
---

# Course Road Map

<br>

![](https://cpit490.gitlab.io/images/cpit-490-course-overview.png)

---
layout: center
---

# Course Syllabus

[https://cpit490.gitlab.io/syllabus/ ↗️](https://cpit490.gitlab.io/syllabus/)
- Read it! It serves as the contract between us.
- > Be prepared, there will be a quiz on the syllabus in the next lecture.

---

## Teaching Philosophy

- Use MS Teams for communication and assignment submissions
- I'm here for you!
  - I want you to participate, interrupt me when you have a question, and ask me to slow down if I'm going too fast!
  - Every question is important
  - Help each other
  - Hands-on instructions are incredibly rewarding and engaging
  - Need help after class? DM me on Teams
- I will be demoing examples in the lectures
  - You will be asked to apply what you've learned in the class
- Apply and deploy. You won't learn by just watching, learn by doing!

---

## Late Policy, Use of AI tools, and Special Accommodations
- Assignments submitted late will incur a 25% penalty.
- You may submit an assignment or a lab activity up to one week late.
  - after that the submission will not be graded and you’ll receive 0 points for it.
  - **Exception**: Every student gets three free late passes, allowing you to submit a maximum of 3 assignments up to 1 week past the due date without penalty.
- If you discover that you cannot attend the midterm or final exam, you will need to provide me with relevant documentation ASAP before the midterm or final exam to make other arrangements.
- Read the syllabus [statement on the use of generative AI tools ↗️](https://cpit490.gitlab.io/syllabus/#policy-on-the-use-of-generative-ai-tools)
- Disability Accommodations:
  - Please be open in communicating any requests for accommodations due to disability no later than the second week of the semester.

---
layout: center
---


## Basic Administration
- Essential duties of a system administrator
- History and background of UNIX and Linux systems
- UNIX and Linux Distributions

---

## Essential duties of a system administrator (I)
- Controlling access
  - Creating and removing accounts for users.
  - Account management is usually done using a configuration management system or a user directory service.
- Adding and configuring hardware
- Automating tasks
  - Reduce the amount of manual operations to automate repetitive tasks.

---

## Essential duties of a system administrator (II)
- Installing and upgrading software
- Performing scheduled backups
- Monitoring
- Tunning performance
- Troubleshooting network problems
- Working with vendors and cloud providers

---

## Related Disciplines
- DevOps
- Site reliability engineers
- Security operation engineers
- Network administrators
- Database administrators
- Data center technicians
- system architects

---

## Introduction to UNIX/LINUX
### History
- In 1969, a team at Bell Labs laboratories developed a new operating system named UNIX.
- UNIX was mostly found in large corporations and government environments due to licenses and cost issues.
- In 1991, Linus Torvalds in Helsinki, Finland, started working on a UNIX-like operating system that's free and open-source.


- A community of developers joined the effort and released version 1.0 of the Linux kernel with Torvalds in 1994.
- Today, Linus Torvalds and thousands of collaborators maintain the Linux kernel.
- A large community of developers maintain a large number of Linux distributions or distros, the Linux kernel with a collection of software packages.


- A Linux distribution comprises the Linux kernel, tools and libraries, a window system, and a desktop environment (GUI).
- Hundreds of Linux distributions exist. Some are commercially supported distros for enterprises.
- Popular Linux distributions: 
  - Debian GNU/Linux
    - Ubuntu Linux
  - Red Hat Enterprise Linux (RHEL)
    - CentOS


---

### Why Linux
- Within cloud computing and server environments, Linux is the operating system for practical reasons:
  - Stable and current
  - Runs on a wide range of architecture
  - Low resource/hardware requirements
  - Uses Unix's modular design
  - Multi-user and multiprocessor support
  - Free and open-source

---

## Where to host it?
- Private data center
- Public cloud provider (e.g., AWS, GCP, Azure)
  - The most practical choice
  - No need to incur management cost
  - They innovate rapidly

---

### Installation, demo, and Overview

---

### Logging in and out
- Linux has two basic modes:
  - Graphical mode: nicer but consumes system resources
    - Examples: Gnome and KDE desktops
  - Text mode: the usual black text console screen

---

### Logging in and out
 - login: you enter your username and password
 - logout: use the _logout_ or _exit_ command

---

### Basic commands

| Command	   |      Meaning                                 |
|----------|:-----------------------------------------------:|
| ls |  List directory contents |
| cd directory | change directories  |
| passwd |  change the password for the current user |
| file filename	 |  determine file type |


| Command	   |      Meaning                                 |
|----------|:-----------------------------------------------:|
| cat textfile | throws content of textfile on the screen  |
| pwd	display  |  present working directory |
|  exit or logout|   leave this session|
| man command	 |  read man pages on command |
| apropos | search the manual page names and descriptions |


---

### The UNIX/Linux Filesystem

> The purpose of a filesystem is to organize the system's storage resources.

---

### Filesystem main components

 1. A namespace: How to name things and organize them in a hierarchy
 2. An API: a set of system calls for manipulating things
 3. Security models: schemes for protecting, hiding, and sharing things
 4. An implementation: software that talks to the underlying hardware

---

 ### The Linux kernel supports many different types of filesystems:
 
  - _ext4_, the predominant type
  - _XFS_
  - _UFS_
  - Non-Linux filesystems: _FAT_ and _NTFS_

---

### Pathname
- A pathname refers to the route to a unique location in the tree structure of the filesystem. The pathname can be described as:
  - Absolute pathname: starts with a slash on the left, e.g. /etc/passwd
  - Relative pathname: does not start with a slash. It's relative to the present working directory (pwd) e.g. etc/passwd

```bash
$ /home/khalid/scripts/bash/script.sh ## absolute pathname
$ cd /home/khalid/                    ## absolute pathname
$ scripts/bash/script.sh              ## relative pathname
```

---

### Mounting and Unmounting
- External storage media devices can be mounted in any directory created by the user.
  - Typically in `/mnt/`
- The `mount` command is used to mount a device and `umount` to unmount it.

```bash
$ mount /dev/cdrom /mnt/cdrom
$ umount /mnt/cdrom
```

---

### Organization of the file tree
| Pathname        | Contents           |
| --------------- |--------------------|
|   /bin   and /sbin       |    Core Operating system commands.                |
|    /boot             |    Boot loader and files needed by the kernel.                |
|    /dev             |   Device entries for disks, printers, etc.                |
|     /home            |  Default home directories for users.                  |
| /root | The home directory for the root user (sometimes just /).  |



| Pathname        | Contents           |
| --------------- |--------------------|
|      /lib           |    Libraries, shared libraries, and commands used by /bin and /sbin
|   /mnt             | Temporarily mount points for removable media. |
|   /tmp              |     Temporarily files that disappear after reboot.               |
| /user | Hierarchy of secondary files and commands (/usr/bin, /usr/lib, etc.). |
| /var | System-specific data and configuration files. |


---

### File types (I)
- Linux uses a symbol to indicate the file-type.
- The symbol is the first 

```bash
$ ls -l
total 4
-rw-r--r--  1 khalid  staff    0 Sep 22 17:49 README.md
drwxr-xr-x  6 khalid  staff  204 Sep 22 16:59 content
drwxr-xr-x  4 khalid  staff  136 Aug 28 22:36 static
drwxr-xr-x  3 khalid  staff  102 Aug 28 22:36 themes
```

---

### File types (II)
| File Type | Symbol |
|-----------|--------------------|
| Regular file | - |
| Directory | d |
| Hard link | c |
| Character and block device files | b |
| Socket | s |
| Named pipe | p |
| Symbolic link | l |

---

### File Access Attributes
- Every file has a set of nine bits called permission bits to control who can read, write, or execute the content of the file.
- The permissions are distributed into three user catergories: user owner (_u_), users in the same group (_g_), and all other users (_o_).
- Permission bits are represented in binary, octal, or character symbols.
- Each permission may be 'on' or 'off' for each of the three categories of users: owner, group, and other.

---

### File Access Attributes (Cont.)
![](./images/file-permission-bits.png)

---

### Inspecting files using ls
```bash
$ ls -l my-script.sh
-rwxr-xr--  1 khalid  staff  0 Sep 22 17:49 my-script.sh
```
- There are read (_r_), write (_w_), and execute (_x_) permissions. 
- The symbol _-_ indicates the permission is turned off.
![](./images/ls-file-ownership-permissions.png)

---

###### Numerical Representation
| Numerical | letter | Meaning |
|--|----|-------------------------|
| 7| rwx| read, write, and execute|
| 6| rw-| read and write|
| 5| r-x| read and execute|
| 4| r--| read-only|
| 3| -wx| write and execute|
| 2| -w-| write only|
| 1| --x| execute only|
| 0| ---| none

---

### Changing permissions using chmod

```bash
# Everybody has full access:
$ chmod 777 main.java
# Owner has full access:
$ chmod 700 main.java
# Owner has full access, group members have read-only access:
$ chmod 740 main.java
```

```bash
# All users have read and write access:
$ chmod a=rw main.java
# User has read and write access:
$ chmod u=rwx main.java
# Group members have read access:
$ chmod g=r main.java
```

```bash
# Add the execute (x) permission to the user:
$ chmod u+x main.java
# Deny the execute (x) permission from the user:
$ chmod u-x main.java
```

---

### Changing file owner and group using chown

```bash
# changing the owner of a file
$ sudo chown ali main.java 
# changing the owner of a directory
$ sudo chown ali ./src/
# changing the owner of a directory and its subdirectories
$ sudo chown -R ali ./src/
```

```bash
# changing the owner and group of a file
$ sudo chown root:staff main.java
# changing the owner and group of a directory
$ sudo chown root:staff ./src
# changing the owner and group of a directory 
#          and its subdirectories
$ sudo chown -R root:staff ./src/
```

---

### The UNIX/Linux Philosophy

> Do One Thing and Do It Well


> "This is the Unix philosophy: Write programs that do one thing and do it well. Write programs to work together. Write programs to handle text streams, because that is a universal interface."

Doug McIlroy

---

### Shell Types
- A shell is a user interface for accessing the operating system.
- Shells are either command-line interface (CLI) or graphical user interface (GUI).
- Text (CLI) shell types:
  - __sh__ the basic shell in UNIX-related environments.
  - __bash__ or Bourne Again shell: the standard shell for common users.
  - __zsh__ An extended Bourne shell with signifcant improvements.

---

### Common shell programs
- _ls_: lists the content of a directory
- _grep_: searches text
- _wc_: counts lines, words, and characters
- _sort_: sorts lines
- _uniq_: prints unique lines
- _head_: reads the beginning of a file
- _tail_: reads the end of a file

---

### Communication Channels
- Every process has at least three communication channels:
  - Standard Input (stdin)
  - Standard Output (stdout)
  - Standard Error (stderr)
- In most interactive text shells, stdin reads from keyboard, stdout and stderr writes outputs to the screen.
- These communication channels can be redirected into a file or piped into the stdin of another program or command.

---

### Redirection (I)
- Communication channels can be redirected into a file
- The symbols `<`, `>`, and `>>` are used to redirect a program's input or output to or from a file. 
  - _>_ Redirects stdout. It creates a file or replaces its content if it exists.
  - _>>_ Redirects stdout. It appends to the existing file's content.

```bash
$ ls /home > users.txt ## stdout to a file (create or replace)
$ ls /home >> users.txt ## stdout to a file (create or append)
```

---

### Redirection (II)
<!-- .slide: style="text-align: left;"> --> 
- The symbol _2>_ is used to redirect stderr into a file.

```bash
$ find /etc -name network 2> error.log
```

- Redirect stdout and stderr into two different files.

```bash
$ find /etc -name network > out.txt 2> error.log
```
  
  - _>_ sends stdout to a file named out.txt
  - _2>_ sends stderr to a file named error.log

---

### Pipes
- Pipes are used to connect the stdout of one command into the stdin of another command.
- Pipes use the pipe symbol _|_ 
  - piping into _wc_ tool, which counts how many lines, words, and characters.

  ```bash
$ ls /etc | wc -l
  ```
  - Counting how many bash users by using the search tool _grep_ and piping into _wc_.

  ```bash
$ grep bash /etc/passwd | wc -l
  ```


### Scripting and Automation
- It's important for a sysadmin to incorporate automation into your daily work.
- Automation is done through writing scripts.
- Whenever you encounter a repetitive task, automate it in a script.
- Examples:
  - Storing backups in two different data centers.
  - Checking if an application or a process has crashed accidently.
  - Creating, configuring, and deploying a cloud service in one command.


### From commands to script
- A typical shell script contains a list of commands
- These commands are exactly the same commands you run in a bash shell
- The script may also include control flow statements, loops, and functions.



### Bash Script Examples (I)
<!-- .slide: style="text-align: left;"> --> 

1) Hello World Example

_script.sh_
```bash
#!/bin/bash
foo="HELLO WORLD!!!"
echo $foo
```
_Running/Execution:_

```bash
# make it executable
chmod u+x script.sh
# run it
./script.sh 
# or
bash ./script.sh
```

---

### Bash Script Examples (II)
<!-- .slide: style="text-align: left;"> --> 
2) Creating an archive (i.e., compressing a directory)
```bash
#!/bin/bash
target="/home/khalid/backup/archive.tar"
tar -cvf $target /home/khalid
```

3) Passing arguments to the bash script

_archive-maker.sh_
```bash
#!/bin/bash
echo "creating an archive file using tar -cvf $0 $1"
tar -cvf $0 $1
```
_Run it:_
```bash
bash ./archive-maker.sh output.tar /path/to/dir
```

---

### Reading Input
```bash
$ echo -n "Proceed? [y/n]: "
$ read ans
$ echo $ans

```

---

### Loops
- The _for ..in_ construct is used to perform loops/iteration.
- Example: copy shell script files (*.sh files) into a directory called _bin_.

```bash
srcDir=/home/khalid
targetDir=/home/khalid/bin
mkdir $targetDir
for scriptFile in $srcDir/*.sh; do
  echo "Moving $scriptFile into $targetDir"
  mv $scriptFile $targetDir
done
```

---

### Exercise (in-class activity)
- Modify the previous bash script to accept command line arguments instead of hard coded source and target path name values. Example:

```bash
$ bash move-sh-files.sh ~/ ~/bin
```

---

### Control Flow Statements

```bash
x=5
if [ $x -eq 5 ]
  then
  echo "$x equals 5"
elif [ $x -lt 5 ]
  then
  echo "$x is less than 5"
elif [ $x -gt 5 ]
  then
  echo "$x is greater than 5"
fi
```

---

### Functions (I)

- Declaring and calling bash functions

```bash
#!/bin/bash 
quit() {
  exit
}
hello() {
  echo Hello!
}
hello
quit
echo "End!"
```

---

### Functions (II)
- Passing parameters to a Bash function

```bash
#!/bin/bash 
my_function() {
  echo "In my_function"
  echo $1 $2 $3
  echo "End!"
}
my_function "Learn" "Bash" "Functions"
```

---

### Environment Variables (I)
- Bash uses certain global variables or environment variables. 
- Examples:
  - $PATH
    - Contains a colon-separated list of directories in which the shell looks for commands.
  - $HOME
    - Contains the path of the current user's home directory.

---

### Environment Variables (II)
- When you type a command you installed recently by its name and get an error message that says: "X: command not found", that means it's not available in your $PATH variable.
- You need to add it to your _$PATH_ environment variable.

---

### Environment Variables (III)
- To add a command to your $PATH variable, you need to edit the `~/.bash_profile` file.
  - Append the path of your tool into the PATH variable
```bash
PATH=$PATH:$HOME/.local/bin:$HOME/bin:/path/to/mytool
export $PATH
```
- Save the file and login again or run the command: 
```bash
source ~/.bash_profile
```

---

### Other Scripting Languages
- There're many general-purpose scripting languages that offer easy to read syntax and have an extensive set of standard libraries.
- Examples include, Perl, Python, and Ruby.
- Python is a widely used scripting language for system adminstration scripting.
- In addition to Bash scripting, it's expected for a system administrator to be familiar with a language like Python.

