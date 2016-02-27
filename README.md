Introduction
============

During my ([@fd0](https://github.com/fd0)) research before starting
[restic](https://restic.github.io) I've tested a lot of different backup
programs. However, even after working in this space for a few years, I still
stumble across backup solutions I didn't know about.

In this repository, I'd like to collect backup solutions and eventually end up
with an exhaustive list of backup software. The criteria for inclusion are:

 * Free Software (not just Open Source)
 * Does not require custom network/cloud service to operate (sorry,
   [tarsnap](http://www.tarsnap.com/))
 * Works on Linux

If you know other backup solutions that fit the criteria above, please create a
pull request!

Note:
=====

A lot of FOSS backup solutions are merely shells on top of rsync and/or duplicity.
Perhaps these should have a category of their own, or a tag?

List of Backup Software
=======================

Tags used below:
- `dedup`: Supports deduplication
- `encrypted`: Supports encrypting data locally (stored encrypted on the backup medium)
- `go`: Written in Go-lang
- `python`: Written in Python
- `review`: Needs to be reviewed by the authors of this list in order to revise the tags assigned here.
- `unmaintained`: Looks unmaintained / dead

The following list is sorted alphabetically:

 * [attic](https://github.com/jborg/attic) review,dedup,encrypted,python,review,unmaintained
 * [areca](http://areca-backup.org) review
 * [backshift](http://stromberg.dnsalias.org/~strombrg/backshift/) review
 * [backup](https://github.com/backup/backup) review
 * [backup2l](http://backup2l.sourceforge.net/) review
 * [backupninja](https://labs.riseup.net/code/projects/backupninja) review
 * [BackupPC](http://backuppc.sourceforge.net/) review
 * [bup](https://github.com/bup/bup) review
 * [burp](http://burp.grke.org/) review
 * [borg](https://github.com/borgbackup) review
 * [btar](http://viric.name/cgi-bin/btar/) review
 * [chop-backup/libchop](http://nongnu.org/libchop/) review
 * [dar](http://dar.linux.free.fr/) review
 * [ddar](https://github.com/basak/ddar) review
 * [deltaic](https://github.com/cmusatyalab/deltaic) review
 * [duplicati](https://github.com/duplicati/duplicati) review
 * [duplicity](http://duplicity.nongnu.org/) review,encrypted
 * [fwbackups](http://www.diffingo.com/oss/fwbackups/features) review
 * [git-annex](https://git-annex.branchable.com/) review
 * [hashbackup](http://www.hashbackup.com/) review
 * [hindsight](https://github.com/br0ns/hindsight) review,unmaintained
 * [obnam](http://obnam.org/) review
 * [rdiff-backup](http://www.nongnu.org/rdiff-backup/) review
 * [restic](https://restic.github.io) review,go,encrypted,dedup
 * [rdup](http://zbackup.org/) review
 * [rsnapshot](http://rsnapshot.org/) review
 * [ugarit](https://www.kitten-technologies.co.uk/project/ugarit/doc/trunk/README.wiki) review
 * [zbackup](http://zbackup.org/) review
