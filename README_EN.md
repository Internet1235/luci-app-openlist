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
git clone https://github.com/Internet1235/luci-app-openlist.git -b lua package/openlist
```
- #### Add OpenList in the configuration menu:
```bash
make menuconfig
```
#### Navigate to ``LuCI → Applications``, select ``luci-app-openlist``, then choose ``Save`` to save and choose ``Exit`` exit.

---
#### To avoid conflicts with the built-in OpenList, run the following command after ```./scripts/feeds update -a```:
```bash
rm -rf feeds/packages/net/openlist
rm -rf feeds/luci/applications/luci-app-openlist
```

-----------------------------


## Plugin Screenshots

![screenshots](./docs/1.jpeg)
---
![screenshots](./docs/2.jpeg)


## Credits: 

- [OpenList](https://github.com/OpenListTeam/OpenList)
- OpenList Plugin: https://github.com/Internet1235/luci-app-openlist.git && https://github.com/coolsnowwolf/packages/tree/master/net/openlist
- [OpenWrt](https://github.com/openwrt/openwrt)
- [coolsnowwolf/lede](https://github.com/coolsnowwolf/lede)
- [ImmortalWrt](https://github.com/immortalwrt/immortalwrt)

