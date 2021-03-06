# VFIO Setup

Files in this repository are my scripts, notes and "all the helper stuff"
related with configuring the GPU passthrough and the guest VM. Essentially,
native-level performance for games in Windows, without dual booting. This
was done on Arch Linux, on other distros your mileage may vary (especially
with outdated libvirt/QEMU).

If you'd like to try such a setup yourself, [try this ArchWiki page](https://wiki.archlinux.org/index.php/PCI_passthrough_via_OVMF).

My setup is described a bit better on [the VFIO examples page](https://wiki.archlinux.org/index.php?title=PCI_passthrough_via_OVMF/Examples).

The VM is started with either `WinVM.sh` or `JustVM.sh`, the first one starts
Windows8.1 and does some magic with displays, the second uses Windows8.1-NoRedir
and doesn't switch displays/start Synergy/etc.

It's exactly the same domain, except that it doesn't pass through any USB devices.
Used mostly for remote access when I've unplugged the mouse (libvirt will fail
to start the VM if one of the passed devices are unavailable).
