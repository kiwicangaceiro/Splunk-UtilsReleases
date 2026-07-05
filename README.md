# Splunk-Utils - Releases

Download page for **Splunk-Utils**, a command-line tool to query Splunk from the
terminal (the `splunk-query` command). This repository only hosts the signed,
ready-to-install downloads - the source lives in a separate repository.

## Download

Get the latest installers from the [**Releases**](../../releases/latest) page:

| Platform | File | Notes |
|----------|------|-------|
| Linux (Intel/AMD) | `splunk-utils_<version>_amd64.deb` | Ubuntu / Debian |
| Linux (ARM) | `splunk-utils_<version>_arm64.deb` | Ubuntu / Debian on ARM |
| Windows (64-bit) | `splunk-utils_<version>_x64.msi` | Windows 10/11 |

Every installer **bundles its own Python runtime** - there are no prerequisites to
install. After installing, the `splunk-query` command is on your PATH.

## Install

**Linux:**
```bash
sudo apt install ./splunk-utils_<version>_amd64.deb
splunk-query --version
```

**Windows:** double-click the `.msi` (or run `msiexec /i splunk-utils_<version>_x64.msi`),
then open a **new** terminal and run `splunk-query --version`.

## Verify your download

Each release ships a `SHA256SUMS` file and a detached GPG signature
`SHA256SUMS.asc`. Verifying proves the file came from Bentosoft and was not
tampered with:

```bash
# 1. import the signing key (fingerprint is printed in the release notes)
# 2. check the signature, then the checksums
gpg --verify SHA256SUMS.asc SHA256SUMS
sha256sum --check SHA256SUMS --ignore-missing
```

If `gpg --verify` does not report a **Good signature**, do not install the file.

## Uninstall

- **Linux:** `sudo apt remove splunk-utils`
- **Windows:** Settings -> Apps -> Splunk-Utils -> Uninstall

---

Splunk-Utils is freeware, provided as-is without warranty. A personal project by
Raul Bento (Bentosoft, https://bentosoft.net). Not affiliated with Splunk Inc.
