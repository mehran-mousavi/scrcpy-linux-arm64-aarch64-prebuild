# scrcpy — Linux ARM64 / AArch64 builds

Unofficial pre-built binaries of **[scrcpy](https://github.com/Genymobile/scrcpy)** for **64-bit ARM Linux** (`aarch64` / `arm64`). The upstream project does not ship ready-made ARM64 Linux packages; this repository publishes builds so you can install and run scrcpy on Raspberry Pi boards, ARM Chromebooks, Asahi Linux, and other AArch64 distributions without compiling from source.

> **Current build:** [scrcpy **3.3.4**](https://github.com/Genymobile/scrcpy/releases/tag/v3.3.4)  
> **Target:** Linux `aarch64`  
> **Built on:** Debian 13 (Trixie)

These artifacts are **not** affiliated with Genymobile or the official scrcpy maintainers. For source code, documentation, and issue reporting about scrcpy itself, use the [official repository](https://github.com/Genymobile/scrcpy).

---

## Requirements

- **CPU / OS:** Linux on AArch64 (`uname -m` should show `aarch64`).
- **Android:** USB debugging enabled; device accessible via `adb` (same expectations as [upstream](https://github.com/Genymobile/scrcpy/blob/master/README.md)).
- **Runtime libraries:** Install the same kinds of dependencies you would for a local build (for example SDL2, FFmpeg, and USB/libusb-related packages as required by your distro). If something is missing, the binary will usually fail at startup with a clear library error—install the matching `-dev` or runtime package from your distribution.

---

## Download

**Always-current archive (from the default branch):**

[https://github.com/mehran-mousavi/scrcpy-linux-arm64-aarch64-prebuild/releases/latest/download/scrcpy-aarch64-linux-aarch64.tar.gz](https://github.com/mehran-mousavi/scrcpy-linux-arm64-aarch64-prebuild/releases/latest/download/scrcpy-aarch64-linux-aarch64.tar.gz)

Each push to `main` (or `master`) refreshes the rolling **continuous** release and replaces that file. Checksums are attached on the same release page as `SHA256SUMS.txt`.

1. Open **[Releases](https://github.com/mehran-mousavi/scrcpy-linux-arm64-aarch64-prebuild/releases)** for notes, checksums, and history.
2. Or use the direct link above, then extract — contents unpack under `scrcpy-aarch64/`.
3. The tree matches **scrcpy 3.3.4** when your committed binaries match that version (see release notes on each build).

---

## Quick start

After extraction, ensure `scrcpy` and related files are on your `PATH` or invoke them with an explicit path. Typical layout from an official-style install:

```bash
tar -xzf scrcpy-aarch64-linux-aarch64.tar.gz
cd scrcpy-aarch64
./scrcpy --version
```

Connect a device with `adb devices` showing it as `device`, then:

```bash
./scrcpy
```

For options (audio, recording, window size, tunneling over TCP/IP, etc.), see the [official README](https://github.com/Genymobile/scrcpy/blob/master/README.md) and `scrcpy --help`.

---

## Verifying the build

```bash
./scrcpy --version
```

You should see **3.3.4** (and commit/build metadata if your packaging includes it).

---

## Reproducibility & trust

These binaries are produced from the tagged upstream source **v3.3.4** on **Debian 13**. For maximum trust, compare checksums published on the release page with your own download, or build from source using the [official build instructions](https://github.com/Genymobile/scrcpy/blob/master/BUILD.md) on the same tag.

---

## License

scrcpy is licensed under the **Apache License 2.0**. See the [official repository](https://github.com/Genymobile/scrcpy) for the full license text and copyright notices. Pre-built binaries here are offered under the same upstream license terms; redistribution should preserve license and attribution files shipped with the release.

---

## About the maintainer

**Mehran Mousavi** — Senior full-stack developer and software architect with over a decade of experience designing and delivering scalable, user-centric platforms. Work spans robust backend architectures, polished frontends, enterprise systems, mobile and web platforms, and data-driven products, with a focus on clarity, scalability, and engineering standards that turn ideas into reliable releases.

**Profiles**

- **GitHub:** [https://github.com/mehran-mousavi](https://github.com/mehran-mousavi)  
- **LinkedIn:** [https://www.linkedin.com/in/mehran-mousavi](https://www.linkedin.com/in/mehran-mousavi)  
- **CV / portfolio:** [https://mehran-mousavi.github.io/CV/](https://mehran-mousavi.github.io/CV/)

**Contact:** [mehran.mousavi@outlook.com](mailto:mehran.mousavi@outlook.com)

---

*If this build helped you on ARM64 Linux, consider starring this repository and the [official scrcpy project](https://github.com/Genymobile/scrcpy).*
