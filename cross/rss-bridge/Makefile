PKG_NAME = rss-bridge
PKG_VERS = 2023-07-13
PKG_EXT = tar.gz
PKG_DIST_NAME = $(PKG_VERS).$(PKG_EXT)
PKG_DIST_SITE = https://github.com/RSS-Bridge/rss-bridge/archive/refs/tags
PKG_DIST_FILE = $(PKG_NAME)-$(PKG_VERS).$(PKG_EXT)
PKG_DIR = $(PKG_NAME)-$(PKG_VERS)

DEPENDS =

HOMEPAGE = https://rss-bridge.org/
COMMENT  = RSS-Bridge is a PHP project capable of generating RSS and Atom feeds for websites that don't have one.
LICENSE  = Unlicense license

INSTALL_TARGET = rssbridge_install

include ../../mk/spksrc.install-resources.mk

.PHONY: rssbridge_install
rssbridge_install:
	install -m 755 -d $(STAGING_INSTALL_PREFIX)/web $(STAGING_INSTALL_PREFIX)/var
	cp -R $(WORK_DIR)/$(PKG_DIR)/* $(STAGING_INSTALL_PREFIX)/web/
	# We put the config file to pkg var and patch the php files to refer to this location
	# This will probably work only on DSM7 as the var/ location is different for DSM<7
	cp $(WORK_DIR)/$(PKG_DIR)/config.default.ini.php  $(STAGING_INSTALL_PREFIX)/var/config.ini.php
