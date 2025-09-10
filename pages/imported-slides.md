---
layout: center
hideInToc: true
---

# Table of Contents

<Toc columns="2" maxDepth="2" mode="all" class="toc-list"/>

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
src: ./roadmap.md
---




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

# Part 1: System Administration Duties and Background

- Essential duties of a system administrator
- History and background of UNIX and Linux systems
- UNIX and Linux Distributions

---

## Essential Duties of a System Administrator
<v-clicks>

- **Controlling access** - Managing user accounts, permissions, authentication
- **Adding hardware** - Installing, configuring, and maintaining system hardware
- **Automating tasks** - Creating scripts and workflows to reduce manual work
- **Scheduling backups** - Ensuring data protection and disaster recovery
- **Installing and upgrading software** - Package management and system updates
- **Monitoring** - System performance, resource usage, and health checks
- **Troubleshooting** - Diagnosing and resolving system issues
- **Maintaining local documentation** - Keeping system documentation current
- **Monitoring security** - Implementing security measures and monitoring threats
- **Tuning performance** - Optimizing system resources and performance
- **Developing site policies** - Creating standards and procedures
- **Working with vendors** - Managing vendor relationships and support
- **Incident Response/ Postmortems** - Handling emergency situations and critical issues

</v-clicks>

---

## Related Disciplines

- **DevOps**: Combines development and operations practices to automate software delivery using continuous integration/deployment (CI/CD), infrastructure as code, etc.
- **Site reliability engineers**: Focus on automation, observability, and reliability of large-scale systems.
- **Security operation engineers**: Monitor and protect systems from security threats, implement security controls, respond to incidents, and maintain security compliance
- **Network Administrators**: Manage network infrastructure, configure networking equipment, monitor performance, and ensure network security and reliability
- **Database administrators**: Maintain database systems, handle backups/recovery, optimize performance, and ensure data security and integrity
- **Data center technicians**: Maintain physical infrastructure, handle hardware installation/repairs, manage power/cooling systems, and ensure facility operations
- **System architects**: Design system infrastructure, plan scalability strategies, create technical specifications, and make high-level technology decisions

---

## Operating Systems managed by System Administrators

<br>

- **Linux**:
  - Industry standard; powers approximately 90% of cloud infrastructure and enterprise servers.
- **Windows Server**:
  - Commonly used for running and testing .NET applications and Microsoft-specific products and services (e.g., Active Directory).
- **macOS** (on Mac mini hardware): Used for running and testing applications in cloud-based macOS environments.

---

## Unix and Linux History
- In 1969, a team at Bell Labs laboratories developed a new operating system named UNIX.
- UNIX was mostly found in large corporations and government environments due to licenses and cost issues.
- In 1991, Linus Torvalds in Helsinki, Finland, started working on a UNIX-like operating system that's free and open-source.
- A community of developers joined the effort and released version 1.0 of the Linux kernel with Torvalds in 1994.
- Today, Linus Torvalds and thousands of collaborators maintain the Linux kernel.
- A large community of developers maintain a large number of Linux distributions or distros, the Linux kernel with a collection of software packages.


---

## Linux and Unix Distributions

- Distribution = OS kernel + system tools + GUI (optional)
- Hundreds of distributions exist. Some community-driven and others enterprise-grade.

- **Linux Distributions**
  - **Debian:** One of the oldest Linux distro known for stability with minimal size.
  - **Ubuntu Server**: Debian-based known for ease of use and wide community support.
  - **Red Hat Enterprise Linux (RHEL)**: Enterprise standard.
  - **Rocky Linux**: Free RHEL alternatives and replacement for the discontinued CentOS Linux distribution.

- **Unix Distributions/BSD Variants**

  - **FreeBSD**: Server environments security and stability focused.
  - **OpenBSD**: Security-first design
  - **NetBSD**: Highly portable across platforms

---

## Why Linux
<br>

- Within cloud computing and server environments, Linux is the operating system of choice for practical reasons:
  - Stable and always receives updates
  - Runs on a wide range of architecture
  - Low resource/hardware requirements
  - Uses Unix's modular design
    - Small programs that do one thing and can be combined to perform complex tasks.
  - Multi-user and multiprocessor support by design
  - Secure, permission-based file system.
  - Free and open-source

