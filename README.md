# rclone-sync-zfs

Whis wrapper script creates a snapshot of a given ZFS dataset and calls rclone
to sync it with a remote folder. Snapshots might be resursive.
Because of snapshot - the created clone is always consistent. No data might change
during synchronization process.

Note:
Because of need to create/destoy snapshot and mount/umount it - this script is to be run as root!

# USAGE

    rclone-sync-zfs source_dataset rclone_destination

Example:

    rclone-sync-zfs mypool/mydataset remote:folder

See configuration variables inside the script.
