!SLIDE redcode bullets list

# Xen-PVM Kernel

* `kernel_path` : valid file on node(s)
* `initrd_path` : valid initrd file
* `kernel_args` : e.g.`ro quiet`
* `root_path` : e.g. `/dev/vda2`
* `bootloader_path` and `bootloader_args` to empty

!SLIDE redcode bullets list

# Xen + pvgrub

* `kernel_path` points to `pvgrub`
* `kernel_args` path of grub config file
* `root_path` **must** be empty
* `bootloader_path` and `bootloader_args` to empty

!SLIDE redcode bullets list

# KVM Kernel

* `kernel_path` : valid file on node(s)
* `initrd_path` : optionally set if using initrd
* `kernel_args` : e.g. `ro quiet`
* `kernel_path` to empty to use from instance disk
