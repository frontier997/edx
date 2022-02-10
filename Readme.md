
### This repository contains the edx series 1 emulator.

Code documentation:

* edxsport.sys configuration file - this file configures the edxsport utility controls for:
  * logfile /edx/edxsport.log
  * System parameters are specifed here.
  * EDX devices are specified here.  Each device will be passed through to the specified TCP port via a symbolic link and a pseudo terminal.
  * TCP port number for device
