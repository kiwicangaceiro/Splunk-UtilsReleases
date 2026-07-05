# Security Policy

Splunk-Utils is freeware maintained by Raul Bento (Bentosoft, https://bentosoft.net).

## Reporting a vulnerability

Please report security issues **privately** - do not open a public issue.

- Preferred: click **"Report a vulnerability"** on this repository's **Security** tab
  (GitHub private advisories).
- Or email: r.bento.brazil@gmail.com

Include the affected version and steps to reproduce. You will get an acknowledgement
as soon as possible.

## Supported versions

Only the latest release receives fixes.

## Verifying your download

Every release ships a GPG-signed `SHA256SUMS`. Verify it before installing:

```bash
gpg --verify SHA256SUMS.asc SHA256SUMS
sha256sum --check SHA256SUMS --ignore-missing
```

If the signature is not reported as **Good**, do not install the file.
