# Luci-app-OpenList

I18N: English | [中文](README.md) | [日本語](README_JA.md)

🗂️A file list program that supports multiple storages, powered by Gin and SolidJS, fork of AList.

## How to add to OpenWrt?

### 1. Clone to OpenWrt source code using git:
```bash
git clone https://github.com/Internet1235/Luci-app-OpenList.git package/openlist
```
- #### Add to configuration menu:
```bash
make menuconfig
```
#### Navigate to ``Luci → Applications``, select ``luci-app-openlist``, then ``save`` and exit.

-----------------------------

## ⚠️ Important Compatibility Notice: 
- This plugin source code only supports the JavaScript version of Luci and does not support the Lua version of Luci (versions 21.02 - 24.10)
- This plugin source code supports official OpenWrt, ImmortalWrt, LEDE, istoreOS, etc., for versions 21.02 - 24.10

## Plugin Screenshots

![screenshots](https://cdn.jsdelivr.net/gh/Internet1235/Luci-app-OpenList@main/docs/1.png)
---
![screenshots](https://cdn.jsdelivr.net/gh/Internet1235/Luci-app-OpenList@main/docs/2.png)


## Credits: 

- [OpenList](https://github.com/OpenListTeam/OpenList)
- OpenList Plugin: https://github.com/Internet1235/Luci-app-OpenList.git && https://github.com/coolsnowwolf/packages/tree/master/net/openlist
- [OpenWrt](https://github.com/openwrt/openwrt)
- [coolsnowwolf/lede](https://github.com/coolsnowwolf/lede)
- [ImmortalWrt](https://github.com/immortalwrt/immortalwrt)

