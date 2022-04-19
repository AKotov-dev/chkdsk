# chkdsk
Bash script for automatic error correction on ntfs partition in Linux. Just run the command with 'su' privileges: `chkdsk`.

If two operating systems (Windows/Linux) are on the same disk at the same time, when the first one is shut down incorrectly, problems often arise with mounting NTFS partitions in the second one, or they are monitored in read-only mode. The packages contain the `/usr/bin/chkdsk` script for quick repair of this malfunction. This script is not an analogue of the `chkdsk` program from Windows (С), it uses the `ntfsfix` utility from the `ntfs-3g` package.  
Designed for Mageia/Fedora/Ubuntu/etc...