---

## Where to Run Linux?

<br>
<v-clicks>

1. **Bare Metal Installation**
   - Direct installation on computer hardware
   - Full hardware access and performance

</v-clicks>

<v-clicks>

2. **Virtualization (Type 2 Hypervisor)**
   - Create virtual machines running Linux alongside the host OS.
   - Install hypervisor software (VirtualBox, VMware) on host OS to run multiple guest OSs simultaneously

</v-clicks>

<v-clicks>

3. **Docker Containers**
   - OS Virtualization: Lightweight, isolated environments that share host OS kernel
   - Widely used for application deployment

</v-clicks>

<v-clicks>

4. **Cloud Providers**
   - Virtualization on the cloud
   - Instant VM deployment (AWS, GCP, Azure)
   - Cost varies by usage, region, VM instance type

</v-clicks>

---

## Installation, Demo, and Overview

- Virtualization: 
  - Windows: Virtual Box
  - macOS: UTM
- Cloud:
  - Azure Virtual Machines
    - ⚠️ **Caution:** When you are done, make sure to delete the VM and all associated resources to avoid ongoing charges.

---

### Shell Types and Interfaces
- Linux has two basic interfaces:

1. **Command Line Interface (CLI)**:  
   - Command-line interface (black screen with text)
   - Lightweight and efficient
   - Default mode for servers and remote administration

2. **Graphical mode (GUI)**
   - User-friendly interface with windows, icons, and menus
   - Requires more system resources
   - Common desktop environments: GNOME, KDE

---

## Logging In
<br>

### Local Login (Terminal or GUI):
- Enter username and password

<br>

### Remote Login via SSH:

`ssh username@hostname`

- Authentication can be either of two methods:

  - **Password-based**: Prompted to enter your Linux user password (not secure)
  - **Public-Key Cryptography**: More secure; uses a public/private key pair.
    - You upload the public key into the remote Linux machine.
    - You keep the private key on your local machine.
    - Private key should be protected by a passphrase
    - SSH Key-pair are generated using the `ssh-keygen` command line tool.

---


## Generating SSH Key Pair for Authentication (I)

- You will generate SSH key pair
  - Public Key 🔓: Copied to the server.
  - Private Key 🔑: Stays on your computer.
- Private keys should be protected with a passphrase.

<!-- Light mode image -->
<LightOrDark>
  <template #light>
    <img src="/images/ssh-private-public-passphrase-key-light.png" alt="SSH key pair with a passphrase" />
  </template>

  <template #dark>
    <img src="/images/ssh-private-public-passphrase-key-dark.png" alt="SSH key pair with a passphrase" />
  </template>
</LightOrDark>



---

### Generating SSH Key Pair for Authentication (II)

- RSA:

```shell
ssh-keygen -t rsa -b 4096 
```

- ED25519:

```shell
ssh-keygen -t ed25519
```


---

### Generating SSH Key Pair for Authentication (III)

```shell
ssh-keygen -t rsa -m PEM -b 4096 -f ~/.ssh/my-vm-key
```

```text   
Generating public/private rsa key pair.
Enter file in which to save the key (/Users/khalidalharbi/.ssh/id_rsa): /Users/khalidAlharbi/.ssh/id_rsa_key
Enter passphrase (empty for no passphrase): 
Enter same passphrase again: 
Your identification has been saved in /Users/khalidAlharbi/.ssh/id_rsa_key
Your public key has been saved in /Users/khalidAlharbi/.ssh/id_rsa_key.pub
The key fingerprint is:
SHA256:UJRVo82P9h0JVpnoN3ucIvgpzoqnZ+AI5BrHPej57pM khalidalharbi@MacBookAir
The key's randomart image is:
+---[RSA 4096]----+
|       .oo..o ..o|
|       ..  + o.o |
|      .   . +o   |
| .     .    .+.o.|
|o. o    S . o o++|
|.o+ o.   . o o ++|
|.+..oo.   . o o o|
|. o.E..+.. o     |
|   +++=.oo.      |
+----[SHA256]-----+
```

---

### Logging in using SSH key pair

