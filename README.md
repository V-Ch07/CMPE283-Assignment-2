# CMPE283-Assignment-2

        Step 1: Choose a Virtual Machine with Ubuntu 18.04 version and then Boot the virtual machine by using the commands - sudo reboot - uname -a.\
        Step 2: The second step is to build a kernel by cloning by using https://cdn.kernel.org/pub/linux/kernel/v5.x/linux-5.14.3.tar.xz source.
        Step 3: Run lsmod | grep kvm in order to verify if the kvm modules are loaded previously or not.
        Step 4: If they are present in the kernel, we need to remove them using rmmod kvm and rmmod kvm_intel commands.
        Step 4: Upon cloning the kernel, we need to build the kernal modules by running - sudo make modules && sudo make modules_install.
                Now we need to build the modules using the following commands: 
                  sudo rmmod kvm_intel
                  sudo rmmod kvm
                  sudo modprobe kvm
                  sudo modprobe kvm_intel
                 Now the kernel is successfully built. 
        Step 5:  We can check the kernel version using "uname -a".
        Step 6: We need to update the cpuid.c as well as vmx.c file in their respective folders.
        Step 7: In order to enable the kvm module in the hosst and to install the packages that are necessary , we need to run the commands in the terminal:
                sudo apt install qemu qemu-kvm qemu-system qemu-utils
                sudo apt install libvirt-clients libvirt-daemon-system virtinst

        Step 8: Now, install and run the Virtual Machine Manager. Then we need to install a guest OS and then login into nested Virtual Machine.
