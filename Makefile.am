## kdeartwork/Makefile.am
## (C) 1997-2001 Stephan Kulow

SUBDIRS = $(TOPSUBDIRS)

AUTOMAKE_OPTIONS = foreign 1.4

$(top_srcdir)/acinclude.m4: $(top_srcdir)/admin/acinclude.m4.in $(top_srcdir)/admin/libtool.m4.in
	@cd $(top_srcdir) && cat admin/acinclude.m4.in admin/libtool.m4.in > acinclude.m4

EXTRA_DIST = admin
dist-hook:
	cd $(top_distdir) && perl $(top_srcdir)/admin/am_edit -padmin

$(top_srcdir)/configure.in: $(top_srcdir)/configure.files $(shell test -f $(top_srcdir)/configure.files && sed -e "s%^%\$(top_srcdir)/%" $(top_srcdir)/configure.files) $(top_srcdir)/subdirs
	cd $(top_srcdir) && $(MAKE) -f admin/Makefile.common configure.in
$(top_srcdir)/subdirs:
	cd $(top_srcdir) && $(MAKE) -f admin/Makefile.common subdirs
$(top_srcdir)/configure.files:
	cd $(top_srcdir) && $(MAKE) -f admin/Makefile.common configure.files

# For Themes
themesdir =  $(kde_datadir)/kthememgr/Themes
install-data-local:
	cp -r $(srcdir)/Themes BuildThemes; \
	rm -rf `find BuildThemes -type d -name CVS -print`; \
	( cd BuildThemes; \
	for f in *; do \
	  if [ -d $$f -a $$f != "CVS" ]; then \
	    $(TAR) -b 16 -c -f - $$f| gzip -c > $(DESTDIR)$(themesdir)/$$f.ktheme; \
	  fi; \
	done ); \
	rm -rf BuildThemes;