<br>
<br>

- We can use the SSH client to establish a secure connection to the remote server:

```shell
ssh -i ~/.ssh/id_rsa_key azureuser@20.173.96.68
```

  - `ssh`: The secure shell command for remote login
  - The `-i` flag specifies the path to your private key file.
  - `azureuser` is the username on the remote system
  - `20.173.96.68` is the IP address of the remote server 

---

### Powering Off and Shutdown
- The `shutdown` and `systemctl` commands can be used to power off the operating system gracefully.

- **Immediate shutdown**
```shell
shutdown -h now
# OR
systemctl poweroff
```

- **Scheduled shutdown**
```shell
shutdown -h +10 "System maintenance in 10 minutes"
```

- **Reboot**

```shell
shutdown -r now
systemctl reboot
```

- **Cancel scheduled shutdown**

```shell
shutdown -c
```

---


## Common Linux Commands

| Command	   |      Meaning                                 |
|----------|:-----------------------------------------------:|
| `ls` |  List directory contents |
| `cd` | change directories  |
| `passwd` |  change the password for the current user |
| `file` filename	 |  determine file type |
| `cat` textfile | throws content of textfile on the screen  |
| `pwd`	|  print working directory |
|  `exit` or `logout`|   leave this session|
| `man` |  read manual/help pages |


---

## The UNIX/Linux Filesystem
<br>

- The purpose of a filesystem is to organize the system's storage resources.
- Filesystem main components:
  1. **Namespace**: How to name things and organize them in a hierarchy
  2. **API**: a set of system calls for manipulating things
  3. **Security models**: schemes for protecting, hiding, and sharing things
  4. **Implementation**: software that talks to the underlying hardware

---

 ### Linux Filesystem Types

The Linux kernel supports several filesystem types:

**Native Linux Filesystems:**
- **_ext4_**: Default Linux filesystem with journaling and large volume support
- **_XFS_**: High-performance scalabile filesystem, optimized for large files and volumes
- **_Btrfs_ (B-tree Filesystem)**: Modern filesystem with snapshots and RAID support

**Non-Linux Filesystems:**
- **_FAT32_**: For USB drives and cross-platform compatibility. Can't handle files larger than 4GB.
- **_NTFS_**: Windows filesystem with permissions and encryption

---

### Pathname
- A pathname refers to the route to a unique location in the tree structure of the filesystem. The pathname can be described as:
  - **Absolute pathname**: starts with a slash on the left, e.g. /etc/passwd
  - **Relative pathname**: does not start with a slash. It's relative to the current working directory (pwd) e.g. etc/passwd

```bash
$ /home/khalid/scripts/bash/script.sh ## absolute pathname
$ cd /home/khalid/                    ## absolute pathname
$ scripts/bash/script.sh              ## relative pathname
```

---

### Special Directory References
- `.` (single dot): 
  - Refers to the current directory
  - Useful in relative paths (e.g., `./script.sh` runs script in current directory)

- `..` (double dot):
  - Refers to the parent directory
  - Used to navigate up directory levels (e.g., `cd ../..` moves up two levels)

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

### File Types (II)
- You can view a file's type using the `ls -l` command (first character) or using the `file` command

| Symbol | File Type | Description |
|--------|-----------|-------------|
| `-` | Regular file | Normal files like text, data, or executable programs |
| `d` | Directory | Contains references to other files and directories |
| `l` | Symbolic link | A special file that acts as a pointer/reference to another file or directory |
| `c` | Character device | Interface for character-oriented hardware, which handles data one byte at a time (e.g., terminals) |
| `b` | Block device | Interface for block-oriented hardware (e.g., disks), which handles data by block of bytes |
| `s` | Socket | Enables inter-process communication |
| `p` | Named pipe | Allows communication between processes without socket overhead |



---

### File Access Attributes (I)
- Every file has a set of nine bits called permission bits to control who can read, write, or execute the content of the file.
- The permissions are distributed into three user categories: user owner (_u_), users in the same group (_g_), and all other users (_o_).
- Permission bits are represented as either absolute (octal) or symbolic (character symbols).
- Each permission may for each of the three categories of users: owner, group, and other.
- Each of the three categories: owner, group, and others can have read, write, and execute permissions be turned 'on' or 'off'.
- File permissions are 4-digit
  - The first digit is optional and used for the special permission bits.
  - The second, third, and fourth digits are for the owner, group, and others.

