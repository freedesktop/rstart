
dnl  Copyright 2005 Red Hat, Inc.
dnl 
dnl  Permission to use, copy, modify, distribute, and sell this software and its
dnl  documentation for any purpose is hereby granted without fee, provided that
dnl  the above copyright notice appear in all copies and that both that
dnl  copyright notice and this permission notice appear in supporting
dnl  documentation, and that the name of Red Hat not be used in
dnl  advertising or publicity pertaining to distribution of the software without
dnl  specific, written prior permission.  Red Hat makes no
dnl  representations about the suitability of this software for any purpose.  It
dnl  is provided "as is" without express or implied warranty.
dnl 
dnl  RED HAT DISCLAIMS ALL WARRANTIES WITH REGARD TO THIS SOFTWARE,
dnl  INCLUDING ALL IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS, IN NO
dnl  EVENT SHALL RED HAT BE LIABLE FOR ANY SPECIAL, INDIRECT OR
dnl  CONSEQUENTIAL DAMAGES OR ANY DAMAGES WHATSOEVER RESULTING FROM LOSS OF USE,
dnl  DATA OR PROFITS, WHETHER IN AN ACTION OF CONTRACT, NEGLIGENCE OR OTHER
dnl  TORTIOUS ACTION, ARISING OUT OF OR IN CONNECTION WITH THE USE OR
dnl  PERFORMANCE OF THIS SOFTWARE.
dnl
dnl Process this file with autoconf to create configure.

AC_PREREQ([2.57])
AC_INIT(rstart,[0.99.0], [https://bugs.freedesktop.org/enter_bug.cgi?product=xorg],rstart)
AM_INIT_AUTOMAKE([dist-bzip2])
AM_MAINTAINER_MODE

AM_CONFIG_HEADER(config.h)

AC_ARG_VAR([RM],[Name of the rm command])
AC_ARG_VAR([LN],[Name of the ln command])

AC_CHECK_PROG([RM],[rm],[rm -f])
AC_CHECK_PROG([LN],[ln],[ln -s])

AC_PROG_CC
AC_PROG_INSTALL
AC_PATH_PROG(SED, sed)
if [[ -z $SED ]] ; then 
   AC_MSG_ERROR([sed not found])
fi

# Checks for pkg-config packages
PKG_CHECK_MODULES(RSTART, x11)
AC_SUBST(RSTART_CFLAGS)
AC_SUBST(RSTART_LIBS)

XORG_RELEASE_VERSION

AC_OUTPUT([
	Makefile 
])