#
# Copyright (C) 2012 Jo-Philipp Wich <jo@mein.io>
#
# This is free software, licensed under the Apache 2 license.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=rktoolkit
PKG_RELEASE:=1

PKG_MAINTAINER:=Kyosuke Nekoyashiki <supercatexpert@gmail.com>
PKG_LICENSE:=LICENSE.APACHE

include $(INCLUDE_DIR)/package.mk

define Package/rktoolkit
  SECTION:=utils
  CATEGORY:=Utilities
  TITLE:=rktoolkit
endef

define Package/rktoolkit/description
  Some toolkits for configuring rockchip board..
endef

define Build/Configure
endef

define Build/Compile
	$(TARGET_CC) $(TARGET_CFLAGS) $(TARGET_LDFLAGS) -o $(PKG_BUILD_DIR)/vendor_storage $(PKG_BUILD_DIR)/vendor_storage.c
endef

define Package/rktoolkit/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/vendor_storage $(1)/usr/bin/vendor_storage
endef

$(eval $(call BuildPackage,rktoolkit))
