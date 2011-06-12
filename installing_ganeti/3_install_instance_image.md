!SLIDE subsec

# Install OS Definition

!SLIDE smbullets list

# Instance creation scripts

* Requires Operating System installation script
* Provide scripts to deploy various operating systems
* _Ganeti Instance Deboostrap_ - upstream supported
* _Ganeti Instance Image_ - written by me

!SLIDE smbullets list

# OS Variants

* _Variants_ of the OS Definition
* Often used for _defining_ operating system
* Different deployment settings
  * Filesystem
  * Image type
  * Image directory
* Example Names:
  * debian-lenny
  * centos-5

!SLIDE commandline bigcode

# Install Instance Image Dependencies

    $ apt-get install dump qemu-kvm kpartx

!SLIDE commandline incremental bigcode

# Install Instance Image

    $ ./configure --prefix=/usr \
        --localstatedir=/var \
        --sysconfdir=/etc \
        --with-os-dir=/srv/ganeti/os
    $ make
    $ make install

!SLIDE codeblock incremental rvc bigcode

# Configure Instance Image

### ``/etc/default/ganeti-instance-image``

    IMAGE_TYPE="dump"
    ARCH="x86_64"

### ``/etc/ganeti/instance-image/variants/debian.conf``

    IMAGE_NAME="debian-6.0.1"

