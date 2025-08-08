# csm-utils

csm-utils is collection of scripts and services required for qdu100 host machine to configure host, store ddr_training_data of qdu100 and start nbd related services on device.

All these scripts run on the host. Here are their descriptions:

csm-check-repair.sh: Checks the integrity of qdu100 images on the host

csm-configure-ip.sh: Configures the IP address of the host and sets /sys/bus/mhi/devices/mhi[0-9]_CSM_CTRL/transport_mode
node depending on qdu100 debug.conf value(usb/pcie)

csm-nbdkit.sh      : Starts nbd on the desired port and exports the qdu100 device-specific
directory as a linuxdisk

csm-nbdkit-stop.sh : Stops nbd and the exposed linuxdisk

csm-store-ddr.sh   : Reads /sys/bus/mhi/devices/mhi[0-9]/ddr-training-data to save
the qdu100 device's DDR data (this one required for sahara and qdu100 driver)

decimal-to-hex.sh  : Converts the qdu100 serial number to hexadecimal


# License

Licensed under BSD 3-Clause-Clear
