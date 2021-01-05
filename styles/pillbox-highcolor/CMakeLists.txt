kde2_module(pillboxhighcolor SOURCES pillbox.cpp plugin.cpp LIBS kde2::kdeui)
install(FILES pillbox.themerc DESTINATION ${KDE2_DATADIR}/kstyle/themes)

