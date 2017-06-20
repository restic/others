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
 * Is a dedicated to backup (sorry, [camlistore](https://camlistore.org/))

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
- `compression`: Storage with compression
- `dedup`: Supports deduplication
- `encrypted`: Supports encrypting data locally (stored encrypted on the backup medium)
- `error-correction`: Supports reconstructing data in scenarios x-of-n backup media are lost
- `golang`: Written in Go-lang
- `gpg`: Uses GPG for the underlying encryption
- `incremental`: Support for incremental backups (through deltas or local deduplication)
- `perl`: Written in Perl
- `python`: Written in Python
- `review`: Needs to be reviewed by the authors of this list in order to revise the tags assigned here.
- `rsync`: Uses `rsync` or `librsync`
- `rust`: Written in Rust
- `s3`: Supports Amazon S3-compatible backends
- `ssh`: Supports SFTP/SCP backends
- `unmaintained`: Looks unmaintained / dead

The following list is sorted alphabetically:

 * [attic](https://github.com/jborg/attic) review,dedup,encrypted,python,authenticated,unmaintained
 * [areca](http://areca-backup.org) review
 * [Arqinator](https://github.com/asimihsan/arqinator) review
 * [backshift](http://stromberg.dnsalias.org/~strombrg/backshift/) review,ssh
 * [backup](https://github.com/backup/backup) review
 * [backup2l](http://backup2l.sourceforge.net/) review
 * [BackupPC](http://backuppc.sourceforge.net/) review
 * [Backups-Done-Right](https://github.com/spikebike/Backups-Done-Right) review
 * [bareos](https://www.bareos.org/en/) review
 * [BlobSnap](https://github.com/tsileo/blobsnap) review,golang,incremental,dedup
 * [borg](https://github.com/borgbackup) review,dedup,encrypted,python,authenticated
 * [boxbackup](https://github.com/boxbackup/boxbackup) review
 * [brackup](http://search.cpan.org/~bradfitz/Brackup-1.10/lib/Brackup/Manual/Overview.pod) review,dedup,encrypted,gpg,perl,unmaintained
 * [btar](http://viric.name/cgi-bin/btar/) review
 * [btbrk](https://github.com/digint/btrbk) review
 * [bup](https://github.com/bup/bup) review,dedup,incremental,error-correction
 * [burp](http://burp.grke.org/) review
 * [casync](https://github.com/systemd/casync) dedup compression
 * [cedar-backup3](https://bitbucket.org/cedarsolutions/cedar-backup3/wiki/Home) review,python
 * [chop-backup/libchop](http://nongnu.org/libchop/) review
 * [dar](http://dar.linux.free.fr/) review
 * [ddar](https://github.com/basak/ddar) review
 * [deltaic](https://github.com/cmusatyalab/deltaic) review
 * [duplicati](https://github.com/duplicati/duplicati) review,encrypted,ssh,gpg
 * [duplicity](http://duplicity.nongnu.org/) review,encrypted,gpg,s3
 * [fwbackups](http://www.diffingo.com/oss/fwbackups/features) review
 * [Frost](https://github.com/X-Ryl669/Frost/) review,encrypted,dedup
 * [git-annex](https://git-annex.branchable.com/) review
 * [hashbackup](http://www.hashbackup.com/) review
 * [hdup2](https://wiki.archlinux.org/index.php/Hdup) review,gpg,ssh,unmaintained
 * [hindsight](https://github.com/br0ns/hindsight) review,unmaintained
 * [kebab](https://github.com/davidlazar/kebab) review,golang
 * [knoxite](https://github.com/knoxite/knoxite) review,golang,dedup,encrypted,authenticated,incremental,error-correction,compression,s3
 * [obnam](http://obnam.org/) review,encrypted,gpg
 * [ori](http://ori.scs.stanford.edu/) review
 * [preserve](https://github.com/cholcombe973/preserve) review,rust,dedup,encrypted
 * [pukcab](https://github.com/lyonel/pukcab) review,golang
 * [PyHardLinkBackup](https://github.com/jedie/PyHardLinkBackup/) dedup,python,incremental
 * [rdiff-backup](http://www.nongnu.org/rdiff-backup/) review
 * [rdedup](https://github.com/dpc/rdedup) review,dedup,rust,encrypted
 * [rdup](http://zbackup.org/) review
 * [restic](https://restic.github.io) review,golang,encrypted,authenticated,dedup,incremental,ssh,s3
 * [rsbackup](http://www.greenend.org.uk/rjk/rsbackup/) review,rsync,ssh
 * [rsnapshot](http://rsnapshot.org/) review
 * [scat](https://github.com/Roman2K/scat) go,dedup,encrypted,error-correction
 * [shield](https://github.com/starkandwayne/shield)
 * [snaprd](https://gitlab.tuebingen.mpg.de/stark/snaprd) golang,rsync
 * [snebu](http://www.snebu.com/) review
 * [s3git](https://github.com/s3git/s3git) review,golang,incremental,dedup,s3
 * [storeBackup](https://savannah.nongnu.org/projects/storebackup) review,unmaintained
 * [ugarit](https://www.kitten-technologies.co.uk/project/ugarit/doc/trunk/README.wiki) review
 * [unison](https://www.cis.upenn.edu/~bcpierce/unison/) review
 * [urbackup](https://www.urbackup.org/) review
 * [veb](https://github.com/spydez/veb) review,golang,incremental
 * [zbackup](http://zbackup.org/) review
 * [zpaq](http://mattmahoney.net/dc/zpaq.html) review,incremental,dedup,encrypted,compression

List of wrappers or helper tools:
- [atticmatic](https://torsion.org/atticmatic/) review,attic,borg
- [backupninja](https://labs.riseup.net/code/projects/backupninja) borg([WIP](https://0xacab.org/riseuplabs/backupninja/merge_requests/1)),bup,duplicity,dsync,rdiff-backup,restic([WIP](https://0xacab.org/riseuplabs/backupninja/merge_requests/2)),rsnapshot,rsync,tar
- [deja-dup](https://wiki.gnome.org/Apps/DejaDup) review,duplicity
