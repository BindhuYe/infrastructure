🔄 Boot Process
Power On – The computer is powered on.

BIOS – The Basic Input/Output System initializes and performs hardware checks.

Master Boot Record (MBR) – Located on the hard disk, it contains the bootloader.

Boot Loader – Loads the Kernel into memory.

Kernel Initialization – The kernel initializes hardware and memory (Initial RAM).

👨‍💻 Kernel and User Space
Kernel Space (Privileged Mode):

Manages system resources and hardware via:

File System Management

System Calls

Device Drivers

Memory Management

Process Management

User Space (Non-Privileged Mode):

Contains user interfaces like:

Shell (/bin/init)

Graphical User Interface (GUI)

⚙️ System Calls and Hardware Access
Applications in user space make System API Calls, which are passed to the Kernel.

The Kernel interacts with:

CPU

Memory

Hard Disk

Network

🛠️ System Call Table
Maintains a list of system calls available for user programs to request services from the kernel.

🔐 Privilege Levels
User Mode (Non-Privileged) – Regular applications.

Kernel Mode (Privileged) – Full access to system hardware.