---

### File Access Attributes (II)

- The "special bits" permissions are three extra permission settings: setuid, setgid, and sticky bit. 
- They are optional when using the `chmod` command
- They provide additional control beyond the standard read, write, and execute permissions

```
4  7  5  5
↑  ↑  ↑  ↑
|  |  |  +-- others (read and execute)
|  |  +----- group (read/write/execute)
|  +-------- owner (read)
+----------- special bits (setuid, setgid, sticky bit)
```


| Value | Bit        | Meaning                                     |
| ----- | ---------- | ------------------------------------------- |
| 4     | setuid     | Run as file **owner**, not as calling user  |
| 2     | setgid     | Run as file **group**, or set group on dirs |
| 1     | sticky bit | Only owner can delete files in a directory  |


---

### File Access Attributes (III)

- In absolute mode, permissions are set using octal numbers, where each digit represents the combined read (4), write (2), and execute (1).


![File Permissions in absolute mode](/images/file-permission-bits.png)

---

### Inspecting File Permission Modes

```bash
ls -l my-script.sh
-rwxr-xr--  1 khalid  staff  0 Sep 22 17:49 my-script.sh
```

- There are read (_r_), write (_w_), and execute (_x_) permissions. 
- The symbol _-_ indicates the permission is turned off.

![](/images/ls-file-ownership-permissions.png)

---

## Absolute Permission modes
| Octal Value | File Permissions Set  | Meaning |
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

### Changing permissions using `chmod` with an absolute mode

- Absolute Permission Modes:
```bash {class="large-code"}
# Everybody has full access:
chmod 777 main.java
# Owner has full access:
chmod 700 main.java
# Owner has full access, group members have read-only access:
chmod 740 main.java
```

---

### Changing permissions using `chmod` with a symbolic mode

- Symbolic Permission Modes:
  - Setting Permission using `=` will turn on the specified permissions and turn off all others.
```bash
# All users have read and write access:
chmod a=rw main.java
# User has read and write access:
chmod u=rwx main.java
# Group members have read access:
chmod g=r main.java
```

  - Adding or removing permissions using `+` or `-` will turn on the specified permissions and keep all others.

```bash
# Add the execute (x) permission to the user:
chmod u+x main.java
# Deny the execute (x) permission from the user:
chmod u-x main.java
```

---

### Changing file owner and group using chown

- The `chown` command is used to change file owner and group.
- `chown owner:group`
- The owner and group operands are both optional, however, one must be specified.  
- If the group operand is specified, it must be preceded by a colon (`:`) character.
- The `-R` option will recursively change the ownership of the directory and all its files and subdirectories.

```bash
# changing the owner of a file
sudo chown ali main.java 
# changing the owner of a directory
sudo chown ali ./src/
# changing the owner of a directory and its subdirectories
sudo chown -R ali ./src/
```

```bash
# changing the owner and group of a file
sudo chown root:staff main.java
# changing the owner and group of a directory
sudo chown root:staff ./src
# changing the owner and group of a directory and its subdirectories
sudo chown -R root:staff ./src/
```

---
layout: center
---

### The UNIX/Linux Philosophy

<br>
<br>

### "Do One Thing and Do It Well"

<br>

> **"This is the Unix philosophy: Write programs that do one thing and do it well. Write programs to work together. Write programs to handle text streams, because that is a universal interface."**
Doug McIlroy; E. N. Pinson; B. A. Tague, July 1978. "Unix Time-Sharing System: Foreword". The Bell System Technical Journal.


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
# stdout to a file (create or replace)
ls /home > users.txt

