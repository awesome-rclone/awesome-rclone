# Awesome Rclone [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> Command-line program for syncing files and directories to and from cloud storage providers.

## Contents
- [Official Resources](#official-resources)
- [Clients \& GUIs](#clients--guis)
	- [Desktop](#desktop)
	- [Web](#web)
	- [Mobile](#mobile)
	- [Terminal](#terminal)
- [Sync and Backup Tools](#sync-and-backup-tools)
	- [Two-Way Sync](#two-way-sync)
	- [Backup Utilities](#backup-utilities)
	- [Backup Software with Rclone Support](#backup-software-with-rclone-support)
- [API Libraries and SDKs](#api-libraries-and-sdks)
	- [JavaScript / TypeScript](#javascript--typescript)
	- [Python](#python)
	- [PHP](#php)
	- [Rust](#rust)
	- [Go](#go)
- [Automation and Scripts](#automation-and-scripts)
- [Cloud and System Integrations](#cloud-and-system-integrations)
	- [Kubernetes](#kubernetes)
	- [Home Automation](#home-automation)
	- [CI/CD](#cicd)
	- [NFS](#nfs)
- [Docker Images](#docker-images)
- [Forks and Alternate Builds](#forks-and-alternate-builds)
- [Utilities and Miscellaneous](#utilities-and-miscellaneous)

---

## Official Resources
- [Rclone](https://github.com/rclone/rclone) - The core command-line tool for syncing files to 70+ cloud storage providers.
- [Docs](https://rclone.org) - The official **`rclone`** docs.
- [Forum](https://forum.rclone.org) - The official **`rclone`** forum.

## Clients & GUIs

### Desktop

- [Rclone UI](https://github.com/rclone-ui/rclone-ui) - Cross-platform desktop GUI built with Rust for managing remotes and tasks.
- [RcloneView](https://rcloneview.com/) - Commercial GUI for Windows/macOS with folder comparison and multi-window remote control. Flutter based and developed in Korea.
- [REM](https://github.com/liriliri/rem) - Kawaii rclone client. Can be seen as an open source version of RcloneView.
- [S3Drive](https://s3drive.app/) - Commercial GUI that includes a proprietary cloud storage offering. Supports encryption.
- [Rclone Manager](https://github.com/Zarestia-Dev/rclone-manager) - Hobby cross-platform GUI built with Angular.
- [Rclone Shuttle](https://github.com/pieterdd/RcloneShuttle) - GTK4-based graphical uploader for rclone. Simple drag-and-drop file transfers written in Rust.
- [Rclone Navigator](https://github.com/Communist02/RcloneNavigator) - Desktop GUI for managing files in cloud storage. Supports Linux and Windows with features for browsing, uploading, downloading, mounting, and serving remotes.
- [Ultra Explorer](https://ultra-explorer.app) - Rclone GUI for macOS (Apple Silicon), Windows and Linux, also available as a self-hosted Docker web app. The free version includes a dual-pane explorer and background transfers; an optional Pro upgrade adds search, space analysis and saved synchronizations.

### Web

- [Motuz](https://github.com/FredHutch/motuz) - Web interface designed for large-scale, multi-user data transfers (e.g., scientists moving TBs of data). Provides web UI and REST API on top of rclone.
- [MultCloud](https://www.multcloud.com/) - Commercial web-based cloud management platform. Transfer, sync, and backup files between 30+ cloud services. Supports cloud-to-cloud transfers without downloading. Available on Android and iOS.

### Mobile

- [RCX (Rclone for Android)](https://github.com/x0b/rcx) - Full-featured Android file manager powered by rclone. Browse, upload, download, stream, and manage files on cloud remotes. Available on [F-Droid](https://f-droid.org/en/packages/io.github.x0b.rcx/) and Google Play.
- [Round Sync](https://github.com/newhinton/Round-Sync) - Fork of RCX with Material 3 Design, task management, and enhanced features. Available on [F-Droid](https://f-droid.org/packages/de.felixnuesse.extract/) and [IzzyOnDroid](https://apt.izzysoft.de/fdroid/index/apk/de.felixnuesse.extract). [Website](https://roundsync.com/)

### Terminal

- [ratclone](https://github.com/SyscallBrain/ratclone) - Keyboard-driven terminal UI for rclone. Browses remotes and the local disk in one or two panes, copies and moves between them as rclone jobs that keep running after the app closes, and shows the rclone command behind each transfer.

## Sync and Backup Tools

### Two-Way Sync

- [syncrclone](https://github.com/Jwink3101/syncrclone) - Python-based bi-directional sync tool built specifically for rclone. Supports conflict resolution, move/rename tracking, and backups of changed files.
- [UpBack](https://github.com/DavideRossi/upback) - Two-way sync utility assuming star topology (one cloud remote syncing with multiple clients).
- [rsinc](https://github.com/ConorWilliams/rsinc) - Tiny hackable two-way cloud sync client for Linux. Tracks file moves using hashes and supports parallel transfers.

### Backup Utilities

- [rclone_jobber](https://github.com/wolfv6/rclone_jobber) - Bash script for backup rotation with logging, archival of old files, retries, and desktop notifications on errors.
- [Rclone BiSync Manager](https://github.com/Gunther-Schulz/rclone-bisync-manager) - GUI + daemon for continuous two-way sync using rclone's bisync. Provides system tray monitor with real-time status.
- [dfb (Dated File Backup)](https://github.com/Jwink3101/dfb) - Wrapper implementing reverse-incremental backups with rclone. Preserves older versions by appending dates to filenames.
- [RCloneBackup](https://github.com/polar147/RCloneBackup) - Cross-platform script for reverse incremental backups with Windows VSS support and email reports.
- [PyClone](https://github.com/PyCloneOrg/PyClone) - Python automation engine for rclone backup scenarios. Define backup strategy in config file with Telegram notifications.

### Backup Software with Rclone Support

- [Kopia](https://github.com/kopia/kopia) - Open-source backup tool for encrypted, deduplicated backups. Supports rclone as transport for additional cloud providers.
- [restic](https://github.com/restic/restic) - Secure deduplicating backup program. Can use rclone as backend to access many cloud storage services.
- [HashBackup](http://www.hashbackup.com/) - Efficient multi-threaded command-line backup for Linux/Unix. Can invoke rclone as transport for unsupported storage systems. **`Commercial`**
- [Rcloner](https://github.com/vifreefly/rcloner) - Ruby gem wrapping Duplicity and rclone for easy app backups with encryption.

## API Libraries and SDKs

### JavaScript / TypeScript

- [rclone](https://github.com/FWeinb/rclone-js) - JavaScript implementation of rclone cryptography for the browser (filename encryption).
- [rclone-sdk](https://github.com/rclone-ui/rclone-sdk?tab=readme-ov-file#-javascript--typescript) - Typed SDK for browser and Node. Integrates with vanilla fetch, React Query, and SWR.
- [@fyears/rclone-crypt](https://www.npmjs.com/package/@fyears/rclone-crypt) - Rclone's Crypt encryption algorithm implemented in TypeScript. Enables encrypting/decrypting compatible with rclone's crypt remote.

### Python

- [rclone-api (PyPI)](https://pypi.org/project/rclone-api/) - High-level Python API focusing on performance. Auto-downloads rclone binary if not in PATH. Includes HTTP server for ranged file access.
- [PyClone (ltgiv)](https://gitlab.com/ltgiv/pyclone) - Python package wrapping rclone with Pythonic interface. Run operations in threads and get results as Python data structures.
- [python-rclone](https://pypi.org/project/python-rclone/) - Simple Python wrapper for invoking rclone commands.

### PHP

- [Flyclone](https://github.com/verseles/flyclone) - Object-oriented PHP library wrapping rclone operations. Supports many backends with progress tracking and transfer stats.

### Rust

- [rclone-sdk](https://github.com/rclone-ui/rclone-sdk) - Rust crate providing full client to rclone's RC REST API. Based on the [OpenAPI spec](https://github.com/rclone-ui/rclone-openapi). Used internally by Rclone UI.

### Go

- [Librclone](https://rclone.org/rc/#using-librclone) - Official C library interface for rclone. Enables embedding rclone in other programs (C, Python via ctypes, etc.). Part of rclone core.

## Automation and Scripts

- [rclone4pi](https://github.com/pageauc/rclone4pi) - Easy installer and cron setup for rclone on Raspberry Pi with sample sync scripts.
- [rhttpserve](https://github.com/brandur/rhttpserve) - Lightweight HTTP server that serves files from any rclone remote with expiring signed URLs for secure sharing.

## Cloud and System Integrations

### Kubernetes

- [CSI Driver (Veloxpack)](https://github.com/veloxpack/csi-driver-rclone) - Kubernetes CSI driver built on rclone Go library. Mounts 50+ cloud providers in pods with dynamic PV provisioning and secrets management.
- [CSI Driver (Wunderio)](https://github.com/wunderio/csi-rclone) - Kubernetes CSI storage driver using rclone mount.

### Home Automation

- [Home Assistant Rclone Backup](https://github.com/jcwillox/hassio-rclone-backup) - Home Assistant add-on that uses rclone to automatically sync backups to remote cloud storage.

### CI/CD

- [GitHub Action for rclone](https://github.com/wei/rclone) - GitHub Action that installs and runs rclone within workflows for syncing artifacts to cloud storage.

### NFS

- [rclone-nfs-server](https://gitlab.com/encircle360/rclone-nfs-server) - Dockerized NFS server exposing any rclone remote as an NFS share. Useful in Kubernetes for providing cached mount points.

## Docker Images

- [rclone/rclone (official)](https://hub.docker.com/r/rclone/rclone) - Official Alpine-based Docker image maintained by rclone developers. Tracks latest stable and beta releases.
- [pfidr/rclone](https://hub.docker.com/r/pfidr/rclone/) - Community image for scheduled rclone sync jobs via cron with Healthchecks.io integration.
- [mumiehub/rclone-mount](https://hub.docker.com/r/mumiehub/rclone-mount) - Container running rclone mount to expose cloud storage to host or other containers.
- [openbridge/ob_bulkstash](https://github.com/openbridge/ob_bulkstash) - Docker image for bulk transfers with Alpine + crond + Monit for reliability.
- [tynor88/rclone](https://hub.docker.com/r/tynor88/rclone) - Minimal Docker image for one-off rclone copy/sync operations.
- [rayou/rclone](https://hub.docker.com/r/rayou/rclone) - Ultra-minimal (~20MB) rclone image for custom usage.

## Forks and Alternate Builds

- [Fclone](https://github.com/NyaMisty/fclone) - Continuously updated fork providing pre-built binaries and speedy updates.

## Utilities and Miscellaneous

- [rclone-openapi](https://github.com/rclone-ui/rclone-openapi) - OpenAPI 3.0 specification for rclone's RC API. Useful for generating clients and documentation.
- [rclone-config-builder](https://github.com/Lesmiscore/rclone-config-builder) - Library to build rclone config files in JSON/YAML.
- [@x-cmd-pkg/rclone](https://www.npmjs.com/package/@x-cmd-pkg/rclone) - Rclone binaries repackaged as npm module for easy installation in Node projects.

---

## Contributing

Contributions are welcome! Please read the [contribution guidelines](contributing.md) first.
