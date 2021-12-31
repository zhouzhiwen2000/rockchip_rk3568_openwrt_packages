#
# Copyright (C) 2016-2018 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=rrdtool
PKG_VERSION:=0.1.15
PKG_RELEASE:=1

PYPI_NAME:=$(PKG_NAME)
PKG_HASH:=5e818ed5b5c656448f2e641af04e1f4e

PKG_LICENSE:=LGPL-2.1
PKG_LICENSE_FILES:=LICENSE
PKG_MAINTAINER:= Christian Kröger

PKG_BUILD_DEPENDS:=librrd1

include ../pypi.mk
include $(INCLUDE_DIR)/package.mk
include ../python3-package.mk

define Package/python3-rrdtool
  SECTION:=lang
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Python bindings for rrdtool
  URL:=https://pypi.org/project/rrdtool
  DEPENDS:=+python3
endef

define Package/python3-rrdtool/description
The bindings are based on the code of the original Python 2
bindings module for rrdtool by Hye-Shik Chang and are now
shipped with the RRDtool distribution. This project is
maintained separately to provide a more pythonic way to install
those bindings via PyPI.
endef

$(eval $(call Py3Package,python3-rrdtool))
$(eval $(call BuildPackage,python3-rrdtool))
$(eval $(call BuildPackage,python3-rrdtool-src))
