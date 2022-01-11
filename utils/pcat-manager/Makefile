include $(TOPDIR)/rules.mk

PKG_NAME:=pcat-manager
PKG_VERSION:=1.0.0
PKG_RELEASE:=0

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=ssh://git@git.g77k.com/supercatexpert/pcat-manager.git
PKG_SOURCE_DATE:=2022-01-11
PKG_SOURCE_VERSION:=a6989792336dbea4d510ba1426a52ce19c8f889a

PKG_LICENSE:=GPL-3.0
PKG_LICENSE_FILES:=LICENSE

PKG_INSTALL:=1
PKG_USE_MIPS16:=0
PKG_BUILD_DEPENDS:=meson/host

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/nls.mk
include ../../devel/meson/meson.mk

define Package/pcat-manager
  SECTION:=utils
  CATEGORY:=Utilities
  DEPENDS:=+glib2 +libgpiod +libjson-c +libusb-1.0
  TITLE:=PCat System Manager
  URL:=https://git.g77k.com
  PROVIDES:=pcat-manager
endef

define Package/pcat-manager/description
  PCat Manager is a system service for power management and modem controlling.
endef

define Package/pcat-manager/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) \
		$(PKG_INSTALL_DIR)/usr/bin/pcat-manager \
		$(1)/usr/bin/pcat-manager

	$(INSTALL_DIR) $(1)/etc/init.d
	$(INSTALL_BIN) ./files/pcat-manager.init $(1)/etc/init.d/pcat-manager
endef


$(eval $(call BuildPackage,pcat-manager))
