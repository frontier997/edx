
## This repository contains the edx series 1 emulator.

<hr>

### Code documentation:

* <b>edxsport.sys</b> configuration file supporting the edxsport utility controls for:
  * logfile /edx/edxsport.log
  * System parameters are specifed here.
  * EDX devices are specified here.  Each device will be passed through to the specified TCP port via a symbolic link and a pseudo terminal.
  * TCP port number for device

<hr>
* <b>ipledx</b> - edx device / pc user paths

Code excerpt indicates 15 workstation ports and asssociated linux path structure:

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
```

<hr>

#### edxnuc -- edxnuc appears to be a primary program driver

* <b> nucxref.sys </b> base and output paths for edxnuc 

```console
BLDNUC:
	base=/edx/edx002/edxpcnuc.edx
	output=/edx/edx002/edxnuc02.edx
```


Associated sys files and code excerpts with internal docstrings referencing edxnuc:

* <b>volxref.sys</b> - $$$EDXNUC is a required stanza which names the sysgen module and the default volume.

This sys file appears to define volume mappings and parameter references for data migration.

```console
# Individual volume stanzas match the VOL parameters specified in the $$$DISK??
# stanzas.  Volume stanzas are only requred to specify a path other than
# the default path created by appending the volume name to the $EDXDIR
# directory, or to specify optional parameters for the volume.  
#
# Parameter   		Description
# ---------   		-----------
# MODE [RO | RW]	Specify read-only or read-write volume
# FASTLOAD <program>	Specify a program to be cached for fast loading.
#
EDX001 /edx/edx001:
EDX002 /edx/edx002:
EDX003 /edx/edx003:
EDX004 /edx/edx004:
EDX005 /edx/edx005:
OBJLIB /edx/objlib:
SOURCE /edx/source:
OLD002 /edx/old002:
NEW002 /edx/new002:
ASMLIB /edx/asmlib:
ASMMAC /edx/asmmac:
EDXMAX /edx/edxmax:
ARC1 /edx/arc1:
BAK003 /edx/bak003:
BAK004 /edx/bak004:
BAK005 /edx/bak005:
```


* <b> termxref.sys </b>

```console
# These lines will specify a tty for terminals start automatically by edxnuc
# The default stanza above will apply to these terminals.
# $SYSLOGX-Z are examples of workstation setup 
# $SYSLOGX  /dev/ttyD000:   Digi
# $SYSLOGY  /dev/ttyS0:     Com1
# $SYSLOGZ  /dev/edxtty00a: Network
```


