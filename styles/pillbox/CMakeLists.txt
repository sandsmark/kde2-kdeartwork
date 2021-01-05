kde2_module(pillboxstyle SOURCES pillbox.cpp plugin.cpp LIBS kde2::kdeui)
install(FILES pillbox.themerc DESTINATION ${KDE2_DATADIR}/kstyle/themes)

