# Calf LV2 ARM64 packs for Machinista

Upstream: https://github.com/calf-studio-gear/calf

Pinned upstream release: Calf 0.90.3; Debian calf 0.90.3-4.


These are independent community ports/packaging, not official upstream releases.
Install the ARM64 ZIP through Machinista WebUI > LV2 Plugins > Upload & check.
Target: 64-bit Raspberry Pi OS / Debian Trixie on Pi 4/5. Other systems need a rebuild.
Controller layouts and parameter banks are provided by the separate Machinista host.
No Roland ROMs or VirtualJV are included.

Binary downloads and complete corresponding sources are attached to Releases.
Original copyright notices and component licenses remain in force. No Machinista
resale restriction is applied to these third-party ports.

The upstream source includes LGPL-2.1 and GPL-covered components. Per-file notices
and COPYING/COPYING.GPL apply; dependencies retain their own licenses.

- Essentials: Filter, Equalizer5Band, Compressor, Reverb, VintageDelay,
  MultiChorus, Saturator, Crusher. DSP from the Debian binary; local library paths
  and headless metadata adjusted by tools/build_calf_effects.py.
- Color: TapeSimulator, BassEnhancer, Vinyl, rebuilt from source. The build recipe
  restricts the exported modules, locates Vinyl noise assets relative to the bundle
  and configures one FluidSynth render core. See tools/build_calf_color.py.

Reproduction inputs and dependency sources are supplied as release assets.
Run `python3 tools/build_calf_effects.py --help` or
`python3 tools/build_calf_color.py --help` for the required extracted source,
Debian package and runtime-library directories. Nothing is installed by those
scripts. Build in a Linux ARM64 environment with g++, Python 3, development
headers, binutils and patchelf (Essentials).

Upstream 0.90.3 COPYING and COPYING.GPL are preserved unmodified. Retain the
Debian copyright files and complete dependency sources when redistributing
packaged runtime libraries. No host resale restriction applies to this repository.
