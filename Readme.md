
### This repository contains the edx series 1 emulator.

Code documentation:

* edxsport.sys configuration file - this file configures the edxsport utility, log file, and also tco oirts, 
     associated paths
     * logfile /edx/edxsport.log

> # System parameters are specifed here.
#   logfile - Log messages to specified file

# EDX devices are specified here.  Each device will be passed through
# to the specified TCP port via a symbolic link and a pseudo terminal.
#   port     - TCP port number for device
