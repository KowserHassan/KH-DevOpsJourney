# Linux notes

## What is Linux?

Linux is an open-source operating system originally developed by Linus Torvalds in 1991. 
It is the backbone of many servers, networks and cloud infrastructures around the world.

Key features of linux:
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

## Virtualisation

This allows you to run linux on your existing computer without needing to replace your current OS.

Windows users use VirtualBox to do this, whilst Mac users use UTM. UTM allows you to emulate any classic or current OS, even Windows XP!

## UTM

When running a VM on UTM, you have two options: virtualisation or emulation.

- Virtualization is faster because  it directly uses your laptop's hardware and CPU architecture and can therefore only run VMs in the native CPU architecture. This means the guest OS running in the VM must be the same architecture as the host system's CPU (e.g., x86 on an x86 CPU). Virtualisation allows the VM to run nearly at native speed since it doesn't need to translate instructions between different architectures.

- Emulation allows you to run a guest OS with a different CPU architecture than the host (e.g., running an ARM-based OS on an x86 CPU). Emulation involves simulating the hardware and translating instructions, which requires more processing power and separate hardware and software, making it significantly slower than virtualisation.

There are 3 ways to boot the Linux OS:

1. Use Apple Virtualisation
2. Boot from Kernel image
3. Boot from ISO image

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

1. Ls - lists everything in the directory 
2. pwd - print working directory (shows you where you are)
3. cd - change directory
4. mkdir - makes new directory
5. rmdir - removes directory 
6. touch - creates new file 
7. rm - removes file
8. echo - writes text in file i.e echo "Hello World" > file.txt
9. cat - displays all contents within a file
10. grep - searches for words/patterns in file - essentially cmd/ctrl F
11. vim

## Shortcuts 
- tab - completes the words for you
- ctrl l - clears screen
- man ‘enter command’

## Miscellaneous Command Line Knowledge
- . : hidden files begin with a '.' and are ignored the ls command and can only be viewed using ls -a command

## Shells

installing zsh

set zsh as default shell 

chsh -s /bin/zsh






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
