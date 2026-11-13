# Alo OS Updates

This is the public, package-only signed APT repository for **Alo OS Sahara**.

It contains approved Debian packages and signed repository metadata only. It does
not contain the private Alo OS source repository, private signing key,
passphrase, user data, or build machine data.

## Current channel

- Suite: `sahara`
- Architecture: `amd64`
- Signing-key fingerprint: `16EA0BC71B3EA62D095E1828417E86A98C9341AC`
- Test publication: `1.0.1~test1`

Alo OS systems verify `InRelease` using the public key included with the OS
before APT or Discover accepts any package. Do not use this repository as a
general-purpose package mirror.
