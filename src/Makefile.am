#  Copyright 2005 Adam Jackson.
#
#  Permission is hereby granted, free of charge, to any person obtaining a
#  copy of this software and associated documentation files (the "Software"),
#  to deal in the Software without restriction, including without limitation
#  on the rights to use, copy, modify, merge, publish, distribute, sub
#  license, and/or sell copies of the Software, and to permit persons to whom
#  the Software is furnished to do so, subject to the following conditions:
#
#  The above copyright notice and this permission notice (including the next
#  paragraph) shall be included in all copies or substantial portions of the
#  Software.
#
#  THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
#  IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
#  FITNESS FOR A PARTICULAR PURPOSE AND NON-INFRINGEMENT.  IN NO EVENT SHALL
#  ADAM JACKSON BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER
#  IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN
#  CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

# this is obnoxious:
# -module lets us name the module exactly how we want
# -avoid-version prevents gratuitous .0.0.0 version numbers on the end
# _ladir passes a dummy rpath to libtool so the thing will actually link
# TODO: -nostdlib/-Bstatic/-lgcc platform magic, not installing the .a, etc.

vmwlegacy_drv_la_LTLIBRARIES = vmwlegacy_drv.la
vmwlegacy_drv_la_LDFLAGS = -module -avoid-version
vmwlegacy_drv_la_CFLAGS = @XORG_CFLAGS@
vmwlegacy_drv_ladir = @moduledir@/drivers

vmwlegacy_drv_la_SOURCES = \
	bits2pixels.c \
	bits2pixels.h \
	guest_os.h \
	includeCheck.h \
	svga_escape.h \
	svga_limits.h \
	svga_modes.h \
	svga_overlay.h \
	svga_reg.h \
	svga_struct.h \
	vm_basic_types.h \
	vm_device_version.h \
	vmware.c \
	vmwarecurs.c \
	vmware.h \
	vmwarectrl.c \
	vmwarectrl.h \
	vmwarectrlproto.h \
	vmwarexinerama.c \
	vmwarevideo.c \
	vmwaremodes.c

vmware_drv_la_LTLIBRARIES = vmware_drv.la
vmware_drv_la_LDFLAGS = -module -avoid-version
vmware_drv_la_CFLAGS = @XORG_CFLAGS@ @LIBDRM_CFLAGS@
vmware_drv_la_LIBADD = @LIBDRM_LIBS@
vmware_drv_ladir = @moduledir@/drivers

vmware_drv_la_SOURCES = \
	vmwaremodule.c
