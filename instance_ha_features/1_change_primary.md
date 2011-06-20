!SLIDE commandline bigcode rvc

# Changing the Primary node

### Failing over an instance

    $ gnt-instance failover INSTANCE_NAME

### Live migrating an instance

    $ gnt-instance migrate INSTANCE_NAME

!SLIDE commandline bigcode rvc bullets smtitle

# Moving an instance (offline)

    $ gnt-instance move -n NEW_NODE INSTANCE

* Instance must be _stopped_
* Currently primary must be _healthy & on-line_
* Instance disk has no errors
