# Firekeeper dashboard server: binaries

This repository holds compiled binaries of the Firekeeper dashboard server
(`firekeeper-server`), and nothing else. There is no source code here. The
server's source is private; it is not open source.

The binaries are part of a commercial product. The license terms will be
published in this repository. They are not final yet, so nothing here is a
license grant.

<!-- Maintainer: delete the next sentence when the first release is published. -->
**No release exists yet.**

## Release layout

Each release has, for every platform:

- `firekeeper-server_<version>_<os>_<arch>.tar.gz`, where `<version>` is the
  tag without the leading `v`, `<os>` is `darwin` or `linux`, and `<arch>` is
  `amd64` or `arm64`. The archive contains the `firekeeper-server` binary (and
  possibly a `LICENSE` file).
- `checksums.txt`, one SHA-256 line per archive in `sha256sum` format.

## Verify a download

Put the archive and `checksums.txt` in one directory, then run one of:

```sh
sha256sum -c checksums.txt --ignore-missing          # Linux
shasum -a 256 -c checksums.txt --ignore-missing      # macOS
```

The line for your archive must say `OK`.

## Install

Not available yet:

- The open client can offer to install the server: `firekeeper serve` asks
  first and downloads nothing unless you answer yes. This is switched off until
  the maintainers turn it on.
- Homebrew: `brew install DanBradbury/tap/firekeeper-server`. The formula does
  not exist yet.

Until then, download an archive from the Releases page once one exists, verify
it as above, and put `firekeeper-server` on your `PATH`.

## More

- The open client: [DanBradbury/firekeeper](https://github.com/DanBradbury/firekeeper),
  see the README section
  [The dashboard server](https://github.com/DanBradbury/firekeeper#the-dashboard-server).
- Problems and questions: open an issue on the
  [client repository](https://github.com/DanBradbury/firekeeper/issues). This
  repository has no code and does not take issues.
