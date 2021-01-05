kde2_module(ksgistyle SOURCES ksgistyle.cpp plugin.cpp LIBS kde2::kdeui)
install(FILES ksgi.themerc DESTINATION ${KDE2_DATADIR}/kstyle/themes)

