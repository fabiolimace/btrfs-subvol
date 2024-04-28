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
- subvol snapshot create [SUBVOLUME|all] [HINT]
- subvol snapshot delete SUBVOLUME [SNAPSHOT|NUMBER|RANGE]
- subvol snapshot rollback SUBVOLUME [SNAPSHOT|NUMBER]
- subvol struct help
- subvol struct check
- subvol struct init
- subvol free

### Structure

The subvolumes and snapshots are organized in the folowing directories:

- /subvol
- /subvol/subvolumes
- /subvol/snapshots

Note that by default the structure is on the file system root. You can change the variable `SUBVOL_BASE_DIR` to use another directory.

### Installation

1. Copy the script `subvol` to `/usr/local/bin/`

```bash
sudo cp 'subvol' '/usr/local/bin/';
sudo chmod +x '/usr/local/bin/subvol';
```

2. Initiate the `subvol` structure on `/subvol` directory

```bash
subvol struct init
```

### Automatic snapshot on system boot

Execute these steps to enable automatic snapshots on boot.

1. Copy the service script to `/etc/systemd/system`:

```bash
sudo cp 'subvol-snapshot-auto.service' '/etc/systemd/system/'
```

2. Enable the service script:

```bash
sudo systemctl enable subvol-snapshot-auto.service
```

// The end
