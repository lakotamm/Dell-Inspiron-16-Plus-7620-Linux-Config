Here are configuration files for my Dell Inspiron 16 Plus 7620 running Linux Fedora.

My use case: 

I dual boot Linux and Windows. I use Linux for majority of my tasks and free time and Windows for occasional gaming. Therefore when I am using Linux, I mostly need a long lasting and quiet device which does not get very warm. The configuration files reflect this use case. In the future I might create additional branches for different use cases.

About the device:
- OS: Fedora Linux 36 (Workstation Edition)
- Host: Inspiron 16 Plus 7620 
- Kernel: 5.18.16-200.fc36.x86_64 
- DE: GNOME 42.3.1 
- CPU: 12th Gen Intel i7-12700H (20) @ 4.600GHz
- GPU: NVIDIA GeForce RTX 3060 Mobile / Max-Q 
- GPU: Intel Alder Lake-P 
- Memory: 15677MiB 

Programs for controling performance and consumption:
- TLP - https://linrunner.de/tlp/index.html (requires masking of power-profiles-daemon.servicepower-profiles-daemon.service)
- Throttled - https://github.com/erpalma/throttled (as of 10.8.2022 the latest GIT version is necessary to control AlderLake CPUs)

Further Linux configuration:
- Using default Nouveau Nvidia GPU (as of 10.8.2022 while writing this it has better power management than the Nvidia driver)
- Bluetooth disabled on startup by replacing AutoEnable=true with AutoEnable=false in /etc/bluetooth/main.conf

BIOS configuration:
- SATA Mode: AHCI (very important for power consumption!)
- Fans/performance mode: Quiet
- Battery max charge: 75%, starts charging at 70%

Speaker fix:
EDIT: UPDATE 22.1.2023 - the speaker fix has been implemented in kernel 6.2RC2 and it has been backported to 5.10, 6.0 and 6.1

- By default only the bottom speakers work. This is due to unsuitable default pin output and amplifier configuration.  With a great help from Philipp Jungkamp we created a kernel patch to fix this issue. The patch has been tested to build with kernels 5.19.2, 6.0 and higher.
The patch is expected to land in kernel 6.2.
https://github.com/tiwai/sound/commit/2912cdda734d9136615ed05636d9fcbca2a7a3c5
- Even with the patch the top speakers start playing sound with a ~0,5 second delay after the bottom speakers.

Other links:
https://github.com/tlvince/dell-inspiron-16-2-in-1-7620
