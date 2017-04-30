Restart pc, press shift at boot menu (OR ESC if laptop).

This should bring up GNU GRUB (ie recovery mode) menu.

    If this doesn't work, just restart mid boot and choose recovery mode when prompted on next launch.

Select the line which starts with Advanced options

Select the topmost version of the OS ending with ("recovery mode")

Press enter

In the following menu, go down to "Drop to root shell prompt"

Type the following:

mount -o remount,rw /

mount --all

chown root:root /usr/bin/sudo

chmod 4755 /usr/bin/sudo

restart

This should restore sudo privellages.
