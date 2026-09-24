<div align="center">

# Floorp Portable

Ready-to-run Floorp Windows x64 portable build. Data stays in the folder; nothing is written to the registry.

[![Release][badge-release]][link-release]
[![Downloads][badge-downloads]][link-release]
[![Build][badge-build]][link-actions]
[![License][badge-license]][link-license]

**[⬇ Download latest][link-release]** · **[📖 User guide][link-usage]**

[简体中文](README.md) | **English**

</div>

> Build system: [Gecko-Portable](https://github.com/Piracola/Gecko-Portable) — this repository is only one of its build configs.

## Navigation

- [Latest release](https://github.com/Piracola/Floorp_portable/releases/latest): grab `Floorp_<version>.7z`
- [User guide](./docs/usage.md): layout, config, verification
- [Development](./docs/development.md): CI and local builds
- [Gecko-Portable](https://github.com/Piracola/Gecko-Portable): shared builder
- [Firefox-Portable](https://github.com/Piracola/Firefox-Portable) · [Zen-Portable](https://github.com/Piracola/Zen-Portable)

## About

[Floorp](https://floorp.app/) is a Firefox-based browser from a Japanese team, known for deep UI customization and vertical tabs. This project takes the official installer as-is and makes it portable with [libportable](https://github.com/adonais/libportable). GitHub Actions rebuilds daily to track official releases.

## Features

- Profile data in `Profiles/`, cache in `Cache/`
- No registry writes — delete the folder to uninstall
- Runs from removable media
- Every release ships a `.sha256` checksum
- Injection check + real portability smoke test before publish

## Quick start

**Install**

1. Open the [latest release](https://github.com/Piracola/Floorp_portable/releases/latest)
2. Download `Floorp_<version>.7z` (**not** `Source code`)
3. Extract anywhere, e.g. `D:\Browser\Floorp`
4. Double-click `开始.bat` to create a shortcut, then launch via that shortcut

**Update**

1. Close Floorp completely
2. Rename the old `Floorp` folder to `Floorp_old`
3. Extract the new `Floorp` folder in place (**keep `Profiles/`**)
4. Confirm data is intact, then delete `Floorp_old`

**Uninstall**

Delete the whole extracted folder after backing up `Profiles/` if needed.

## FAQ

**Which file do I download?**  
`Floorp_<version>.7z`. `Source code` is not a browser.

**Where is my data?**  
`Profiles/` next to the browser folder.

**Can I run it from a USB drive?**  
Yes. Prefer a short path such as `U:\Floorp`.

**Antivirus alert?**  
Portable patching rewrites module imports and is often a false positive. Download only from this repo's Releases and verify the `.sha256` hash.

**How do I change the language?**  
The Floorp installer is multilingual: `Settings → General → Language`.

More in the [user guide](./docs/usage.md).

## Related projects

| Project | Notes |
| --- | --- |
| [Gecko-Portable](https://github.com/Piracola/Gecko-Portable) | Shared builder |
| [Firefox-Portable](https://github.com/Piracola/Firefox-Portable) | Portable Firefox |
| [Zen-Portable](https://github.com/Piracola/Zen-Portable) | Portable Zen |
| [Floorp](https://github.com/Floorp-Projects/Floorp) | Upstream browser |
| [libportable](https://github.com/adonais/libportable) | Upstream portable runtime |

## License

MIT — see [LICENSE](LICENSE).

Floorp itself remains copyright Floorp Projects and is covered by its own license. The libportable component ships with the package under its own license.

---

<div align="center">

<sub>Built and maintained by</sub>

**Piracola**

</div>

[badge-release]: https://img.shields.io/github/v/release/Piracola/Floorp_portable?display_name=tag&style=flat-square&color=3b82f6&label=Release
[badge-downloads]: https://img.shields.io/github/downloads/Piracola/Floorp_portable/total?style=flat-square&color=2ea043&label=Downloads
[badge-build]: https://img.shields.io/github/actions/workflow/status/Piracola/Floorp_portable/Floorp-Portable-package.yml?branch=main&style=flat-square&label=Build
[badge-license]: https://img.shields.io/github/license/Piracola/Floorp_portable?style=flat-square&color=6e7681&label=License

[link-release]: https://github.com/Piracola/Floorp_portable/releases/latest
[link-usage]: ./docs/usage.md
[link-actions]: https://github.com/Piracola/Floorp_portable/actions/workflows/Floorp-Portable-package.yml
[link-license]: https://github.com/Piracola/Floorp_portable/blob/main/LICENSE
