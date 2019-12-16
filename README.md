# panic_fs
Filesystems that cause an OS panic.
Output from [Death by Thumb Drive](https://resources.sei.cmu.edu/library/asset-view.cfm?assetid=551450) filesystem fuzzing research.
You can write the filesystem to a USB drive using for example:

`dd if=/dev/ext2_panic_fsonly.bin of=/dev/sdb1`

Assuming that your USB drive lives at `/dev/sdb` and is partitioned to have `sdb1`

| File                                                               | Target OS   | Fixed              | Unlocked session required | Interaction Required | Date Vendor Notified
| -----------                                                        | ----------- | ---                | ---                       | --- | ---
| [ext2_panic_fsonly.bin](ext2_panic_fsonly.bin)                     | Linux       | **No**             | Varies                    | Varies | 22 Aug, 2019
| [ntfs_panic_macos_fsonly.bin](ntfs_panic_macos_fsonly.bin)         | MacOS       | **No**             | Yes                       | Yes (browse) | 1 Mar, 2019
| [ntfs_panic_macos_old_fsonly.bin](ntfs_panic_macos_old_fsonly.bin) | MacOS       | Yes<br>(in Mavericks) | Yes                       | **No** | 1 Mar, 2019
| [ntfs_panic_windows_fsonly.bin](ntfs_panic_windows_fsonly.bin)     | Windows     | **No**             | **No**                    | **No** | 8 Mar, 2019
