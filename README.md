# Awesome Rclone [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of tools, GUIs, integrations, libraries, and resources for [rclone](https://rclone.org/#docs) - the "Swiss army knife of cloud storage".

[Rclone](https://github.com/rclone/rclone?tab=readme-ov-file#rclone) is a command-line program to sync files and directories to and from dozens of cloud storage providers. This list collects the ecosystem of projects built around rclone.

## Contents
- [Official Resources](#official-resources)
- [Clients \& GUIs](#clients--guis)
	- [Desktop](#desktop)
	- [Web](#web)
	- [Mobile](#mobile)
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
- [Rclone](https://github.com/rclone/rclone) - The core command-line tool for syncing files to 70+ cloud storage providers. Created by @ncw and loved by everyone. ![GitHub stars](https://img.shields.io/github/stars/rclone/rclone)
- [Docs](https://rclone.org) - The official **`rclone`** docs.
- [Forum](https://forum.rclone.org) - The official **`rclone`** forum.

## Clients & GUIs

### Desktop

- [Rclone UI](https://github.com/rclone-ui/rclone-ui) - Modern, battle-tested, cross-platform desktop GUI built with Rust. Most recommended & actively maintained solution for both newbies and veterans. ![GitHub stars](https://img.shields.io/github/stars/rclone-ui/rclone-ui)
- [RcloneView](https://rcloneview.com/) - Commercial GUI for Windows/macOS with folder comparison and multi-window remote control. Flutter based and developed in Korea.
- [REM](https://github.com/liriliri/rem) - Kawaii rclone client. Can be seen as an open source version of RcloneView. ![GitHub stars](https://img.shields.io/github/stars/liriliri/rem)
- [S3Drive](https://s3drive.app/) - Commercial GUI that includes a proprietary cloud storage offering. Supports encryption.
- [Rclone Manager](https://github.com/Zarestia-Dev/rclone-manager) - Hobby cross-platform GUI built with Angular. ![GitHub stars](https://img.shields.io/github/stars/Zarestia-Dev/rclone-manager)
- [Rclone Shuttle](https://github.com/pieterdd/RcloneShuttle) - GTK4-based graphical uploader for rclone. Simple drag-and-drop file transfers written in Rust. ![GitHub stars](https://img.shields.io/github/stars/pieterdd/RcloneShuttle)
- [Rclone Navigator](https://github.com/Communist02/RcloneNavigator) - Desktop GUI for managing files in cloud storage. Supports Linux and Windows with features for browsing, uploading, downloading, mounting, and serving remotes. ![GitHub stars](https://img.shields.io/github/stars/Communist02/RcloneNavigator)
- [Rclone Browser](https://github.com/kapitainsky/RcloneBrowser) - Cross-platform Qt GUI for browsing, transferring, mounting, and streaming files. Fork of original by mmozeiko. **`Inactive since 2020`** ![GitHub stars](https://img.shields.io/github/stars/kapitainsky/RcloneBrowser)
- [RcloneTray](https://github.com/dimitrov-adrian/RcloneTray) - Minimal Electron-based system tray application for mounting and managing remotes. **`Inactive since 2018`** ![GitHub stars](https://img.shields.io/github/stars/dimitrov-adrian/RcloneTray)
- [RcloneNg](https://github.com/ElonH/RcloneNg) - Angular-based web app GUI with two-pane file manager interface. Packaged for OpenWrt. **`Inactive since 2021`** ![GitHub stars](https://img.shields.io/github/stars/ElonH/RcloneNg)

### Web

- [Motuz](https://github.com/FredHutch/motuz) - Web interface designed for large-scale, multi-user data transfers (e.g., scientists moving TBs of data). Provides web UI and REST API on top of rclone. ![GitHub stars](https://img.shields.io/github/stars/FredHutch/motuz)
- [WebUI React](https://github.com/rclone/rclone-webui-react) - Official web-based GUI bundled with rclone (`rclone rcd --rc-web-gui`). ![GitHub stars](https://img.shields.io/github/stars/rclone/rclone-webui-react)
- [MultCloud](https://www.multcloud.com/) - Commercial web-based cloud management platform. Transfer, sync, and backup files between 30+ cloud services. Supports cloud-to-cloud transfers without downloading. Available on Android and iOS.


### Mobile

- [RCX (Rclone for Android)](https://github.com/x0b/rcx) - Full-featured Android file manager powered by rclone. Browse, upload, download, stream, and manage files on cloud remotes. Available on [F-Droid](https://f-droid.org/en/packages/io.github.x0b.rcx/) and Google Play. ![GitHub stars](https://img.shields.io/github/stars/x0b/rcx)
- [Round Sync](https://github.com/newhinton/Round-Sync) - Fork of RCX with Material 3 Design, task management, and enhanced features. Available on [F-Droid](https://f-droid.org/packages/de.felixnuesse.extract/) and [IzzyOnDroid](https://apt.izzysoft.de/fdroid/index/apk/de.felixnuesse.extract). [Website](https://roundsync.com/) ![GitHub stars](https://img.shields.io/github/stars/newhinton/Round-Sync)
- [Rclone Explorer](https://github.com/patrykcoding/rcloneExplorer) - Original Android GUI for rclone. **`Inactive since 2018, superseded by RCX`** ![GitHub stars](https://img.shields.io/github/stars/patrykcoding/rcloneExplorer)
- [Unified Cloud Storage](https://play.google.com/store/apps/details?id=com.codestation.unifiedcloudstorage) - Legacy Android app for managing multiple cloud storage accounts via rclone. **`Inactive since 2017`**


## Sync and Backup Tools

### Two-Way Sync

- [syncrclone](https://github.com/Jwink3101/syncrclone) - Python-based bi-directional sync tool built specifically for rclone. Supports conflict resolution, move/rename tracking, and backups of changed files. ![GitHub stars](https://img.shields.io/github/stars/Jwink3101/syncrclone)
- [rclonesync V2](https://github.com/cjnaz/rclonesync-V2) - Python script for two-way sync with safety checks and max deletion limits. **`Superseded by rclone's built-in bisync`** ![GitHub stars](https://img.shields.io/github/stars/cjnaz/rclonesync-V2)
- [PyFiSync](https://github.com/Jwink3101/PyFiSync) - Python-based 2-way sync utility that can use rclone for transfers. Tracks moves/deletions and backs up on conflict. **`Predecessor to syncrclone`** ![GitHub stars](https://img.shields.io/github/stars/Jwink3101/PyFiSync)
- [UpBack](https://github.com/DavideRossi/upback) - Two-way sync utility assuming star topology (one cloud remote syncing with multiple clients). ![GitHub stars](https://img.shields.io/github/stars/DavideRossi/upback)
- [rsinc](https://github.com/ConorWilliams/rsinc) - Tiny hackable two-way cloud sync client for Linux. Tracks file moves using hashes and supports parallel transfers. ![GitHub stars](https://img.shields.io/github/stars/ConorWilliams/rsinc)

### Backup Utilities

- [rclone_jobber](https://github.com/wolfv6/rclone_jobber) - Bash script for backup rotation with logging, archival of old files, retries, and desktop notifications on errors. ![GitHub stars](https://img.shields.io/github/stars/wolfv6/rclone_jobber)
- [Rclone BiSync Manager](https://github.com/Gunther-Schulz/rclone-bisync-manager) - GUI + daemon for continuous two-way sync using rclone's bisync. Provides system tray monitor with real-time status. ![GitHub stars](https://img.shields.io/github/stars/Gunther-Schulz/rclone-bisync-manager)
- [dfb (Dated File Backup)](https://github.com/Jwink3101/dfb) - Wrapper implementing reverse-incremental backups with rclone. Preserves older versions by appending dates to filenames. ![GitHub stars](https://img.shields.io/github/stars/Jwink3101/dfb)
- [RCloneBackup](https://github.com/polar147/RCloneBackup) - Cross-platform script for reverse incremental backups with Windows VSS support and email reports. ![GitHub stars](https://img.shields.io/github/stars/polar147/RCloneBackup)
- [PyClone](https://github.com/PyCloneOrg/PyClone) - Python automation engine for rclone backup scenarios. Define backup strategy in config file with Telegram notifications. ![GitHub stars](https://img.shields.io/github/stars/PyCloneOrg/PyClone)

### Backup Software with Rclone Support

- [Kopia](https://github.com/kopia/kopia) - Open-source backup tool for encrypted, deduplicated backups. Supports rclone as transport for additional cloud providers. ![GitHub stars](https://img.shields.io/github/stars/kopia/kopia)
- [restic](https://github.com/restic/restic) - Secure deduplicating backup program. Can use rclone as backend to access many cloud storage services. ![GitHub stars](https://img.shields.io/github/stars/restic/restic)
- [HashBackup](http://www.hashbackup.com/) - Efficient multi-threaded command-line backup for Linux/Unix. Can invoke rclone as transport for unsupported storage systems. **`Commercial`**
- [Duplicity Backend](https://github.com/GilGalaad/duplicity-rclone) - Plugin allowing Duplicity backup software to use rclone as a storage backend. **`Archived`** ![GitHub stars](https://img.shields.io/github/stars/GilGalaad/duplicity-rclone)
- [Rcloner](https://github.com/vifreefly/rcloner) - Ruby gem wrapping Duplicity and rclone for easy app backups with encryption. ![GitHub stars](https://img.shields.io/github/stars/vifreefly/rcloner)
- [Doomsday Machine](https://github.com/johnjones4/Doomsday-Machine) - Backup tool using rclone to archive data from various cloud services (IMAP, Drive, etc.) into Docker containers. **`Archived`** ![GitHub stars](https://img.shields.io/github/stars/johnjones4/Doomsday-Machine)

## API Libraries and SDKs

### JavaScript / TypeScript

- [rclone](https://github.com/FWeinb/rclone-js) - JavaScript implementation of rclone cryptography for the browser (filename encryption). ![GitHub stars](https://img.shields.io/github/stars/FWeinb/rclone-js)
- [rclone-sdk](https://github.com/rclone-ui/rclone-sdk?tab=readme-ov-file#-javascript--typescript) - Typed SDK for browser and Node. Integrates with vanilla fetch, React Query, and SWR. ![GitHub stars](https://img.shields.io/github/stars/rclone-ui/rclone-sdk) 
- [rclone-api](https://github.com/rclone/rclone-js-api) - JavaScript client for rclone's RC HTTP API. Promise-based functions for all RC endpoints. **`Inactive, superseded by rclone-sdk`** ![GitHub stars](https://img.shields.io/github/stars/rclone/rclone-js-api) 
- [rclone.js](https://github.com/sntran/rclone.js) - Node.js wrapper exposing rclone functions via JavaScript. Downloads rclone binary on install and provides Promise-based API. **`Inactive, superseded by rclone-sdk`** ![GitHub stars](https://img.shields.io/github/stars/sntran/rclone.js) 
- [@fyears/rclone-crypt](https://www.npmjs.com/package/@fyears/rclone-crypt) - Rclone's Crypt encryption algorithm implemented in TypeScript. Enables encrypting/decrypting compatible with rclone's crypt remote.


### Python

- [rclone-api (PyPI)](https://pypi.org/project/rclone-api/) - High-level Python API focusing on performance. Auto-downloads rclone binary if not in PATH. Includes HTTP server for ranged file access.
- [PyClone (ltgiv)](https://gitlab.com/ltgiv/pyclone) - Python package wrapping rclone with Pythonic interface. Run operations in threads and get results as Python data structures.
- [python-rclone](https://pypi.org/project/python-rclone/) - Simple Python wrapper for invoking rclone commands.

### PHP

- [Flyclone](https://github.com/verseles/flyclone) - Object-oriented PHP library wrapping rclone operations. Supports many backends with progress tracking and transfer stats. ![GitHub stars](https://img.shields.io/github/stars/verseles/flyclone)

### Rust

- [rclone-sdk](https://github.com/rclone-ui/rclone-sdk) - Rust crate providing full client to rclone's RC REST API. Based on the [OpenAPI spec](https://github.com/rclone-ui/rclone-openapi). Used internally by Rclone UI. ![GitHub stars](https://img.shields.io/github/stars/rclone-ui/rclone-sdk)

### Go

- [Librclone](https://rclone.org/rc/#using-librclone) - Official C library interface for rclone. Enables embedding rclone in other programs (C, Python via ctypes, etc.). Part of rclone core.

## Automation and Scripts

- [AutoRclone](https://github.com/xyou365/AutoRclone) - Scripts to automate rclone Google Drive operations using multiple service accounts to bypass quotas. ![GitHub stars](https://img.shields.io/github/stars/xyou365/AutoRclone)
- [rclone4pi](https://github.com/pageauc/rclone4pi) - Easy installer and cron setup for rclone on Raspberry Pi with sample sync scripts. ![GitHub stars](https://img.shields.io/github/stars/pageauc/rclone4pi)
- [rhttpserve](https://github.com/brandur/rhttpserve) - Lightweight HTTP server that serves files from any rclone remote with expiring signed URLs for secure sharing. ![GitHub stars](https://img.shields.io/github/stars/brandur/rhttpserve)

## Cloud and System Integrations

### Kubernetes

- [CSI Driver (Veloxpack)](https://github.com/veloxpack/csi-driver-rclone) - Kubernetes CSI driver built on rclone Go library. Mounts 50+ cloud providers in pods with dynamic PV provisioning and secrets management. ![GitHub stars](https://img.shields.io/github/stars/veloxpack/csi-driver-rclone)
- [CSI Driver (Wunderio)](https://github.com/wunderio/csi-rclone) - Original Kubernetes CSI storage driver using rclone mount. **`Archived`** ![GitHub stars](https://img.shields.io/github/stars/wunderio/csi-rclone)

### Home Automation

- [Home Assistant Rclone Backup](https://github.com/jcwillox/hassio-rclone-backup) - Home Assistant add-on that uses rclone to automatically sync backups to remote cloud storage. ![GitHub stars](https://img.shields.io/github/stars/jcwillox/hassio-rclone-backup)

### CI/CD

- [GitHub Action for rclone](https://github.com/wei/rclone) - GitHub Action that installs and runs rclone within workflows for syncing artifacts to cloud storage. ![GitHub stars](https://img.shields.io/github/stars/wei/rclone)

### NFS

- [rclone-nfs-server](https://gitlab.com/encircle360/rclone-nfs-server) - Dockerized NFS server exposing any rclone remote as an NFS share. Useful in Kubernetes for providing cached mount points.

## Docker Images

- [rclone/rclone (official)](https://hub.docker.com/r/rclone/rclone) - Official Alpine-based Docker image maintained by rclone developers. Tracks latest stable and beta releases.
- [pfidr/rclone](https://hub.docker.com/r/pfidr/rclone/) - Community image for scheduled rclone sync jobs via cron with Healthchecks.io integration.
- [mumiehub/rclone-mount](https://hub.docker.com/r/mumiehub/rclone-mount) - Container running rclone mount to expose cloud storage to host or other containers.
- [openbridge/ob_bulkstash](https://github.com/openbridge/ob_bulkstash) - Docker image for bulk transfers with Alpine + crond + Monit for reliability. ![GitHub stars](https://img.shields.io/github/stars/openbridge/ob_bulkstash)
- [tynor88/rclone](https://hub.docker.com/r/tynor88/rclone) - Minimal Docker image for one-off rclone copy/sync operations.
- [rayou/rclone](https://hub.docker.com/r/rayou/rclone) - Ultra-minimal (~20MB) rclone image for custom usage.

## Forks and Alternate Builds

- [gclone (dogbutcat)](https://github.com/dogbutcat/gclone) - Actively maintained fork with Google Drive Service Account rotation to bypass API quotas. ![GitHub stars](https://img.shields.io/github/stars/dogbutcat/gclone)
- [gclone (l3v11)](https://github.com/l3v11/gclone) - Another gclone fork with auto SA rotation. **`Archived`** ![GitHub stars](https://img.shields.io/github/stars/l3v11/gclone)
- [gclone (donwa)](https://github.com/donwa/gclone) - Original gclone mod optimized for Google Drive SA usage. Based on rclone v1.51. **`Inactive`** ![GitHub stars](https://img.shields.io/github/stars/donwa/gclone)
- [Fclone](https://github.com/NyaMisty/fclone) - Continuously updated fork providing pre-built binaries and speedy updates. ![GitHub stars](https://img.shields.io/github/stars/NyaMisty/fclone)
- [Rclone_RD](https://github.com/itsToggle/rclone_RD) - Fork integrating Real-Debrid API as a backend. Mount and stream cached torrents from Real-Debrid. ![GitHub stars](https://img.shields.io/github/stars/itsToggle/rclone_RD)

## Utilities and Miscellaneous

- [rclone-openapi](https://github.com/rclone-ui/rclone-openapi) - OpenAPI 3.0 specification for rclone's RC API. Useful for generating clients and documentation. ![GitHub stars](https://img.shields.io/github/stars/rclone-ui/rclone-openapi)
- [rclone-config-builder](https://github.com/Lesmiscore/rclone-config-builder) - Library to build rclone config files in JSON/YAML. ![GitHub stars](https://img.shields.io/github/stars/Lesmiscore/rclone-config-builder)
- [@x-cmd-pkg/rclone](https://www.npmjs.com/package/@x-cmd-pkg/rclone) - Rclone binaries repackaged as npm module for easy installation in Node projects.
- [vim-netranger](https://github.com/ipod825/vim-netranger) - Vim/Neovim plugin providing ranger-like file explorer with rclone cloud storage support. **`Deprecated`** ![GitHub stars](https://img.shields.io/github/stars/ipod825/vim-netranger)
- [Sprinkle](https://mmontuori.github.io/Sprinkle/) - Volume clustering utility presenting multiple rclone cloud drives as one virtual volume for backup/recovery. **`Inactive`**
- [Polo File Manager](https://teejee2008.github.io/polo/) - Advanced Linux file manager with built-in rclone integration for cloud storage. **`Inactive`**

---

## Contributing

Contributions are welcome!

Please read the [contribution guidelines](contributing.md) before submitting a pull request:
- Ensure the project is actively related to rclone
- Include a brief description and link to the project
- Check that the project isn't already listed
- Add new entries in alphabetical order within their section
