!SLIDE commandline

# Listing Jobs

    $ gnt-job list
    17771 success INSTANCE_QUERY_DATA
    17773 success CLUSTER_VERIFY_DISKS
    17775 success CLUSTER_REPAIR_DISK_SIZES
    17776 error   CLUSTER_RENAME(cluster.example.com)
    17780 success CLUSTER_REDIST_CONF
    17792 success INSTANCE_REBOOT(instance1.example.com)

!SLIDE commandline

# Detailed Info

    $ gnt-job info 17776
    Job ID: 17776
      Status: error
      Received:         2009-10-25 23:18:02.180569
      Processing start: 2009-10-25 23:18:02.200335 (delta 0.019766s)
      Processing end:   2009-10-25 23:18:02.279743 (delta 0.079408s)
      Total processing time: 0.099174 seconds
      Opcodes:
        OP_CLUSTER_RENAME
          Status: error
          Processing start: 2009-10-25 23:18:02.200335
          Processing end:   2009-10-25 23:18:02.252282
          Input fields:
            name: cluster.example.com
          Result:
            OpPrereqError
            [Neither the name nor the IP address of the cluster has changed]
          Execution log:

!SLIDE commandline tiny smcommandline

# Watching a job

    $ gnt-instance add --submit … instance1
    JobID: 17818
    $ gnt-job watch 17818
    Output from job 17818 follows
    -----------------------------
    Mon Oct 26 2009  - INFO: Selected nodes for instance instance1 via iallocator dumb: node1, node2
    Mon Oct 26 2009 * creating instance disks...
    Mon Oct 26 2009 adding instance instance1 to cluster config
    Mon Oct 26 2009  - INFO: Waiting for instance instance1 to sync disks.
    …
    Mon Oct 26 2009 creating os for instance instance1 on node node1
    Mon Oct 26 2009 * running the instance OS create scripts...
    Mon Oct 26 2009 * starting instance...

