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
 * Is a dedicated to backup (sorry, [perkeep](https://perkeep.org/))

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

List of tags used
=================

- `authenticated`: Uses cryptographic signatures or MAC tags to ensure integrity
- `compression`: Storage with compression
- `dedup`: Supports deduplication
- `dbsrc`: backup a database by properly dumping its data, rather than simply copying its files
- `encrypted`: Supports encrypting data locally (stored encrypted on the backup medium)
- `error-correction`: Supports reconstructing data in scenarios x-of-n backup media are lost
- `golang`: Written in Go-lang
- `gpg`: Uses GPG for the underlying encryption
- `incremental`: Support for incremental backups (through deltas or local deduplication)
- `perl`: Written in Perl
- `python`: Written in Python
- `repo`: rather than creating separate archives (tarball or similar), the program operates on a repository/store
- `review`: Needs to be reviewed by the authors of this list in order to revise the tags assigned here.
- `rsync`: Uses `rsync` or `librsync`
- `rust`: Written in Rust
- `s3`: Supports Amazon S3-compatible backends
- `ssh`: Supports SFTP/SCP backends
- `unmaintained`: Looks unmaintained / dead

### The list, sorted alphabetically, also contain some wrappers or helper tools and can be found at [table.csv](table.csv).
