# btrfs-subvol

### Description

Subvol is a simple tool for BTRFS subvolumes and snapshots.

### How to use

- subvol help
- subvol list
- subvol create SUBVOLUME
- subvol delete SUBVOLUME
- subvol snapshot help
- subvol snapshot list SUBVOLUME
- subvol snapshot create SUBVOLUME [HINT]
- subvol snapshot delete SUBVOLUME [SNAPSHOT|NUMBER]
- subvol snapshot rollback SUBVOLUME [SNAPSHOT|NUMBER]
- subvol struct help
- subvol struct check
- subvol struct init

### Structure

The subvolumes and snapshots are organized in the folowing directories:

- /subvol
- /subvol/subvolumes
- /subvol/snapshots
