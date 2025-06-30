# Luci-app-OpenList

I18N: 中文 | [English](README_EN.md) | [日本語](README_JA.md)

🗂️一个支持多存储的文件列表程序，使用 Gin 和 SolidJS，基于 AList 项目 fork 开发

## 如何添加到OpenWrt里?

### 1. 使用git clone克隆到OpenWrt源码里:
```bash
git clone https://github.com/Internet1235/Luci-app-OpenList.git package/openlist
```
- #### 在配置菜单中添加OpenList:
```bash
make menuconfig
```
#### 在``Luci -> Applications``勾选``luci-app-openlist``,选择``Save``保存退出即可。

-----------------------------

## ⚠️ 重要兼容性说明: 
- 该插件源码仅支持js版本的Luci，不支持lua版本的Luci(即版本号21.02 - 24.10)
- 该插件源码支持版本号21.02 - 24.10的官方OpenWrt、ImmortalWrt、LEDE、istoreOS等等

## 插件使用效果

![screenshots](https://cdn.jsdelivr.net/gh/Internet1235/Luci-app-OpenList@main/docs/1.png)
---
![screenshots](https://cdn.jsdelivr.net/gh/Internet1235/Luci-app-OpenList@main/docs/2.png)


## Credits: 

- [OpenList](https://github.com/OpenListTeam/OpenList)
- OpenList插件: https://github.com/Internet1235/Luci-app-OpenList.git && https://github.com/coolsnowwolf/packages/tree/master/net/openlist
- [OpenWrt](https://github.com/openwrt/openwrt)
- [coolsnowwolf/lede](https://github.com/coolsnowwolf/lede)
- [ImmortalWrt](https://github.com/immortalwrt/immortalwrt)

