# chkdsk
Bash script for automatic error correction on ntfs partition in Linux. Just run the command with 'su' privileges: `chkdsk`.

If two operating systems (Windows/Linux) are on the same disk at the same time, when the first one is shut down incorrectly, problems often arise with mounting NTFS partitions in the second one, or they are monitored in read-only mode. The packages contain the `/usr/bin/chkdsk` script for quick repair of this malfunction. This script is not an analogue of the `chkdsk` program from Windows (С), it uses the `ntfsfix` utility from the `ntfs-3g` package.  
```
> chkdsk
Mounting volume... OK
Processing of $MFT and $MFTMirr completed successfully.
Checking the alternate boot sector... OK
NTFS volume version is 3.1.
NTFS partition /dev/sda3 was processed successfully.
```
Designed for Mageia/Fedora/Ubuntu/etc...
