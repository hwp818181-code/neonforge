# Neonforge Linux

Gaming-first live distro. Debian 13 base, KDE Plasma 6, zero-terminal design.
Builds an amd64 and an arm64 hybrid ISO, unattended, on GitHub Actions.

## Build
1. Actions > "Build Neonforge ISOs" > Run workflow.
2. Wait ~40-70 min. Download `neonforge-amd64` and `neonforge-arm64` artifacts.
3. Verify with the SHA256SUMS file.
4. If the ISO came as `.part` files, rejoin with 7-Zip.

## Write / boot
- x86 PC: flash with balenaEtcher. BIOS and UEFI both boot. Disable Secure Boot.
- arm64 VM: UEFI firmware, 4+ cores, 8 GB RAM, virtio-gpu with 3D acceleration.
- Live user is `gamer`, password `live`, sudo passwordless.

## Notes
- Steam does not exist for ARM. arm64 uses box64/box86 plus RetroArch.
- Add a partition labelled `persistence` to the USB stick to keep changes.
- Install to disk with the Calamares icon on the desktop.

MIT licensed.