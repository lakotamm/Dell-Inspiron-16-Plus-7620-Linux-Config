#Dell Inspiron-16 Plus 7620 Linux Config
Here are configuration files for my Dell Inspiron 16 Plus 7620 running Linux

My use case: 
I dual boot Linux and Windows. I use Linux for majority of my tasks and free time and Windows for occasional gaming. Therefore when I am using Linux, I mostly need a long lasting and quiet device which does not get very warm. The configuration files reflect this use case. In the future I might create additional branches for different use cases.

About the device:
OS: Fedora Linux 36 (Workstation Edition)
Host: Inspiron 16 Plus 7620 
Kernel: 5.18.16-200.fc36.x86_64 
DE: GNOME 42.3.1 
CPU: 12th Gen Intel i7-12700H (20) @ 4 
GPU: NVIDIA GeForce RTX 3060 Mobile /  
GPU: Intel Alder Lake-P 
Memory: 15677MiB 

Programs for controling performance and consumption:
TLP - https://linrunner.de/tlp/index.html
Throttled - https://github.com/erpalma/throttled

BIOS configuration:
SATA Mode: AHCI (very important for power consumption!)
Fans/performance mode: Quiet
Battery max charge: 75%, starts charging at 70%
