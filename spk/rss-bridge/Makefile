SPK_NAME = rss-bridge
SPK_VERS = 2023.07.13
SPK_REV = 1
SPK_ICON = src/rss-bridge.png
DSM_UI_DIR = app

DEPENDS = cross/$(SPK_NAME)

MAINTAINER = vitkabele
DESCRIPTION = The RSS feed for websites missing it.
ADMIN_URL = /rss-bridge/
DISPLAY_NAME = RSS Bridge

HOMEPAGE = https://rss-bridge.org
LICENSE  = Unlicense

include ../../mk/spksrc.common.mk
##
## This package can be built for DSM <6.0, DSM >=6.0;<7.0 and DSM >=7.0
## To build all versions call:
## make && make TCVERSION=6.0 && make TCVERSION=7.0 
##
SPK_DEPENDS = "WebStation>=2.1.0:PHP7.4>=7.4.0"
CONF_DIR = src/conf

# we need a nop sss script to avoid creation of service control.
SSS_SCRIPT = src/dsm-control.sh

# Pure PHP package, make sure ARCH is not defined
override ARCH=

include ../../mk/spksrc.spk.mk

