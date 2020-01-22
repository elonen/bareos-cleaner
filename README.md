# bareos-cleaner

BASH tools cleaning up Bareos database and file storage.

This is a purely pragmatic toolset, i.e. no plans for making it a "product" of any kind for now!

Current commands:


    -e
       delete empty (JobBytes=0) jobs
    -p
       prune all volumes
    -t
       update all volumes to "actiononpurge=Truncate"
    -n
       update all volumes to "actiononpurge=None"
    -Dc
       delete all jobs that have a copy job
    -Do
       delete obsolete volume files from the disk (those not listed in catalog)
         NOTE: this operation can take several minutes to complete
    -Dp
       delete all purged volumes from Bacula catalog
    -h
       print this screen
       
## USAGE: 
 
    export BAREOS_POOLDIR=/mnt/bareos
    bareos-cleanup -e
