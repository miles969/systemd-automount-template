# systemd-automount-template
These 2 templates can be used to automount network filesystems without editing fstab. It uses systemd's automount function to monitor access requests to local mountpoints and mount the corresponding network filesystem on the fly

Usage:

1) Save the files in /etc/systemd/system (I haven't managed to make these work as user units)
2) Edit the template files to reflect your network mount details and create the necessary mountpoints.
3) Rename the templates to reflect their local mountpoint.
4) enable the .automount file to install the automount service.
5) systemctl daemon-reload and systemctl start the automount service (or reboot)
6) cd or ls the local mountpoint to test
