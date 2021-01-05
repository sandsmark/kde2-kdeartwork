kde2_module(ksgistyle SOURCES ksgistyle.cpp plugin.cpp LIBS kde2::kdeui)
install(FILES ksgistyle.themerc DESTINATION ${KDE2_DATADIR}/kstyle/themes)

