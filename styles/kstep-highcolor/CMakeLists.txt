kde2_module(kstephighcolorstyle SOURCES kstep.cpp plugin.cpp LIBS kde2::kdeui)
install(FILES kstep-highcolor.themerc DESTINATION ${KDE2_DATADIR}/kstyle/themes)

