# Run Fedora Linux on RISC-V under QEMU

Build

   ./build  # Downloads Fedora disk image and creates QEMU RISC-V docker image

Run

   ./run    # Boots into Fedora login if your host machine is sufficiently large:


    Welcome to the Fedora/RISC-V stage4 disk image
    https://fedoraproject.org/wiki/Architectures/RISC-V
    
    Build date: 2018-04-06 08:24
    
    Kernel 4.16.0-rc5-01493-g7f82cffaad50 on an riscv64 (ttyS0)
    
    The root password is ‘riscv’.
    
    To install new packages use ‘dnf install ...’
    
    If DNS isn’t working, try editing ‘/etc/yum.repos.d/local.repo’.
    
    For updates and latest information read:
    https://fedorapeople.org/groups/risc-v/disk-images/readme.txt
    
    stage4 login: root
    Password: 
    
    [root@stage4 ~]# uname -a
    Linux stage4.fedoraproject.org 4.16.0-rc5-01493-g7f82cffaad50 #6 SMP Fri Mar 16 00:38:51 UTC 2018 riscv64 riscv64 riscv64 GNU/Linux
    [root@stage4 ~]# 

