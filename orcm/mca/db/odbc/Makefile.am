#
# Copyright (c) 2013-2014 Intel, Inc. All rights reserved.
# $COPYRIGHT$
# 
# Additional copyrights may follow
# 
# $HEADER$
#

sources = \
        db_odbc.h \
        db_odbc_component.c \
        db_odbc.c

# Make the output library in this directory, and name it either
# mca_<type>_<name>.la (for DSO builds) or libmca_<type>_<name>.la
# (for static builds).

if MCA_BUILD_orcm_db_odbc_DSO
component_noinst =
component_install = mca_db_odbc.la
else
component_noinst = libmca_db_odbc.la
component_install =
endif

mcacomponentdir = $(orcmlibdir)
mcacomponent_LTLIBRARIES = $(component_install)
mca_db_odbc_la_CPPFLAGS = $(db_odbc_CPPFLAGS)
mca_db_odbc_la_SOURCES = $(sources)
mca_db_odbc_la_LDFLAGS = -module -avoid-version $(db_odbc_LDFLAGS)
mca_db_odbc_la_LIBADD = $(db_odbc_LIBS)

noinst_LTLIBRARIES = $(component_noinst)
libmca_db_odbc_la_SOURCES =$(sources)
libmca_db_odbc_la_CPPFLAGS = $(db_odbc_CPPFLAGS)
libmca_db_odbc_la_LDFLAGS = -module -avoid-version $(db_odbc_LDFLAGS)
libmca_db_odbc_la_LIBADD = $(db_odbc_LIBS)
