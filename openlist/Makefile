# SPDX-License-Identifier: GPL-2.0-only
#
# Copyright (C) 2025 LEDE

include $(TOPDIR)/rules.mk

PKG_NAME:=openlist
PKG_VERSION:=4.1.0
PKG_RELEASE:=1

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://codeload.github.com/OpenListTeam/OpenList/tar.gz/v$(PKG_VERSION)?
PKG_HASH:=cdaf91413fe07b3d8155f644237a839dac09f084e812b25c76effca7dfc1d3f2
PKG_BUILD_DIR:=$(BUILD_DIR)/OpenList-$(PKG_VERSION)

PKG_LICENSE:=AGPL-3.0-only
PKG_LICENSE_FILES:=LICENSE
PKG_MAINTAINER:=Internet1235

PKG_BUILD_DEPENDS:=golang/host
PKG_BUILD_PARALLEL:=1
PKG_BUILD_FLAGS:=no-mips16
PKG_USE_MIPS16:=0

GO_PKG:=github.com/OpenListTeam/OpenList/v4
GO_PKG_LDFLAGS_X:= \
	$(GO_PKG)/internal/conf.Version=$(PKG_VERSION) \
	$(GO_PKG)/internal/conf.WebVersion=$(FRONTEND_VERSION)
ifeq ($(filter aarch64 x86_64, $(ARCH)),)
  GO_PKG_EXCLUDES:=drivers/lark
endif

include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/golang/golang-package.mk

define Package/openlist
  SECTION:=net
  CATEGORY:=Network
  TITLE:=A file list program that supports multiple storage
  URL:=https://openlist.team/
  DEPENDS:=$(GO_ARCH_DEPENDS) +ca-bundle +fuse-utils
endef

define Package/openlist/description
  A file list program that supports multiple storage, and supports
  web browsing and webdav, powered by gin and Solidjs, fork of AList.
endef

define Package/openlist/conffiles
/etc/openlist/
/etc/config/openlist
endef

FRONTEND_VERSION:=4.1.0
FRONTEND_FILE:=$(PKG_NAME)-frontend-v$(FRONTEND_VERSION).tar.gz
define Download/openlist-forntend
	URL:=https://github.com/OpenListTeam/OpenList-Frontend/releases/download/v$(FRONTEND_VERSION)/
	URL_FILE:=openlist-frontend-dist-v$(FRONTEND_VERSION).tar.gz
	FILE:=$(FRONTEND_FILE)
	HASH:=ddaeb76aad74a858358de9a1e0d1aff93651605859813b0891b9f4f431d1a87f
endef

define Build/Prepare
	$(call Build/Prepare/Default)

	( \
		mkdir -p $(PKG_BUILD_DIR)/public/dist ; \
		gzip -dc $(DL_DIR)/$(FRONTEND_FILE) | $(HOST_TAR) -C $(PKG_BUILD_DIR)/public/dist $(TAR_OPTIONS) ; \
	)
endef

ifneq ($(CONFIG_USE_MUSL),)
  TARGET_CFLAGS += -D_LARGEFILE64_SOURCE
endif

define Package/openlist/install
	$(call GoPackage/Package/Install/Bin,$(PKG_INSTALL_DIR))

	$(INSTALL_DIR) $(1)/usr/bin/
	$(INSTALL_BIN) $(PKG_INSTALL_DIR)/usr/bin/OpenList $(1)/usr/bin/

	$(INSTALL_DIR) $(1)/etc/config
	$(INSTALL_CONF) $(CURDIR)/files/openlist.config $(1)/etc/config/openlist
	$(INSTALL_DIR) $(1)/etc/init.d
	$(INSTALL_BIN) $(CURDIR)/files/openlist.init $(1)/etc/init.d/openlist
endef

$(eval $(call Download,openlist-forntend))
$(eval $(call GoBinPackage,openlist))
$(eval $(call BuildPackage,openlist))
