# Install ubuntu and avoid nasty errors
To temporarily add a boot parameter to a kernel:

    Start your system and wait for the GRUB menu to show (if you don't see a GRUB menu, press and hold the left Shift key right after starting the system).
    Now highlight the kernel you want to use, and press the e key. You should be able to see and edit the commands associated with the highlighted kernel.
    Go down to the line starting with linux and add your parameter foo=bar to its end.
    Now press Ctrl + x to boot.

Add a boot parameter to a kernel (temporary while installing, need to add it permanent further):

    Start your system and wait for the GRUB menu to show (if you don't see a GRUB menu, press and hold the left Shift key right after starting the system).
    Now highlight the kernel you want to use, and press the e key. You should be able to see and edit the commands associated with the highlighted kernel.
    Go down to the line starting with linux and add your parameter foo=bar to its end.
    Now press Ctrl + x to boot.


To make this change permanent:

    From a terminal (or after pressing Alt + F2) run:

    gksudo gedit /etc/default/grub

    and enter your password.

    Find the line starting with GRUB_CMDLINE_LINUX_DEFAULT and append pci=noaer

    GRUB_CMDLINE_LINUX_DEFAULT="quiet splash pci=noaer"

    Save the file and close the editor.

    Finally, start a terminal and run:

    sudo update-grub

    to update GRUB's configuration file (you probably need to enter your password).

On the next reboot, the kernel should be started with the boot parameter. To permanently remove it, simply remove the parameter from GRUB_CMDLINE_LINUX_DEFAULT and run sudo update-grub again.

To verify your changes, you can see exactly what parameters your kernel booted with by executing cat /proc/cmdline.