# stdout to a file (create or append)
ls /home >> users.txt
```

---

### Redirection (II)

- The symbol _2>_ is used to redirect stderr into a file.

```bash
find /etc -name network 2> error.log
```

- Redirect stdout and stderr into two different files.

```bash
find /etc -name network > out.txt 2> error.log
```
  
  - _>_ sends stdout to a file named out.txt
  - _2>_ sends stderr to a file named error.log

---

### Pipes

- Pipes are used to connect the stdout of one command into the stdin of another command.
- Pipes use the pipe symbol _|_ 
- piping into _wc_ tool, which counts how many lines, words, and characters.

- Example 1: List how many users (including system accounts) are on a Linux system

```shell
cat /etc/passwd | wc -l
```

  - Example 2: List how many users on the system have Bash set as their login shell by using the search tool _grep_ and piping into _wc_.

```shell
grep bash /etc/passwd | wc -l
```

---

## Scripting and Automation

- It's important for a sysadmin to incorporate automation into your daily work.
- Automation is done through writing scripts.
- Whenever you encounter a repetitive task, automate it in a script.
- Examples:
  - Storing backups in two different data centers.
  - Checking if an application or a process has crashed accidently.
  - Creating, configuring, and deploying a cloud service in one command.

---

### From commands to script
- Scripts are plain text files containing shell commands
- These commands are exactly the same commands you run in a bash shell
- The script may also include control flow statements, loops, and functions.


--- 

## Bash Scripting Syntax

- Scripts start with a shebang: `#!/bin/bash`
  - It tells the system which shell interpreter to use when executing the script directly (e.g., `./script.sh`).
- Each command is written on a new line
- Variables are assigned without spaces: `name="value"`
  - ⚠️ **Warning:** Do not use spaces before or after the `=` sign. Spaces are interpreted as command arguments, which will cause errors.
- Access variable values with the *\$*  symbol (e.g., `$name`)
- Comments start with `#`
- Use `echo` to print output
- Control flow: `if`, `for`, `while`, `case`
- Functions are defined with `function_name() { ... }`
- Scripts must be executable: `chmod +x script.sh`

---

### Bash Script Examples (I)

#### 1) Hello World Example

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
echo -n "Proceed? [y/n]: "
read ans
echo $ans
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
bash move-sh-files.sh ~/ ~/bin
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

### Environment Variables: PATH and HOME (I)
- Bash uses certain global variables or environment variables. 
- Examples:
  - $PATH
    - Contains a colon-separated list of directories in which the shell looks for commands.
  - $HOME
    - Contains the path of the current user's home directory.

---

### Environment Variables (II)
- When you type a command you installed recently by its name and get an error message that says: "X: command not found", that means it's not available in your $PATH variable.
- If a command is not found, it usually means its location is not included in the `$PATH` variable.
- The full path name of commands must be added to your _$PATH_ environment variable.

---

### Environment Variables (III)

- You can set or update your `$PATH` in your shell configuration file (e.g., `~/.bash_profile`, `~/.bashrc`, or `~/.zshrc`).
  - Append the path of your tool into the PATH variable.

```bash
PATH=$PATH:$HOME/.local/bin:$HOME/bin:/path/to/mytool
export $PATH
```

- Save the file and login again or run the command: 

```bash
source ~/.bash_profile
```

- ⚠️ **Warning:** Always append to the existing `$PATH` variable instead of replacing it. Do not set it directly, or you may lose access to essential system commands.

---

### Other Scripting Languages
- There're many general-purpose scripting languages that offer easy to read syntax and have an extensive set of standard libraries.
- Examples include Perl, Python, and Ruby.
- Python is a widely used scripting language for complex system administration tasks.
- System administrators are expected to be familiar with a language beyond Bash, such as Python to handle advanced automation and integration tasks.


---
layout: two-cols
---

## Wrapping Up
We have discussed the following:
- **System Administration Fundamentals**
  - Essential duties and responsibilities
  - Related disciplines (DevOps, SRE, Security)
  - Unix/Linux Background
  - Different ways to run Linux (bare metal, VM, cloud)

- **Core Concepts**
  - Remote access with SSH
  - File system organization and permissions
  - Basic Linux commands
  
::right::

<br>
<br>

  - Input/Output Redirection (`>`, `>>`, `2>`)
  - Pipes (`|`) to connect commands

- **Automation & Scripting**
  - Bash scripting fundamentals
  - Environment variables
  - Connecting commands using pipes
  - Alternative scripting languages

- Coming up next: Cloud Computing
