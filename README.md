# Alo OS Updates

This is the public, package-only signed APT repository for **Alo OS Sahara**.

Alo OS Sahara is a Kubuntu 26.04 LTS–based KDE Plasma desktop distribution with
an original, cohesive Sahara visual experience, a branded installer, familiar
everyday desktop applications, and a separately managed Alo OS update stream.
It preserves Ubuntu's normal package management, hardware support, and security
updates rather than replacing the base operating system architecture.

> This repository is an update service, not a source repository or ISO-download
> host. It contains approved Debian packages and signed repository metadata
> only. It never contains a private signing key, passphrase, user data, build
> machine data, or full ISO image.

## Current channel

| Setting | Value |
| --- | --- |
| Release | Alo OS Sahara |
| Suite | `sahara` |
| Architecture | `amd64` |
| Signing-key fingerprint | `16EA0BC71B3EA62D095E1828417E86A98C9341AC` |
| First verification update | `1.0.1~test1` |

The `1.0.1~test1` publication is deliberately small and safe. It is used to
confirm that a newly installed Sahara system can discover, verify, and install
a signed Alo OS update without changing the user’s desktop experience.

## For Alo OS users

Alo OS Sahara is preconfigured with this update source. No repository address,
signing key, terminal command, or manual setup is required.

When an Alo OS update is available:

1. A normal update check refreshes metadata over HTTPS.
2. APT verifies the signed `InRelease` metadata using the public key shipped
   with the operating system.
3. Discover lists compatible updates alongside normal Ubuntu and application
   updates.
4. The **Alo OS Updates** launcher opens the relevant update view.

Advanced users can use the normal APT workflow:

```bash
sudo apt update
sudo apt upgrade
```

Never add this repository manually to a non-Alo-OS system. Its packages are
built and tested for the Sahara release channel only.

## Trust and safety

- The public key is included in the official Sahara build; the private key is
  never distributed.
- APT rejects unsigned or incorrectly signed repository metadata.
- Sahara receives compatible patch releases only. A future named Alo OS release
  uses a separately tested upgrade path rather than silently changing the
  current system.
- Ubuntu security and application updates continue through their normal
  upstream sources.
- If a package needs correction, the project publishes a higher fixed version;
  it does not rewrite published signed history.

## ISO distribution

The verified Sahara 1.0.0 ISO is maintained for direct physical testing and is
not published in this repository. GitHub cannot host its 4.6 GB size as one
Release asset, and this repository intentionally remains a small, reliable
signed package archive.

Do not upload ISO images, screenshots, source build trees, private keys,
passphrases, or unrelated files here.

## Maintainers

The private source repository builds and signs this archive through the
documented release workflow. A release may publish only:

- signed `.deb` packages;
- signed APT metadata under `dists/sahara/`;
- repository indexes and the public key material required by clients.

For project architecture, build procedures, and update-maintenance guidance,
refer to the authorized private Alo OS source repository.
