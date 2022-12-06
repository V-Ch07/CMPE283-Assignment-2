# CMPE283-Assignment-2

 Question 1:- 
         
      1.For each member in your team, provide 1 paragraph detailing what parts of the lab that member implemented / researched.
                  
                - I had done it alone.
                 
  Question 2: - The following are the steps involved in the completion of the project.

   Step 1: Choose a Virtual Machine with Ubuntu 18.04 version and then Boot the virtual machine by using the commands 
   - sudo reboot - uname -a.
   
   Step 2: The second step is to build a kernel by cloning by using https://cdn.kernel.org/pub/linux/kernel/v5.x/linux-5.14.3.tar.xz source.\
   Step 3: Run lsmod | grep kvm in order to verify if the kvm modules are loaded previously or not.\
   Step 4: If they are present in the kernel, we need to remove them using rmmod kvm and rmmod kvm_intel commands.\
   Step 4: Upon cloning the kernel, we need to build the kernal modules by running - sudo make modules && sudo make modules_install.\
           Now we need to build the modules using the following commands: \
                
                  sudo rmmod kvm_intel\
                  sudo rmmod kvm
                  sudo modprobe kvm\
                  sudo modprobe kvm_intel
                  Now the kernel is successfully built. \
                 
   Step 5:  We can check the kernel version using "uname -a".\
   Step 6: We need to update the cpuid.c as well as vmx.c file in their respective folders.\
   Step 7: In order to enable the kvm module in the hosst and to install the packages that are necessary , we need to run the commands in the terminal:\
                
                sudo apt install qemu qemu-kvm qemu-system qemu-utils
                sudo apt install libvirt-clients libvirt-daemon-system virtinst

   Step 8: Now, install and run the Virtual Machine Manager. Then we need to install a guest OS and then login into nested Virtual Machine.\
  
   Step 9: Now install the cpuid using sudo apt install cpuid.\
          Now, run the command cpuid -1 0x4FFFFFFF in order to verify the specific output.\
           
   Step 10: Now, run the test script to see the results and to print the number of exits. We can also find the no. of cycles in ebx and ecx registers when             eax=0xFFFFFFFe
   
   Outputs: 
   
   The total number of exits is displayed in the following figure:
   
   <img width="352" alt="image" src="https://user-images.githubusercontent.com/98682905/205846282-04513b9f-6f4f-400c-8bf2-2cf534f03bc2.png">

   The number of cycles spent is displayed in the following figure: 
   
   
   <img width="749" alt="image" src="https://user-images.githubusercontent.com/98682905/205846718-38361aab-c78f-484e-9aeb-9288b9abe927.png">

  
   
           
