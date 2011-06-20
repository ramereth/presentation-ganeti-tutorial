!SLIDE commandline medcode incremental smtitle

# Conversion of an instance's disk type

    $ # start with a non-redundant instance
    gnt-instance add -t plain ... INSTANCE

    $ # later convert it to redundant
    gnt-instance stop INSTANCE
    gnt-instance modify -t drbd \
        -n NEW_SECONDARY INSTANCE
    gnt-instance start INSTANCE

    $ # and convert it back
    gnt-instance stop INSTANCE
    gnt-instance modify -t plain INSTANCE
    gnt-instance start INSTANCE

