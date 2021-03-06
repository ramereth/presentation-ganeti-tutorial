!SLIDE subsec

# Install OS Definition 

!SLIDE smbullets list rvc

# Instance creation scripts

### also known as OS Definitions

* Requires Operating System installation script
* Provide scripts to deploy various operating systems
* _Ganeti Instance Deboostrap_ - upstream supported
* _Ganeti Instance Image_ - written by me

!SLIDE bullets list

# OS Variants

* _Variants_ of the OS Definition
* Used for _defining_ guest operating system
* Types of deployment settings:
  * Filesystem
  * Image directory
  * Image Name

!SLIDE commandline bigcode smtitle

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

!SLIDE bullets redcode

# Creating images

* Manually install/setup guest
* Shutdown guest
* Create filesystem _dump_ or _tarball_
* Place in `IMAGE_DIR`
