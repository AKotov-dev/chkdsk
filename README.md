# chkdsk
Bash script for automatic error correction on ntfs partition in Linux. Just run the command with 'su' privileges: `chkdsk`.

If two operating systems (Windows/Linux) are on the same disk at the same time, when the first one is shut down incorrectly, problems often arise with mounting NTFS partitions in the second one, or they are monitored in read-only mode. The packages contain the `/usr/bin/chkdsk` script for quick repair of this malfunction. This script is not an analogue of the `chkdsk` program from Windows (С), it uses the `ntfsfix` utility from the `ntfs-3g` package. In addition to eliminating common errors, the option is used `-d` to fix dirty states.
  
Demonstration of the correction of NTFS errors:
```
> chkdsk
Mounting volume... The disk contains an unclean file system (0, 0).
Metadata kept in Windows cache, refused to mount.
FAILED
Attempting to correct errors... 
Processing $MFT and $MFTMirr...
Reading $MFT... OK
Reading $MFTMirr... OK
Comparing $MFTMirr to $MFT... OK
Processing of $MFT and $MFTMirr completed successfully.
Setting required flags on partition... OK
Going to empty the journal ($LogFile)... OK
Checking the alternate boot sector... OK
NTFS volume version is 3.1.
NTFS partition /dev/sda3 was processed successfully.
```
Designed for Mageia/Fedora/Ubuntu/etc...
