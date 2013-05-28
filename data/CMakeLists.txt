ADD_SUBDIRECTORY(netpanel)
SET(ICON_SRCS
	search-icons/Ask.ico
	search-icons/Bing.ico
	search-icons/Google.ico
	search-icons/Twitter.ico
	search-icons/Wikipedia.ico
	search-icons/Yahoo.ico

    )

INSTALL(FILES ${ICON_SRCS} DESTINATION ${PKG_DATADIR}/${PROGRAMS}/search-icons)
