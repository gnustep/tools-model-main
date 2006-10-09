#
#  GNUmakefile for GNUstep nib2model Documentation directory
#  Copyright (C) 1999 Free Software Foundation, Inc.
#
#  Written by:	Adam Fedor <fedor@gnu.org>
#
#  This file is part of GNUstep.
#
#  This package is free software; you can redistribute it and/or
#  modify it under the terms of the GNU Library General Public
#  License as published by the Free Software Foundation; either
#  version 2 of the License, or (at your option) any later version.
#
#  This package is distributed in the hope that it will be useful,
#  but WITHOUT ANY WARRANTY; without even the implied warranty of
#  MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.	 See the GNU
#  Library General Public License for more details.
#
#  You should have received a copy of the GNU Library General Public
#  License along with this library; if not, write to the Free
#  Software Foundation, Inc., 675 Mass Ave, Cambridge, MA 02139, USA.

include $(GNUSTEP_MAKEFILES)/common.make

include ../Version

# The documents to be generated
DOCUMENT_NAME = 

# The text documents to be generated
DOCUMENT_TEXT_NAME = \
INSTALL \
README \
ANNOUNCE \
NEWS 

TOP_DOC_FILES = \
INSTALL \
README \
ANNOUNCE \
NEWS

INSTALL_TEXI_FILES = version.texi
INSTALL_TEXT_MAIN = install.texi

README_TEXI_FILES = version.texi
README_TEXT_MAIN = readme.texi

ANNOUNCE_TEXI_FILES = version.texi news.texi
ANNOUNCE_TEXT_MAIN = announce.texi

NEWS_TEXI_FILES = version.texi
NEWS_TEXT_MAIN = news.texi

#
# Include in the rules
#
-include GNUmakefile.preamble

-include GNUmakefile.local

include $(GNUSTEP_MAKEFILES)/documentation.make

-include GNUmakefile.postamble
