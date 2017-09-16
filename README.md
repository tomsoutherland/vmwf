# vmwf
This is a perl program written to manage VMware Fusion
virtual hosts on a Mac system. Although not tested, it
could be modified to work with other VMware virtualization
platforms. You will also need to install 'socat' as this
handles the I/O to the console device (pipe). When a VM is booted,
/vmwf/ will injet a serial port into the VMs configuration file
and create a named pipe for console communications. The VM will
need to be configured to use a serial port console for this to work.

    usage:

    vmwf -l [ -v ]
    vmwf -n VM -b [ -v ] [ -g ]
    vmwf -n VM -p [ -v ]
    vmwf -a X -c X -s XX -N VMx,VMy,VMz,... [ -v ]
    vmwf -h

    -l : list VMware machines
    -n : name of the VMware machine
    -b : power on and boot machine
    -v : verbose
    -g : enable GUI
    -p : power off machine
    -a : add X drives
    -c : controller number should be 0, 1, 2, or 3
    -s : size of drive(s), xxKB, xxMB, xxGB
    -N : comma seperated list of VMs to which the disks should be attached
    -h : duh!

    Note: The key sequence, "Control ]" (^]) disconnects from the console leaving the VM running.

