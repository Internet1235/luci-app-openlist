# Luci-app-OpenList

I18N:  日本語 | [中文](README.md) | [English](README_EN.md)

🗂️複数のストレージをサポートするファイルリストプログラムで、Gin と SolidJS を使用し、AList プロジェクトをフォークして開発されまし

## OpenWrtへの追加方法

### 1. git cloneを使用してOpenWrtソースコードにクローンする:
```bash
git clone https://github.com/Internet1235/Luci-app-OpenList.git package/openlist
```
- #### 設定メニューにopenlistを追加:
```bash
make menuconfig
```
#### ``Luci → Applications``で``luci-app-openlist``を選択し、``Save``で保存して終了します。

-----------------------------

## ⚠️ 重要な互換性に関する注意: 
- このプラグインソースは、JavaScript版のLuci のみをサポートしています。Lua版のLuci(バージョン21.02 - 24.10)はサポートしていません
- このプラグインソースは、バージョン21.02 - 24.10の公式OpenWrt、ImmortalWrt、LEDE、istoreOSなどをサポートしています

## プラグインのスクリーンショット

![screenshots](https://cdn.jsdelivr.net/gh/Internet1235/Luci-app-OpenList@main/docs/1.png)
---
![screenshots](https://cdn.jsdelivr.net/gh/Internet1235/Luci-app-OpenList@main/docs/2.png)


## Credits: 

- [OpenList](https://github.com/OpenListTeam/OpenList)
- OpenListプラグイン: https://github.com/Internet1235/Luci-app-OpenList.git && https://github.com/coolsnowwolf/packages/tree/master/net/openlist
- [OpenWrt](https://github.com/openwrt/openwrt)
- [coolsnowwolf/lede](https://github.com/coolsnowwolf/lede)
- [ImmortalWrt](https://github.com/immortalwrt/immortalwrt)

