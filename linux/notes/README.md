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
