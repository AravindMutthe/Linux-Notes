# 1.Linux-Kernel:

**Should be familiar with,**

1. Linux Command Line,
2. C Programming,
3. Editing files in linux.

**My Setup,(tutor)**

1. connecting a LM( linux Machine)
2. That LM also running a VM.

**Your Setup,**

1. Should have LM or VM with root access.
2. use any distro is fine.

# 3. What is Linux Kernel ?

1. Linux Kernel is a program (a program name with vmlinuz-[ version ])
2. That program needed to be loaded into memory and run.
3. This operation done by boot loader
4. With linux boot loader called as GRUB.
5. GRUB reads Kernal program(files) from disk(HDD) into the memory (RAM) and transfers control to it(RAM).
6. The kernel program, like other programs, has command-line parameters.

   1. GRUB is responsible for passing those parameters to the kernel.
   2. The kernel image itself, that V-M-L-I-N-U-Z file, is relatively small, just a few meg

**The Linux kernel has an API:** it provides the programming interface.
including
1. **system calls:** The functions that we can call from user space into the kernel.
2. **virtual file systems.**(Linux Kernel also provides)

   1. **Proc,**
   2. **sys,**
   3. **debugfs(not popular).**

through those virtual file systems, we can interact directly with the kernel,
getting information from the kernel and changing things in the kernel.

3. **Device Files (system calls):** We interact with device drivers by doing operations on those device files.
Those are standard system calls
   1. read,
   2. write,
   3. open.

**The kernel is a gatekeeper:**

1. The kernel enforces privileges.
2. In Linux, we call those privileges capabilities
3. In the Linux kernel source code, it refers to the capabilities of a process to
see if it is allowed to perform some sort of privileged operation.
4. We think of root processes having all the privileges. But More precisely, root
processes typically have a large set of capabilities
5. Also CPUs have special instructions that are only allowed to be executed
when the CPU itself is in a special supervisory mode.
6. It's in that mode when we're executing inside the kernel. So that means there
are assembly language instructions that can only be executed by the kernel.
7. The Linux kernel also implements a number of security policies. The
underlying mechanisms used by SELinux,
8. The kernel has to provide controlled access to make sure that things are done
in an orderly and safe manner.

**The kernel is modular:**

   1. Kernel image is small.
   2. The kernel image though is sufficient to boot to user space to begin in running some processes(dbms, ms ofc)
   3. Once we have processes, we can load additional functionality into the kernel
through the loadable kernel module mechanism.
   4. The loadable module mechanism means we can just load the drivers that we need.
   5. We don't need to load drivers for hardware that's not present.
   6. We can also just load additional sorts of functionality that's not drivers but
say for security or other things.

# 1. Where is Linux Kernel. ?

* Inside boot directory i.e **aravind@X1-Yoga:/boot$ ls**
we see a bunch of stuff, including some vmlinuz files(kernal files)

1. To know Which kernel(program/ file)we're booted in now, use 
    > uname -r
So there is a vmlinuz-5.3.0-29-generic. That's the kernel we're booted
into right now
2. To find size of that program(kernael/file)
    > ls -l vmlinuz-5.3.0-29-generic.

3. the vmlinuz file, is going to be loaded into memory(RAM) by GRUB and
GRUB will transfer control to it(RAM).

4. Don't delete that file. It's not being used right now because it's been loaded
into memory but if you deleted it, when you tried to reboot there'd be
trouble. 