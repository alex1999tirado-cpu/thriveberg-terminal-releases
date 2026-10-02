# THRIVEBERG Terminal Releases

Official Windows beta installers for THRIVEBERG Terminal.

## Current release

[Download THRIVEBERG Terminal Beta 018](https://github.com/alex1999tirado-cpu/thriveberg-terminal-releases/releases/latest)

THRIVEBERG is a desktop financial research workstation with market data,
company fundamentals, filings, portfolio analytics, alerts, charts and a
Bloomberg-inspired command workflow.

## Install

1. Open the latest release.
2. Download `THRIVEBERG-Terminal-BETA-018-Setup.exe`.
3. Run the installer and keep **Create a desktop shortcut** selected if desired.

The application installs per user under `%LOCALAPPDATA%\Programs` and can be
upgraded in place. Existing encrypted settings and local user data are retained.

## Release integrity

Each release publishes four files:

- the Windows setup executable;
- its human-readable `.sha256` checksum;
- an Ed25519-signed update manifest;
- the detached manifest signature.

The in-app `UPD` command accepts online updates only after verifying the
Ed25519 signature, signed filename, byte size and SHA-256. Interrupted downloads
can resume, and cached installers are revalidated before launch.

The installer is not yet Authenticode signed, so Microsoft SmartScreen may show
an unknown-publisher warning on the initial manual installation.

## Privacy and credentials

Private API keys are not included in these releases. Optional credentials added
by a user are stored for that Windows account in a versioned DPAPI-encrypted
settings file. The `DIAG` support export excludes credential values, portfolio
values and database contents.

THRIVEBERG Terminal is beta research software, not investment advice or a
licensed real-time market-data service.
