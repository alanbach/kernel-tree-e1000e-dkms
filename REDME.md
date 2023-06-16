# Intel e1000e ethernet adapter driver (DKMS version)

__Intel Network Adapter Driver for PCIe* Intel Gigabit Ethernet Network Connections Under Linux*__

This is a DKMS package version of the Intel's e1000e ethernet driver merged into kernel tree under drivers/net/ethernet/intel/e1000e.

---

## Requirements
DKMS and Linux headers packages are required to produce a successful build. 

On a Debian/Ubuntu based system, they can be installed using:

```
sudo apt-get install linux-headers-$(uname -r) dkms build-essential
```

---

## Installing and building the DKMS kernel module

Here is the process to install and build the kernel module after the above dependencies are met:
```
sudo cp -r e1000e-dkms /usr/src/
sudo dkms add -m e1000e -v dkms
sudo dkms build -m e1000e -v dkms
sudo dkms install -m e1000e -v dkms
```

To uninstall and remove the kernel module:
```
sudo dkms remove -m e1000e -v dkms --all
```
