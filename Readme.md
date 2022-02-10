
### This repository contains the edx series 1 emulator.

Code documentation:

* <b>edxsport.sys</b> configuration file supporting the edxsport utility controls for:
  * logfile /edx/edxsport.log
  * System parameters are specifed here.
  * EDX devices are specified here.  Each device will be passed through to the specified TCP port via a symbolic link and a pseudo terminal.
  * TCP port number for device


* <b>ipledx</b> - edx device / pc user paths

```console
PATH=$PATH:/edx/bin:
export PATH
# desktop pc's
edx -B -d /dev/edxtty001
edx -B -d /dev/edxtty002
edx -B -d /dev/edxtty003
edx -B -d /dev/edxtty004
edx -B -d /dev/edxtty005
edx -B -d /dev/edxtty006
edx -B -d /dev/edxtty007
edx -B -d /dev/edxtty008
edx -B -d /dev/edxtty009
edx -B -d /dev/edxtty010
edx -B -d /dev/edxtty011
edx -B -d /dev/edxtty012
edx -B -d /dev/edxtty013
edx -B -d /dev/edxtty014
edx -B -d /dev/edxtty015
# serial terminals IBM 3151 or 3153
# if you use one of these ports for a printer
# you must delete the command below for that port
edx -B -d /dev/ttyS0
```console
