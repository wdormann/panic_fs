# panic_fs
Filesystems that cause an OS panic

You can write the filesystem to a USB drive using for example:
dd if=/dev/ext2_panic_fsonly.bin of=/dev/sdb1
Assuming that your USB drive lives at /dev/sdb and is partitioned to have sdb1
