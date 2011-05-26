!SLIDE transition=fade

# Ganeti Web Manager
### Installation

!SLIDE bullets transition=fade

# Dependencies
* Python >=2.5, 2.7 recommended
* Pip - Python package installer
* Fabric - Install scripts
* VirtualEnv - Python virtual environments

!SLIDE commandline incremental transition=fade

# Fabric Installer

    $ fab dev deploy
    $ fab prod deploy

!SLIDE bullets transition=fade

# Settings

* Database: sqlite by defauilt
* Outgoing Mail
* Cache Backend
    
!SLIDE commandline incremental transition=fade

# Activate Virtualenv

    $ source bin/activate 
    $ which python
    /home/peter/wrk/ganeti_webmgr/bin/python


!SLIDE commandline incremental transition=fade

# Create Database

    $ python manage.py syncdb
    $ python manage.py migrate
