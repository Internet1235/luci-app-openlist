# LuCI-app-OpenList

I18N: English | [中文](README.md) | [日本語](README_JA.md)

[![GitHub License](https://img.shields.io/github/license/Internet1235/luci-app-openlist)
](https://github.com/Internet1235/Luci-app-OpenList/blob/main/LICENSE)
[![GitHub Release](https://img.shields.io/github/v/release/Internet1235/luci-app-openlist)
](https://github.com/Internet1235/luci-app-openlist/releases)

🗂️A file list program that supports multiple storages, powered by Gin and SolidJS, fork of AList.

## How to add to OpenWrt?

### 1. Clone into OpenWrt source code using git:
```bash
git clone https://github.com/Internet1235/luci-app-openlist.git package/openlist
```
- #### Add OpenList in the configuration menu:
```bash
make menuconfig
```
#### Navigate to ``LuCI → Applications``, select ``luci-app-openlist``, then choose ``Save`` to save and choose ``Exit`` exit.

-----------------------------

## ⚠️ Important Compatibility Notice: 
- This plugin source code only supports the JavaScript version of LuCI and does not support the Lua version of LuCI (i.e., versions 21.02 - 24.10)
- This plugin source code supports official OpenWrt, ImmortalWrt, LEDE, istoreOS, etc., for versions 21.02 - 24.10

## Plugin Screenshots

![screenshots](https://cdn.jsdelivr.net/gh/Internet1235/luci-app-openlist@main/docs/1.png)
---
![screenshots](https://cdn.jsdelivr.net/gh/Internet1235/luci-app-openlist@main/docs/2.png)


## Credits: 

- [OpenList](https://github.com/OpenListTeam/OpenList)
- OpenList Plugin: https://github.com/Internet1235/luci-app-openlist.git && https://github.com/coolsnowwolf/packages/tree/master/net/openlist
- [OpenWrt](https://github.com/openwrt/openwrt)
- [coolsnowwolf/lede](https://github.com/coolsnowwolf/lede)
- [ImmortalWrt](https://github.com/immortalwrt/immortalwrt)

