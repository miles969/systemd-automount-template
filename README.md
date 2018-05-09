# systemd-automount-template
These 2 templates can be used to automount network filesystems without editing fstab. It uses systemd's automount function to monitor access requests to local mountpoints and mount the corrosponding network filesystem on the fly

Usage:

1) Edit the template files to reflect your network mount details and create the necessary mountpoints.
2) Rename the templates to reflect their local mountpoint.
3) enable the .automount file to install the automount service.
4) systemctl daemon-reload and systemctl start the automount service (or reboot)
5) cd or ls the local mountpoint to test
