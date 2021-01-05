kde2_module(pillboxhighcolor SOURCES pillbox.cpp plugin.cpp LIBS kde2::kdeui)
install(FILES pillboxhighcolor.themerc DESTINATION ${KDE2_DATADIR}/kstyle/themes)

