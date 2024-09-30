# Linux notes

  - [What is Linux?](#what-is-linux)
  - [Why Linux?](#why-linux)
  - [Linux Distributions](#linux-distributions)
  - [The Anatomy: Commands, Options and Arguments](#the-anatomy-commands-options-and-arguments)
  - [Linux Commands](#linux-commands)
  - [Miscellaneous Command Line Knowledge](#miscellaneous-command-line-knowledge)
  - [Shells: The intermediary between the User and the OS](#shells-the-intermediary-between-the-user-and-the-os)
  - [Programs and Binaries](#programs-and-binaries)
  - [What happens when you type the 'ls' command?](#what-happens-when-you-type-the-ls-command)
  - [Common shells:](#common-shells)
  - [Installing zsh](#installing-zsh)
  - [The Linux File System](#the-linux-file-system)
  - [File Permissions](#file-permissions)
  - [Data Redirection](#data-redirection)
  - [Environment Variables](#environment-variables)
  - [How to rent a Virtual Machine from AWS? ☁️](#how-to-rent-a-virtual-machine-from-aws-️)


## What is Linux?

Linux is an open-source operating system originally developed by Linus Torvalds in 1991. 
It is the backbone of many servers, networks and cloud infrastructures around the world.

Key features of Linux:
1. Stability
2. Security 
3. Customisatibiltiy
4. Compatibility 
5. Community support

## Why Linux?

Linux is widely used in servers, cloud services and networking. These are 5 key features that make Linux a top choice for businesses and developers:

**1. Stability and Reliability:**
Linux systems are known for their stability and reliability. They can run for years without needing a reboot, which is a critical requirement for servers and continuous operation systems. This stability makes Linux a favourite for servers and systems where uptime is crucial.

**2. Security:**
Linux is considered highly secure compared to many other OS. Its permission and user role features, along with a strong community and frequent updates, help keep systems secure from malware and other vulnerabilities. Linux's architecture and user privileges (especially the separation of standard and administrative duties) also contribute to its robust security.

**3. Customisability:**
Linux is highly customisable. Users can modify everything from the kernel (the core of the operating system) up to the desktop environment, allowing for a tailored experience that meets specific needs or preferences. This level of customisation is not as easily achieved with other more closed OS such as Windows and macOS.

**4. Cost-Effectiveness:**
Most Linux distributions are free to download and use, which can result in significant cost savings, especially for businesses and developers who need to deploy multiple machines. In contrast, Windows and macOS often come with licensing fees.

**5. Community Support:**
The Linux community is one of its greatest assets. A large, active community means users often get rapid support and help through forums, blogs, and community-driven projects. This is particularly beneficial for solving problems, learning, and integrating systems.

## Linux Distributions

These are different verions of Linux. Each one is has unique strengths and is therefore suited to different tasks.

Popular examples:
- Ubuntu - beginner friendly :)
- Debian
- Centos
- Fedora

**Virtualisation:**

This allows you to run linux on your existing computer without needing to replace your current OS.

Windows users use VirtualBox to do this, whilst Mac users use UTM. UTM allows you to emulate any classic or current OS, even Windows XP!

## The Anatomy: Commands, Options and Arguments

Linux commands are textual instructions that tells the OS what to do.

They:
- can be entered directly in the terminal
- are CASE SENSITIVE
- have various options and arguments that can modifytheir behaviour
- have instructions VIA a manual

Commands have anatomy, they are comprised of 3 parts:

1. the command itself
2. the options that can be used with the command 
3. the argument 

e.g ls -a.
- ls = list contents
- -a = list ALL the contents in the current directory - including hidden files and directories
- . = represents that the arguemnt is the current working directory

## Linux Commands

<table>
  <tr>
    <td>

| Command        | Description                                 |   
|----------------|---------------------------------------------|
| `ls`           | Lists directory contents                    |
| `pwd`          | Prints the current working directory        |
| `cd`           | Changes the current directory               |
| `mkdir`        | Creates a new directory                     |
| `rmdir`        | Removes a directory                         |
| `cp`           | Copies files or directories                 |
| `touch`        | Creates a new empty file                    |
| `mv`           | Moves or renames files or directories       |
| `rm`           | Removes files or directories                |
| `grep`         | Searches text for words/patterns            |
| `echo`         | Writes text in file                         |
| `cat`          | Concatenates and displays file contents     |
| `vim`          | Opens the Vim text editor to edit files     |
| `chmod`        | Changes file permissions                    |
| `chown`        | Changes file owner and group                |
| `find`         | Searches for files in a directory hierarchy |
| `tar`          | Archives files                              |
| `df`           | Reports file system disk space usage        |
| `du`           | Estimates file space usage                  |

  </td>
    <td>

| Shortcut            | Description                                                      |
|---------------------|------------------------------------------------------------------|
| `Tab`               | Autocompletes file and directory names                           |
| `Ctrl + L`          | Clears the terminal screen                                       |
| `Ctrl + C`          | Stops the current command or process                             |
| `sudo !!`           | Re-runs last command with superuser privileges                   |
| `!!`                | Re-runs the last command entered                                 |
| `man <command>`     | Displays manual page for the specified command                   |
| `Ctrl + R`          | Searches through command history                                 |
| `!number`           | Executes previous command from command history                   |
| `Ctrl + Alt + T`    | Opens a new terminal window                                      |
| `Ctrl + D`          | Logs out of current shell/closes the terminal                    |
| `Ctrl + Z`          | Suspends current process and puts in background                  |
| `Ctrl + A`          | Moves the cursor to the beginning of a line                      |
| `Ctrl + E`          | Moves the cursor to the end of a line                            |
| `Ctrl + U`          | Deletes the entire line before the cursor                        |
| `Ctrl + K`          | Deletes the entire line after the cursor                         |
| `Ctrl + W`          | Deletes the word before the cursor                               |


 </td>
  </tr>
</table>

## Miscellaneous Command Line Knowledge

- . : hidden files begin with a '.' and are ignored by the ls command and can only be viewed using ls -a command

## Shells: The intermediary between the User and the OS

The shell:
1. interprets the command
2. translates it into instructions that the OS can understand known as system calls or function calls (involves understanding the command syntax and any arguments provided)
3. then passes these instructions to the OS (the OS processes the instructions and provides an output)

Binary Translation: The shell does not directly convert commands into binary, it translates them into system calls or instructions that the OS understands. The OS and its underlying hardware ultimately process these instructions, involving binary at the lower level.

## Programs and Binaries
Commands can be considered to be small programs. These programs are written in a programming language and then compiled into a format that the computer can execute called a binary.

The program is written by a developer which performs a specific task e.g 'ls'
A binary is simply a compiled version of programs that the computer can run directly.

## What happens when you type the 'ls' command?

- the shell interprets it and understands that we want to run the ls programme
- it then searches for the ls programme in certain directories on the computer which are listed in the path enviornment variable
- when the shell finds the ls programme, excecutes it

The path environment variable tells the shell which directories we need to look in to excute the command we want to run

i.e. /usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin:/opt/homebrew/bin

## Common shells:
- bash
- zsh
- ksh
- fish
- csh/Tcsh
These shells have unique capabilities but they all serve the same fundamental purpose - helping the user interact with the OS
  
**Check the shell you are using by running the command: echo $SHELL**

## Installing zsh
**Installation command**

- sudo apt-get install zsh

**Set zsh as default shell permanently**

- chsh -s /bin/zsh
- there will be a password prompt
- if there's an authentification failure, run the command - **sudo** chsh -s /bin/zsh
- reboot instance to update the new defualt shell

.. if that did not work run the command: sudo chsh -s $ (which zsh) $ (whoami)

- sudo: Runs the command with superuser (root) privileges.
- chsh: The chsh (change shell) command changes the user's default shell.
- -s: Specifies the new shell.
- $(which zsh): Finds the path of the Zsh shell (e.g., /bin/zsh).
- $(whoami): specifies current user

## The Linux File System

In Linux, everything is treated as a file, including devices and processes. This structure provides a flexible way to manage the file system
It is organsied in a hierarachal structure, starting at the root directory which is denoted by a single /

| Directory | Description                                                                                                                                              |
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| /         | The root directory of the entire filesystem hierarchy, everything is nested under this directory.                                                        |
| /bin      | Essential ready-to-run programs (binaries), includes the most basic commands such as `ls` and `cp`.                                                      |
| /boot     | Contains kernel boot loader files.                                                                                                                       |
| /dev      | Device files.                                                                                                                                            |
| /etc      | Core system configuration directory, should hold only configuration files and not any binaries.                                                          |
| /home     | Personal directories for users, holds your documents, files, settings, etc.                                                                              |
| /lib      | Holds library files that binaries can use.                                                                                                               |
| /media    | Used as an attachment point for removable media like USB drives.                                                                                         |
| /mnt      | Temporarily mounted filesystems.                                                                                                                         |
| /opt      | Optional application software packages.                                                                                                                  |
| /proc     | Information about currently running processes.                                                                                                           |
| /root     | The root user's home directory.                                                                                                                          |
| /run      | Information about the running system since the last boot.                                                                                                |
| /sbin     | Contains essential system binaries, usually can only be run by root.                                                                                     |
| /srv      | Site-specific data which are served by the system.                                                                                                       |
| /tmp      | Storage for temporary files.                                                                                                                             |
| /usr      | This is a misleading name as it suggests that it is for "user" files, similar to a home directory but most often it does not contain user files in the sense of a home folder. This instead stores user-installed software and utilities, however, that is not to say you can't add personal directories in there. Inside this directory are sub-directories for `/usr/bin`, `/usr/local`, etc. |
| /var      | Variable directory, it's used for system logging, user tracking, caches, etc. Basically, anything that is subject to change all the time.                 |


## File Permissions

File permissions control who can read, write and execute a file. This is important in order to maintain security and order in your system. Command: ls -l 

There are 3 ways to represent file permissions:
1. Symbolic (Text)
2. Numeric (Octal)
3. Binary

### 1. Symbolic

The format is rwxrwxrwx, where each set of three letters represents the permissions for the owner, group, and others, respectively.

- r - read: allows you to view file content
- w - write: allows you to modify file content
- x - execute: allows you to run the file as as programme
- "-" - No permission

<img width="404" alt="Screenshot 2024-09-02 at 14 29 14" src="https://github.com/user-attachments/assets/307da4a9-7dde-4a43-85f8-afde3e6e2534">

For example:

rwxr-xr-- means:
- Owner: read, write, and execute (rwx)
- Group: read and execute (r-x)
- Others: read only (r--)

### 2. Numeric 

Each permission set (owner, group, others) is calculated by adding up the values:

For example:

- Owner: rwx = 4 (read) + 2 (write) + 1 (execute) = 7
- Group: r-x = 4 (read) + 0 (no write) + 1 (execute) = 5
- Other: r-- = 4 (read) + 0 (no write) + 0 (no execute) = 4

The symbolic representation rwxr-xr-- can be represented numerically as 754.

Convert rw-----w- to Octal Representation:  602

### 3. Binary

Permissions are simply represented as:

1: Permission is granted.
0: Permission is denied.

For example:

111101100 (rwxr-xr--) means:
- Owner: 111 (rwx: full permissions)
- Group: 101 (r-x: read and execute)
- Other: 100 (r--: read only)
  
<img width="997" alt="Screenshot 2024-09-02 at 15 13 09" src="https://github.com/user-attachments/assets/37bce9fe-3088-4e0f-b276-3c66c5135304">

## chmod command

- used to change permissions of a file or directory

There are 2 ways to use chmod:
1. Symbolic - chmod u+x, g+r, o-w 
2. Numeric - chmod 777 example.txt

- you can also specify a set by using the '=' operator

e.g if you wanted to give users and group read and write permissions, and others read permissions

run command: chmod ug=rw, o=r example.txt

## chown command

- used to change the ownership of a file or directory. You can change both the user and the group that owns the file.
- requires sudo

e.g sudo chown newuser example.txt

## chgrp command

- used to change the group ownership of a file or directory.

e.g sudo chgrp admin2 example.txt

>- Shortcut! You can change BOTH the owner and the group using the **chown** command
>- `sudo chown ubuntu:admin2 example.txt` - this changes the user to ubuntu and the group to admin2

## Dir ownership

You can recursively change the ownership of a directory and its contents

sudo chown -R newuser:admin2 my_directory 

## Data Redirection

Standard stream is essential for effectively handling input and output

There are 3 standard streams:
1. Standard input (keyboard)
2. Standard output (terminal screen, or redirected to a file)
3. Standard error (terminal screen, or redirected to a file)

<img width="997" alt="Screenshot 2024-09-04 at 00 20 19" src="https://github.com/user-attachments/assets/beba105b-c3c6-4259-a2f8-7227eaf02cd8">

To redirect errors to a file, run command `ls non_existent_file **2>** error_log.txt` so when you read contents of the file by running `cat error_log.txt`, it outputs the error

>- The &> operator is used to redirect both stdout and stderr to a single location

## What is /dev/null?

/dev/null is a special device file that acts like a black hole — anything written to it is discarded, and nothing is saved.

It's used to get rid of unwanted output or errors by redirecting them to this file.

e.g `ls > /dev/null` , discards the stdout of the ls command, meaning the file listing won't be shown anywhere.

or `ls nonexistentfile 2> /dev/null`, discards the error message generated by trying to list a non-existent file.

## Environment Variables

Variables that are set in the environment and control the behaviour of processes on your system. 

<img width="655" alt="Screenshot 2024-09-30 at 12 39 36" src="https://github.com/user-attachments/assets/d1d8e83f-7e53-4b49-afd7-fa8a9338bc3c">

Each environment variable is a key-value pair—the key is the name of the variable, and the value is the data or information it holds

- **Key:** The name of the environment variable.

  - It acts as an identifier, allowing you to reference the variable later.
Example: In the environment variable HOME, HOME is the key.

- **Value:** The actual data or information associated with that key.

    - It provides the content that the variable holds.
Example: For the HOME variable, the value might be /home/yourusername, which indicates the path to your home directory.

>- When you set an environment variable, you create a relationship between a key and a value which allows programs and the OS to access specific information using the variable's key.

## Common Uses:

1. **Configuration:** Environment variables store settings and paths that programs and scripts rely on.
2. **Shell customisation:** You can customise how the shell behaves or what paths it uses to find executables.
3. **Accessing system information:** Environment variables can store system details like the current user, home directory, or shell type.

## How to View Environment Variables

- env or printenv: Lists all environment variables
- echo: You can display the value of a specific variable using echo

## Setting Environment Variables

1. **Temporarily in a Shell:** You can define or update an environment variable within your current shell session, but it will only last until the session is closed.

`export MY_VAR="Hello World"`
`echo $MY_VAR`  # Output: Hello World

2. **Permanently:** To set environment variables permanently, you can add them to your shell’s configuration file e.g. .zshrc and apply changes using `source .zshrc`

<img width="655" alt="Screenshot 2024-09-30 at 12 45 15" src="https://github.com/user-attachments/assets/d5fe3a5c-757b-46eb-b9eb-961ad57c62e6">

## How to rent a Virtual Machine from AWS? ☁️

EC2 is an AWS service that allows you to rent out virtual servers in the cloud.

**Launching a new EC2 instance:**
1. On your AWS account, navigate to EC2 and launch a new EC2 instance
2. Name the instance appropriately
3. Select an AMI (Amazon Machine Image): Choose an operating system (e.g. **Amazon Linux (free tier)**, Ubuntu, Windows Server).
4. Choose an Instance Type: Select a VM size -> **t2.micro for the free tier**
5. Create a Key Pair: Download the .pem file (needed to connect securely to your instance later)
6. Set network and instance settings: Select edit and autoassign a public IP by selecting "enable"
7. Configure Security Group: Allow necessary ports (e.g., SSH for Linux, RDP for Windows).
8. Next to "Allow SSH traffic from" Personalise the IP address from "anywhere" your personal IP to enhance security.
9. Add Storage: Adjust disk size if needed (default usually suffices).
10. Review and Launch

**Connecting to Your Instance:**
1. When your instance is in running state, click "connect" and navigate to "select SSH client"
2. Open an SSH client (SSH client is typically built into the terminal for Linux/MacOS)
3. Locate you private key file (.pem) that you should have downloaded
4. Run the command - chmod 400 "YOURPEMFILE"
5. Connect to instance using public DNS by running the command - ssh -i /path/to/your-key-file.pem ubuntu@ec2-xx-xx-xx-xx.compute-1.amazonaws.com

**Manage Your Instance:**

Use the instance for your tasks but remember to stop or terminate it when done to avoid charges!
