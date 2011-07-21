!SLIDE commandline incremental bigcode rvc

# Install Ganeti

### Note: this is for >=ganeti-2.5

    $ ./configure --localstatedir=/var \
        --sysconfdir=/etc \
        --enable-htools
    $ make
    $ make install

!SLIDE commandline incremental redcode medcode

# Startup Scripts

### Installed into ``/usr/local/``

    $ cp doc/examples/ganeti.initd /etc/init.d/ganeti
    $ update-rc.d ganeti defaults 20 80


!SLIDE commandline bullets list medcode

# `ganeti-watcher`

    $ cp doc/examples/ganeti.cron /etc/cron.d/ganeti

* _Automatically_ restarts failed instances
* Restarts _failed_ secondary storage

!SLIDE smbullets list redcode

# What gets installed

* Python libraries under the *ganeti* namespace
* Set of programs under ``/usr/local/sbin`` or ``/usr/sbin``
* Set of tools under ``lib/ganeti/tools`` directory
* IAllocator scripts under ``lib/ganeti/tools directory``
* *Cron job* needed for cluster maintenance
* *Init script* for Ganeti daemons

