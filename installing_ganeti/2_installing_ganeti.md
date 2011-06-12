!SLIDE commandline incremental bigcode

# Install Ganeti

    $ ./configure --localstatedir=/var \
        --sysconfdir=/etc \
        --enable-htools
    $ make
    $ make install

!SLIDE commandline incremental redcode

# Post-install Steps

### Installs into ``/usr/local/``

    $ cp doc/examples/ganeti.initd /etc/init.d/ganeti
    $ update-rc.d ganeti defaults 20 80
    $ cp doc/examples/ganeti.cron /etc/cron.d/ganeti

!SLIDE smbullets list redcode

# What gets installed

* Python libraries under the *ganeti* namespace
* Set of programs under ``/usr/local/sbin`` or ``/usr/sbin``
* Set of tools under ``lib/ganeti/tools`` directory
* IAllocator scripts under ``lib/ganeti/tools directory``
* *Cron job* needed for cluster maintenance
* *Init script* for Ganeti daemons

