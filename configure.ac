#
#   configure.ac
#
#   Copyright (C) 1997 Free Software Foundation, Inc.
#
#   Author:  Adam Fedor <fedor@gnu.org>
#
#   This file is part of GNUstep.
#
#   This library is free software; you can redistribute it and/or
#   modify it under the terms of the GNU General Public License
#   as published by the Free Software Foundation; either version 2
#   of the License, or (at your option) any later version.
#   
#   You should have received a copy of the GNU General Public
#   License along with this library; see the file COPYING.LIB.
#   If not, write to the Free Software Foundation,
#   59 Temple Place - Suite 330, Boston, MA 02111-1307, USA.

AC_INIT
AC_CONFIG_SRCDIR([ChangeLog])

#--------------------------------------------------------------------
# top-level dir and arguments
#--------------------------------------------------------------------
TOPLEV=`pwd`
AC_SUBST(TOPLEV)

#--------------------------------------------------------------------
# The GNUstep root directory.
# This is local just for compiling nib2gmodel
#--------------------------------------------------------------------
AC_PREFIX_DEFAULT(`if test "x$GNUSTEP_SYSTEM_ROOT" = "x"; then
  if test -d C: ; then
    echo C:/GNUstep;
  else
    echo /usr/GNUstep ;
  fi
else
  echo "$GNUSTEP_SYSTEM_ROOT" ;
fi`)

EXEEXT=
if test "$program_suffix" != "NONE"; then
  EXEEXT=$program_suffix
fi
AC_SUBST(EXEEXT)

AC_CANONICAL_TARGET([])
AC_PROG_INSTALL
AC_PROG_LN_S([])

AC_ARG_WITH(library-combo,
[--with-library-combo		Set default library combinations ],
ac_cv_library_combo=$withval,
ac_cv_library_combo=
)

if test "$ac_cv_library_combo" = ""; then
  case "$host_os" in
    darwin*)   ac_cv_library_combo=apple-apple-apple ;;
    nextstep4) ac_cv_library_combo=nx-nx-nx          ;;
    openstep4) ac_cv_library_combo=nx-nx-nx          ;;
    *)         ac_cv_library_combo=gnu-gnu-gnu       ;;
  esac
fi
AC_SUBST(ac_cv_library_combo)

#--------------------------------------------------------------------
# Configure subdirectories
#
#--------------------------------------------------------------------
AC_CONFIG_SUBDIRS([make])

#--------------------------------------------------------------------
# Produce the output files
#--------------------------------------------------------------------
AC_CONFIG_FILES([GNUmakefile])
AC_OUTPUT


