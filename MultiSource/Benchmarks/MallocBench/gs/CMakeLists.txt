set(PROG gs)
list(APPEND LDFLAGS -lm)
list(APPEND CPPFLAGS -DNOMEMOPT -DGS_LIB_DEFAULT="${CMAKE_CURRENT_SOURCE_DIR}:${CMAKE_CURRENT_SOURCE_DIR}/fonts")
list(APPEND CFLAGS -Wno-implicit-function-declaration)
list(APPEND CPPFLAGS -DNOPRIVATE)
set(Source gs.c gsmain.c gp_unix.c utrace.c)
list(APPEND Source ialloc.c idebug.c idict.c iinit.c iname.c interp.c iscan.c iutil.c stream.c zarith.c zarray.c zcontrol.c zdict.c zfile.c zgeneric.c zmath.c zmisc.c zpacked.c zrelbit.c zstack.c zstring.c ztype.c zvmem.c zchar.c zcolor.c zfont.c zdevice.c zgstate.c zht.c zmatrix.c zpaint.c zpath.c zpath2.c)
list(APPEND Source gschar.c gscolor.c gscoord.c gsdevice.c gsfile.c gsfont.c gsimage.c gsim2out.c gsline.c gsmatrix.c gsmisc.c gspaint.c gspath.c gspath2.c gsstate.c gstype1.c gxcache.c gxcolor.c gxdither.c gxdraw.c gxfill.c gxht.c gxpath.c gxpath2.c gxstroke.c gdevmem.c gdevs.c)
set(RUN_OPTIONS -DNODISPLAY ${CMAKE_CURRENT_SOURCE_DIR}/INPUT/large.ps)
llvm_multisource()
