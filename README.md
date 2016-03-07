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

TODO
====

In the future we plan to provide benchmarks using [fakedatafs](https://github.com/restic/fakedatafs) and a table to sort by the tag categories.

If anyone wants to help out, please submit a PR with your contribution.

List of Backup Software
=======================

Tags used below:
- `authenticated`: Uses cryptographic signatures or MAC tags to ensure integrity
- `dedup`: Supports deduplication
- `encrypted`: Supports encrypting data locally (stored encrypted on the backup medium)
- `error-correction`: Supports reconstructing data in scenarios x-of-n backup media are lost
- `golang`: Written in Go-lang
- `gpg`: Uses GPG for the underlying encryption
- `incremental`: Support for incremental backups (through deltas or local deduplication)
- `python`: Written in Python
- `review`: Needs to be reviewed by the authors of this list in order to revise the tags assigned here.
- `rsync`: Uses `rsync` or `librsync`
- `s3`: Supports Amazon S3-compatible backends
- `ssh`: Supports SFTP/SCP backends
- `unmaintained`: Looks unmaintained / dead

The following list is sorted alphabetically:

 * [attic](https://github.com/jborg/attic) review,dedup,encrypted,python,authenticated,unmaintained
 * [areca](http://areca-backup.org) review
 * [backshift](http://stromberg.dnsalias.org/~strombrg/backshift/) review,ssh
 * [backup](https://github.com/backup/backup) review
 * [backup2l](http://backup2l.sourceforge.net/) review
 * [backupninja](https://labs.riseup.net/code/projects/backupninja) review
 * [BackupPC](http://backuppc.sourceforge.net/) review
 * [bareos](https://www.bareos.org/en/) review
 * [borg](https://github.com/borgbackup) review,dedup,encrypted,python,authenticated
 * [boxbackup](https://github.com/boxbackup/boxbackup) review
 * [btar](http://viric.name/cgi-bin/btar/) review
 * [btbrk](https://github.com/digint/btrbk) review
 * [bup](https://github.com/bup/bup) review,dedup,incremental,error-correction
 * [burp](http://burp.grke.org/) review
 * [cedar-backup3](https://bitbucket.org/cedarsolutions/cedar-backup3/wiki/Home) review,python
 * [chop-backup/libchop](http://nongnu.org/libchop/) review
 * [dar](http://dar.linux.free.fr/) review
 * [ddar](https://github.com/basak/ddar) review
 * [deltaic](https://github.com/cmusatyalab/deltaic) review
 * [duplicati](https://github.com/duplicati/duplicati) review,encrypted,ssh,gpg
 * [duplicity](http://duplicity.nongnu.org/) review,encrypted,gpg
 * [fwbackups](http://www.diffingo.com/oss/fwbackups/features) review
 * [git-annex](https://git-annex.branchable.com/) review
 * [hashbackup](http://www.hashbackup.com/) review
 * [hdup2](https://wiki.archlinux.org/index.php/Hdup) review,gpg,ssh,unmaintained
 * [hindsight](https://github.com/br0ns/hindsight) review,unmaintained
 * [obnam](http://obnam.org/) review,encrypted,gpg
 * [ori](http://ori.scs.stanford.edu/) review
 * [pukcab](https://github.com/lyonel/pukcab) review,golang
 * [rdiff-backup](http://www.nongnu.org/rdiff-backup/) review
 * [rdup](http://zbackup.org/) review
 * [restic](https://restic.github.io) review,golang,encrypted,authenticated,dedup,incremental,ssh,s3
 * [rsbackup](http://www.greenend.org.uk/rjk/rsbackup/) review,rsync,ssh
 * [rsnapshot](http://rsnapshot.org/) review
 * [snebu](http://www.snebu.com/) review
 * [storeBackup](https://savannah.nongnu.org/projects/storebackup) review,unmaintained
 * [ugarit](https://www.kitten-technologies.co.uk/project/ugarit/doc/trunk/README.wiki) review
 * [unison](https://www.cis.upenn.edu/~bcpierce/unison/) review
 * [zbackup](http://zbackup.org/) review

List of wrappers or helper tools:
- [atticmatic](https://torsion.org/atticmatic/) review,attic,borg
- [deja-dup](https://wiki.gnome.org/Apps/DejaDup) review,duplicity
