<div align="center">

# Floorp 便携版

全自动构建的 Floorp Windows x64 便携版，数据随目录携带，不写注册表。

[![最新版本][badge-release]][link-release]
[![总下载量][badge-downloads]][link-release]
[![构建状态][badge-build]][link-actions]
[![许可证][badge-license]][link-license]

**[⬇ 下载最新版本][link-release]** · **[📖 使用文档][link-usage]**

**简体中文** | [English](README.en.md)

</div>

> 构建系统见 [Gecko-Portable](https://github.com/Piracola/Gecko-Portable)——本仓库仅是其构建配置之一。

## 仓库导航

- [Releases 下载](https://github.com/Piracola/Floorp_portable/releases/latest)：获取 `Floorp_<版本>.7z`
- [使用文档](./docs/usage.md)：目录结构、配置、校验与完整说明
- [开发文档](./docs/development.md)：自动构建与本地复现
- [Gecko-Portable](https://github.com/Piracola/Gecko-Portable)：通用构建器
- [Firefox-Portable](https://github.com/Piracola/Firefox-Portable) · [Zen-Portable](https://github.com/Piracola/Zen-Portable)：同系列项目

## 项目简介

[Floorp](https://floorp.app/) 是基于 Firefox 的浏览器，由日本团队开发，主打丰富的界面定制和垂直标签页。本项目直接取用其官方安装包，通过 [libportable](https://github.com/adonais/libportable) 实现便携化：所有数据都留在解压目录里，不写注册表、不污染系统，可以放进 U 盘随身携带。GitHub Actions 每天自动跟进官方新版本。

## 功能特性

- 用户数据保存在解压目录的 `Profiles/`，缓存在 `Cache/`
- 不写注册表，删除文件夹即卸载
- 可放在 U 盘等移动介质中使用
- 每个 Release 附带 `.sha256` 校验文件
- 发布前经过注入校验 + 真机便携性实测

## 快速开始

**安装**

1. 打开 [最新 Release](https://github.com/Piracola/Floorp_portable/releases/latest)
2. 下载 `Floorp_<版本号>.7z`（**不要**下载 `Source code`）
3. 解压到任意目录，例如 `D:\Browser\Floorp`
4. 双击 `开始.bat` 生成快捷方式，之后用快捷方式启动

**更新**

1. 完全关闭 Floorp
2. 把旧的 `Floorp` 目录改名为 `Floorp_old`
3. 解压新版 `Floorp` 目录到原位置（**保留旁边的 `Profiles/`**）
4. 确认数据正常后删除 `Floorp_old`

**卸载**

删除整个解压目录即可。请先确认 `Profiles/` 里没有还需要的数据。

## 常见问题

**该下载哪个文件？**  
`Floorp_<版本号>.7z`。`Source code` 是仓库源码，不是浏览器。

**数据存在哪？**  
解压目录下的 `Profiles/`。备份和迁移时保留它即可。

**能放 U 盘吗？**  
可以。建议用简单路径，例如 `U:\Floorp`。

**杀毒软件报毒？**  
便携化需要修改模块导入表，容易被误报。请只从本仓库 Release 下载，并用 `.sha256` 核对后自行判断。

**界面语言怎么改？**  
Floorp 安装包自带多语言，在 `设置 → 常规 → 语言` 切换即可。

更多问题见 [使用文档](./docs/usage.md)。

## 相关项目

| 项目 | 说明 |
| --- | --- |
| [Gecko-Portable](https://github.com/Piracola/Gecko-Portable) | 通用构建器 |
| [Firefox-Portable](https://github.com/Piracola/Firefox-Portable) | Firefox 便携版 |
| [Zen-Portable](https://github.com/Piracola/Zen-Portable) | Zen 便携版 |
| [Floorp](https://github.com/Floorp-Projects/Floorp) | 上游浏览器项目 |
| [libportable](https://github.com/adonais/libportable) | 上游便携化运行时 |

## 许可证

本仓库采用 MIT 许可证，详见 [LICENSE](LICENSE)。

Floorp 浏览器本体的版权归 Floorp Projects 所有，遵循其自身许可证。便携化组件 libportable 遵循其自身许可证，随成品一起分发。

---

<div align="center">

<sub>Built and maintained by</sub>

**Piracola**

</div>

[badge-release]: https://img.shields.io/github/v/release/Piracola/Floorp_portable?display_name=tag&style=flat-square&color=3b82f6&label=%E6%9C%80%E6%96%B0%E7%89%88%E6%9C%AC
[badge-downloads]: https://img.shields.io/github/downloads/Piracola/Floorp_portable/total?style=flat-square&color=2ea043&label=%E6%80%BB%E4%B8%8B%E8%BD%BD%E9%87%8F
[badge-build]: https://img.shields.io/github/actions/workflow/status/Piracola/Floorp_portable/Floorp-Portable-package.yml?branch=main&style=flat-square&label=%E6%9E%84%E5%BB%BA%E7%8A%B6%E6%80%81
[badge-license]: https://img.shields.io/github/license/Piracola/Floorp_portable?style=flat-square&color=6e7681&label=%E8%AE%B8%E5%8F%AF%E8%AF%81

[link-release]: https://github.com/Piracola/Floorp_portable/releases/latest
[link-usage]: ./docs/usage.md
[link-actions]: https://github.com/Piracola/Floorp_portable/actions/workflows/Floorp-Portable-package.yml
[link-license]: https://github.com/Piracola/Floorp_portable/blob/main/LICENSE
