# auto-usb-storage-mount

## Welcome to the Rebellion of Mounting

Ever felt like the world of Linux mounting was too orderly, too predictable, too... structured? Enter `auto-usb-storage-mount`, the anarchist in the world of USB drive management. This software doesn't just mount your USB drives; it launches a full-scale revolution against the tyranny of manual mounting, making your drives appear exactly where you want them, as if by magic (or anarchy).

### Features

- **Auto-Magic Mounting**: Why bother with the mundane task of manually mounting USB drives when `auto-usb-storage-mount` can do it for you? It's like having your own personal rebellion against the establishment, but for USB drives.
- **User-Specific Anarchy**: Mount drives with the precision of a graffiti artist tagging a moving train. Each drive is mounted according to your whims (or the instructions you've painstakingly provided in a config file).
- **Persistent Insistence**: Like the most dedicated of protesters, `auto-usb-storage-mount` doesn't give up. It keeps your drives mounted.

### Installation: Join the Movement

Liberate your USB drives with these simple commands. First, seize the software from the clutches of GitHub:

```bash
wget https://raw.githubusercontent.com/psyb0t/auto-usb-storage-mount/master/auto-usb-storage-mount
```

Next, empower the script with the ability to execute its mission:

```bash
chmod +x auto-usb-storage-mount
```

Finally, place `auto-usb-storage-mount` in a position of power, within your `/usr/local/bin`:

```bash
sudo mv auto-usb-storage-mount /usr/local/bin/
```

### Usage

To deploy `auto-usb-storage-mount` in the field, simply invoke its name followed by the path to your configuration manifest (a.k.a. the mount rules file):

```bash
sudo auto-usb-storage-mount /path/to/your/mount_rules.txt
```

Prepare to watch in awe as your USB drives are mounted in defiance of the manual methods of old.

### Configuration: The Rules of Engagement

Your `mount_rules.txt` is the manifesto of this mounting rebellion. It outlines which drives are to be mounted and where, all in a format that even the most sleep-deprived sysadmin could understand:

```
PARTUUID@username:/mount/point
```

How to get PARTUUID:

```bash
sudo blkid /dev/sda1
```

This spits out something like `/dev/sda1: BLOCK_SIZE="512" UUID="7FEC5B8016173001" TYPE="ntfs" PARTLABEL="Elements" PARTUUID="0f119989-6380-4106-896e-f8e6372170ee"`

Replace `PARTUUID` with the PARTUUID of your device, `username` with the user you wish to own the mount point, and `/mount/point` with the desired location in the filesystem.

### License: WTFPL

`auto-usb-storage-mount` is released under the Do What The F**_ You Want To Public License (WTFPL), the most anarchic license in the world of open source. Copy it, modify it, distribute it – do whatever the F_** you want with it. Because, in the end, isn't that what software freedom is all about?

Join us in the mounting rebellion with `auto-usb-storage-mount`. Together, we can overthrow the tyranny of manual mounting, one USB drive at a time.
