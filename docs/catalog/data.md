# Data: Storage, Backups & Databases

This page catalogs self-hostable tools for storing and managing data: SQL and NoSQL databases, encryption utilities, backup and snapshot systems, archiving platforms, storage management tools, and file systems.

[← Catalog index](./README.md) · [← Handbook home](../../README.md)

## Databases

SQL is a standard language for storing, manipulating, and retrieving data in relational databases; NoSQL refers to nonrelational databases designed to handle large volumes of unstructured or rapidly changing data.

### SQL

- [Coolify](https://coolify.io/) — Open-source, self-hostable Heroku/Netlify alternative.
- [MySQL](https://www.mysql.com/) — Widely used open source relational database.
- [PostgreSQL](https://www.postgresql.org/) — Open source object-relational database system with a long track record for reliability and performance.
- [PostgREST](https://github.com/PostgREST/postgrest) — Serves a RESTful API from any existing PostgreSQL database.
- [NocoDB](https://www.nocodb.com/) — Open source no-code platform that turns MySQL, PostgreSQL, SQL Server, SQLite, and MariaDB into a spreadsheet interface.
- [DBeaver](https://dbeaver.io/) — Multi-platform database tool supporting MySQL, PostgreSQL, SQLite, Oracle, DB2, SQL Server, and many others.
- [OmniDB](https://github.com/OmniDB/OmniDB) — Web-based tool for database management.
- [Navicat](https://www.navicat.com/) — Graphical database management and development software for MySQL, MariaDB, MongoDB, Oracle, SQLite, PostgreSQL, and SQL Server.
- [HeidiSQL](https://www.heidisql.com/) — Tool for viewing and editing data and structures in MariaDB, MySQL, Microsoft SQL, PostgreSQL, and SQLite.
- [Beekeeper Studio](https://www.beekeeperstudio.io/) — Cross-platform SQL editor and database manager for MySQL, Postgres, SQLite, SQL Server, and more, on Linux, Mac, and Windows.
- [UI Bakery](https://uibakery.io/) — Web-based low-code internal tool builder that visualizes data from PostgreSQL, MongoDB, MySQL, Microsoft SQL, and Redis.
- [IBM DB2](https://www.ibm.com/analytics/db2) — Hybrid data management product suite for structured and unstructured data on premises and in the cloud.
- [OracleDB](https://www.oracle.com/database/) — Managed relational database for business-critical data.
- [MariaDB](https://mariadb.com/) — Open source relational database for mission-critical applications.
- [EventQL](https://eventql.io/documentation/) — Distributed analytical database for storing structured data and querying it with SQL.
- [CockroachDB](https://www.cockroachlabs.com/docs/stable/) — Distributed SQL database for global, scalable cloud services that survive failures.
- [SQLite](https://sqlite.org/index.html) — Self-contained, embedded SQL database engine in a C library.
- [SQLite Database Browser](https://sqlitebrowser.org/) — Open source tool to create, design, and edit SQLite database files.
- [TimescaleDB](https://github.com/timescale/timescaledb) — Open source time-series database packaged as a PostgreSQL extension.
- [InfluxDB](https://www.influxdata.com/) — Open source time-series platform with APIs for storing, querying, and processing data.
- [Atlas](https://github.com/Netflix/atlas) — In-memory dimensional time-series database.
- [dbWatch](https://www.dbwatch.com/) — Database monitoring and management solution for SQL Server, Oracle, PostgreSQL, Sybase, MySQL, and Azure.
- [Adminer](https://www.adminer.org/) — SQL management client for databases, tables, relations, indexes, and users, supporting MySQL, MariaDB, PostgreSQL, SQLite, MS SQL, Oracle, and more.
- [Knex](https://github.com/knex/knex) — Query builder for PostgreSQL, MySQL, CockroachDB, SQL Server, SQLite3, and Oracle.
- [rqlite](https://github.com/rqlite/rqlite) — Lightweight distributed relational database that uses SQLite as its storage engine.
- [osquery](https://github.com/osquery/osquery) — SQL-powered operating system instrumentation, monitoring, and analytics framework.
- [SQLModel](https://github.com/tiangolo/sqlmodel) — Library for interacting with SQL databases from Python using Python objects.
- [Citus](https://github.com/citusdata/citus) — PostgreSQL extension that transforms Postgres into a distributed database.
- [DbVisualizer](https://dbvis.com/) — SQL management tool for databases including Oracle, Sybase, SQL Server, MySQL, H3, and SQLite.
- [AppDynamics Database](https://www.appdynamics.com/supported-technologies/database) — Management product for monitoring Microsoft SQL Server performance metrics.
- [Toad](https://www.quest.com/toad/) — SQL Server DBMS toolset for relational and non-relational databases.
- [Lepide SQL Server](https://www.lepide.com/sql-storage-manager/) — Storage manager utility for analyzing SQL Server performance and tracking configuration and permission changes.
- [Sequel Pro](https://sequelpro.com/) — macOS database management tool for working with MySQL.
- [ElasticSearch](https://www.elastic.co/) — Distributed, multitenant full-text search engine based on the Lucene library, with an HTTP interface and schema-free JSON documents.
- [Logstash](https://www.elastic.co/products/logstash) — Tool for managing events and logs, covering collection, processing, storage, and searching.
- [Kibana](https://www.elastic.co/products/kibana) — Data visualization plugin for Elasticsearch.
- [Trino](https://trino.io/) — Distributed SQL query engine for big data across numerous data sources.
- [Tableau](https://www.tableau.com/) — Data visualization software for relational databases, cloud databases, and spreadsheets.
- [DataGrip](https://www.jetbrains.com/datagrip/) — Database IDE with context-sensitive code completion aware of table structure and foreign keys.
- [RStudio](https://rstudio.com/) — Integrated development environment for R and Python with a console, editor, and plotting and debugging tools.

### NoSQL

- [Scylla](https://github.com/scylladb/scylla) — Real-time big data database that is API-compatible with Apache Cassandra and Amazon DynamoDB.
- [Apache Cassandra](https://cassandra.apache.org/) — Open source NoSQL distributed database offering linear scalability and fault tolerance.
- [Apache HBase](https://hbase.apache.org/) — Open source NoSQL distributed big data store for random, real-time access to large, sparse datasets.
- [Hadoop Distributed File System (HDFS)](https://www.ibm.com/analytics/hadoop/hdfs) — Distributed file system for large data sets running on commodity hardware, a core component of Apache Hadoop.
- [Redis](https://redis.io/) — Open source in-memory data structure store used as a database, cache, and message broker.
- [FoundationDB](https://www.foundationdb.org/) — Open source distributed database that organizes data as an ordered key-value store with ACID transactions.
- [CouchbaseDB](https://www.couchbase.com/) — Open source distributed multi-model NoSQL document-oriented database with a managed cache and query engine.
- [MongoDB](https://www.mongodb.com/) — Document database that stores data in JSON-like documents.
- [NoSQLBooster](https://www.nosqlbooster.com/) — Cross-platform IDE for MongoDB with a script debugger, SQL query support, and server monitoring tools.
- [ClickHouse](https://github.com/ClickHouse/ClickHouse) — Open source column-oriented database management system for real-time analytical reports.
- [Neo4j](https://neo4j.com/) — Graph database management system with tools, libraries, and frameworks for development.

## Encryption

- [VeraCrypt](https://www.veracrypt.fr/code/VeraCrypt/) — Open source disk encryption software for Windows, macOS, and Linux with real-time, on-the-fly encryption.
- [AxCrypt](https://axcrypt.net/) — Encryption tool for Windows, macOS, iOS, and Android.
- [AESCrypt](https://www.aescrypt.com/) — File encryption utility using AES, available for Windows, macOS, and Linux.
- [Linux Unified Key Setup (LUKS)](https://www.redhat.com/sysadmin/disk-encryption-luks) — Disk encryption specification using dm-crypt to handle encryption at the block device level.
- [GNU Privacy Guard (GnuPG)](https://gnupg.org/) — Free implementation of the OpenPGP standard for encrypting and signing data and communications, with key management.
- [Pretty Good Privacy (PGP)](https://en.wikipedia.org/wiki/Pretty_Good_Privacy) — Encryption program providing cryptographic privacy and authentication for signing, encrypting, and decrypting data.
- [Deadbolt](https://github.com/alichtman/deadbolt) — File encryption tool for any OS.
- [Infisical](https://infisical.com/) — Open source, end-to-end encrypted platform to sync secrets and configs across teams and infrastructure.
- [Hemmelig.app](https://github.com/HemmeligOrg/Hemmelig.app) — Tool for sharing sensitive information as encrypted secrets.

## Backups

- [Proxmox Backup Server](https://www.proxmox.com/en/proxmox-backup-server) — Open source backup solution for VMs, containers, and physical hosts, with incremental backups, deduplication, Zstandard compression, and authenticated encryption.
- [BackupPC](https://github.com/backuppc/backuppc) — System for backing up Linux, Windows, and macOS machines to a server's disk.
- [BorgWarehouse](https://borgwarehouse.com/) — Web UI for a BorgBackup central repository server.
- [Emborg](https://emborg.readthedocs.io/en/latest/) — Command line utility to orchestrate backups as a front-end to Borg.
- [Borgmatic](https://github.com/modem7/docker-borgmatic) — Configuration-driven backup software for servers and workstations with client-side encryption and database support.
- [Vorta](https://vorta.borgbase.com/) — Backup client for macOS and Linux desktops built on Borg Backup.
- [UrBackup](https://www.urbackup.org/) — Open source client/server backup system combining image and file backups, for Windows, macOS, and Linux.
- [Kopia](https://kopia.io/) — Desktop app for Windows, macOS, and Linux to create snapshots, define policies, and restore files with encrypted backups.
- [Clonezilla](https://clonezilla.org/) — Partition and disk imaging/cloning program for system deployment and bare-metal backup and recovery.
- [rsnapshot](https://rsnapshot.org/) — Filesystem snapshot utility based on rsync for periodic snapshots of local and remote machines over ssh.
- [Duplicity](https://duplicity.us/) — Tool that backs up directories as encrypted tar-format volumes using librsync for space-efficient incremental archives.
- [ZnapZend](https://www.znapzend.org/) — Open source ZFS backup with mbuffer and ssh support, using ZFS snapshots for consistent backups.
- [SnapRAID](https://github.com/amadvance/snapraid) — Folder-based backup tool that behaves like a software RAID5/6 disk array without being a disk array itself.
- [rsync.net](https://rsync.net/) — Cloud storage for offsite backup providing a UNIX filesystem accessible via SSH, built on ZFS, with support for rsync, sftp, scp, borg, rclone, restic, and git-annex.

## Snapshots & System Recovery

- [rsnapshot](https://rsnapshot.org/) — Filesystem snapshot utility based on rsync for periodic snapshots of local and remote machines over ssh.
- [rsync.net](https://rsync.net/) — Cloud storage for offsite backup providing a UNIX filesystem accessible via SSH, built on ZFS.
- [ZnapZend](https://www.znapzend.org/) — Open source ZFS backup with mbuffer and ssh support, using ZFS snapshots for consistent backups.
- [Sanoid](https://github.com/jimsalterjrs/sanoid) — Policy-driven snapshot management tool for ZFS filesystems.
- [ZFSBootMenu](https://zfsbootmenu.org/) — Linux bootloader that allows multiple boot environments, snapshot manipulation before booting, and bootstrapping installs via `zfs recv`.
- [Btrfs maintenance toolbox](https://github.com/kdave/btrfsmaintenance) — Set of scripts to automate btrfs maintenance tasks such as scrub, balance, snapshots, trim, and defragmentation.
- [Btrbk](https://github.com/digint/btrbk) — Backup tool for btrfs subvolumes that creates atomic snapshots and transfers them incrementally.
- [ksync](https://github.com/ksync/ksync) — Tool that syncs files between a local system and a Kubernetes cluster.
- [Verify](https://github.com/VerifyTests/Verify) — Snapshot tool for asserting complex data models and documents.
- [Timeshift](https://github.com/linuxmint/timeshift) — Linux application for system restore, taking snapshots at regular intervals for restoration or undo.
- [CRIU (Checkpoint and Restore in Userspace)](https://github.com/checkpoint-restore/criu) — Utility to checkpoint a running Linux application to disk and restore it later.
- [Rsync time backup](https://github.com/laurent22/rsync-time-backup) — Time Machine style incremental backup with rsync for Linux, macOS, and Windows via WSL.
- [rdiff-backup](https://rdiff-backup.net/) — Backup tool for local and remote use on Linux, Windows, and other platforms.
- [Mainframer](https://github.com/buildfoundation/mainframer) — Tool that executes a command on a remote machine while syncing files back and forth.

## Archiving

- [Access to Memory (AtoM)](https://www.accesstomemory.org/) — Web-based, open source application for standards-based archival description and access in a multilingual, multi-repository environment.
- [ArchiveBox](https://archivebox.io/) — Self-hosted wayback machine that creates HTML and screenshot archives of sites from bookmarks, browsing history, RSS feeds, and other sources.
- [Archivematica](https://www.archivematica.org/en/) — Digital preservation system for standards-based, long-term access to collections of digital objects.
- [ArchivesSpace](https://archivesspace.org/) — Archives information management application for managing and providing web access to archives, manuscripts, and digital objects.
- [CKAN](https://ckan.org) — Tool for making open data websites.
- [Collective Access - Providence](https://collectiveaccess.org/) — Web-based framework for management, description, and discovery of digital and physical collections supporting various metadata standards, data types, and media formats.
- [Omeka S](https://omeka.org/s/) — Web publication system for universities, galleries, libraries, archives, and museums, with independently curated exhibits sharing a pool of items and metadata.
- [Wayback](https://github.com/wabarc/wayback) — Self-hosted toolkit for archiving webpages to the Internet Archive, archive.today, IPFS, and local file systems.

## Storage

- [Scrutiny](https://github.com/AnalogJ/scrutiny) — Web UI for smartd hard drive S.M.A.R.T. monitoring, historical trends, and failure thresholds.
- [smartd](https://www.smartmontools.org/) — SMART disk monitoring daemon for Linux that controls and monitors ATA/SATA, SCSI/SAS, and NVMe disks.
- [DUA (Disk Usage Analyzer)](https://lib.rs/crates/dua-cli) — Parallel tool to analyze disk space usage of a directory and optionally delete superfluous data.
- [Perkeep](https://github.com/perkeep/perkeep) — Set of formats, protocols, and software for modeling, storing, searching, sharing, and synchronizing data, accessible via phone, browser, or FUSE filesystem.
- [duf](https://github.com/muesli/duf) — Disk usage/free utility for Linux, BSD, macOS, and Windows.
- [Dirstat-rs](https://github.com/scullionw/dirstat-rs) — Fast, cross-platform disk usage CLI similar to WinDirStat.
- [Dutree](https://github.com/nachoparker/dutree) — Tool to analyze file system usage, written in Rust.
- [Shufflecake](https://shufflecake.net/) — Tool for Linux to create multiple hidden volumes on a storage device that are difficult to detect, even under forensic inspection.
- [btdu](https://github.com/CyberShadow/btdu) — Sampling disk usage profiler for btrfs.
- [Btrfs maintenance toolbox](https://github.com/kdave/btrfsmaintenance) — Set of scripts to automate btrfs maintenance tasks such as scrub, balance, trim, and defragmentation.

## File Systems

- [FSArchiver](https://www.fsarchiver.org/) — System tool that saves the contents of a file system to a compressed archive, restorable on a different-sized partition or file system.
- [WekaFS](https://www.weka.io/resources/datasheet/wekafs-the-weka-file-system/) — Shared parallel file system delivering high performance at scale with enterprise storage features.
- [GlusterFS](https://www.gluster.org/) — Free and open source scalable network filesystem for building distributed storage solutions on commodity hardware.
- [Ceph](https://ceph.io/) — Software-defined storage solution addressing object, block, and file storage needs for data centers.
- [Hadoop Distributed File System (HDFS)](https://www.ibm.com/analytics/hadoop/hdfs) — Distributed file system for large data sets running on commodity hardware, a core component of Apache Hadoop.
- [ZFS](https://docs.oracle.com/cd/E19253-01/819-5461/zfsover-2/) — Open source file system and volume manager focused on flexibility and data integrity.
- [ZFSBootMenu](https://zfsbootmenu.org/) — Linux bootloader that uses ZFS features to support multiple boot environments, snapshot manipulation, and bootstrapping installs via `zfs recv`.
- [OpenZFS](https://openzfs.org/wiki/Main_Page) — Open source storage platform combining file system and volume manager functionality with data corruption protection, integrity checking, and self-healing repair.
- [Btrfs](https://btrfs.wiki.kernel.org/index.php/Main_Page) — Copy-on-write filesystem for Linux with snapshots, software RAID support, and self-healing checksums.
- [Composefs](https://github.com/containers/composefs) — Native Linux file system for sharing filesystem contents and ensuring they are not modified, targeting container images and ostree commits.
- [MergerFS](https://github.com/trapexit/mergerfs) — Union filesystem for managing files across multiple commodity storage devices, similar to mhddfs, unionfs, and aufs.
- [Proxmox Cluster File System (PMXCFS)](https://pve.proxmox.com/wiki/Cluster_Manager) — File system that distributes cluster configuration to all cluster nodes.
- [UnionFS](https://unionfs.filesystems.org/) — Filesystem service for Linux, FreeBSD, and NetBSD implementing a union mount that overlays multiple file systems into one.
- [OverlayFS](https://www.kernel.org/doc/html/latest/filesystems/overlayfs.html) — Union filesystem similar to AUFS but faster and simpler, often used on embedded devices.
- [Bcachefs](https://bcachefs.org/) — Filesystem for Linux emphasizing reliability and robustness, tested to 50+ TB.
- [Squashfs](https://www.kernel.org/doc/html/latest/filesystems/squashfs.html) — Compressed read-only filesystem for Linux using zlib, lz4, lzo, or xz compression.
- [SeaweedFS](https://github.com/seaweedfs/seaweedfs) — Distributed storage system for blobs, objects, files, and data lakes, with cloud tiering, replication, POSIX FUSE mount, S3 API, and erasure coding.
- [CubeFS](https://cubefs.io/) — Cloud native distributed storage platform used as storage infrastructure for online applications, databases, and machine learning jobs on Kubernetes.
- [Apple File System (APFS)](https://support.apple.com/guide/disk-utility/file-system-formats-available-in-disk-utility-dsku19ed921c/mac) — Default file system for macOS 10.13 and later, with encryption, space sharing, and snapshots.
- [NTFS (New Technology File System)](https://docs.microsoft.com/en-us/windows-server/storage/file-server/ntfs-overview) — Primary file system for recent Windows and Windows Server versions, with security descriptors, encryption, disk quotas, and Cluster Shared Volumes support.
- [exFAT (Extended File Allocation Table)](https://docs.microsoft.com/en-us/windows/win32/fileio/exfat-specification) — Successor to FAT32 in the FAT family, optimized for flash memory such as USB drives and SD cards.
