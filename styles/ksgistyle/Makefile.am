INCLUDES= $(all_includes)
METASOURCES=AUTO
noinst_HEADERS = ksgistyle.h
lib_LTLIBRARIES = ksgistyle.la
ksgistyle_la_LDFLAGS = $(all_libraries) -module -avoid-version -no-undefined
ksgistyle_la_SOURCES = ksgistyle.cpp plugin.cpp
ksgistyle_la_LIBADD = $(LIB_KDEUI) 

data_DATA = ksgistyle.themerc
datadir = $(kde_datadir)/kstyle/themes
EXTRA_DIST = $(data_DATA)
