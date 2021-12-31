#
# Copyright (C) 2016-2018 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python-rrdtool
PKG_VERSION:=1.4.7
PKG_RELEASE:=1

PYPI_NAME:=python-rrdtool
PKG_HASH:=7112a594ccd7759d59eaebf061ddacbd

PKG_LICENSE:=LGPL-3.0-or-later
PKG_LICENSE_FILES:=LICENSE
PKG_MAINTAINER:= pbnan

include ../pypi.mk
include $(INCLUDE_DIR)/package.mk
include ../python3-package.mk

define Package/python3-rrdtool
  SECTION:=lang
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Working Python RRDTool binding
  URL:=https://pypi.org/project/python-rrdtool
  DEPENDS:=+python3 +rrdtool1
endef

define Package/python3-rrd/description
This is a working Python Package of RRDtool binding to Python.
It delivers the same API as original binding (actually, it IS
original binding, but installable via pip.)
endef

$(eval $(call Py3Package,python3-rrdtool))
$(eval $(call BuildPackage,python3-rrdtool))
$(eval $(call BuildPackage,python3-rrdtool-src))
