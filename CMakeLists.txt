cmake_minimum_required(VERSION 3.2)

project(python VERSION 2.7.12 LANGUAGES C)

if(MSVC)
    set(CMAKE_DEBUG_POSTFIX "d")
endif()

add_library(python SHARED
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/abstract.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/asdl.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/ast.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/bitset.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/boolobject.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/bufferobject.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/bytes_methods.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/bytearrayobject.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/bytesobject.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/cellobject.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/ceval.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/classobject.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/cobject.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/code.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/codecs.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/compile.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/complexobject.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/cStringIO.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/datetime.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/descrobject.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/dictobject.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/dtoa.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/enumobject.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/errcode.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/eval.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/fileobject.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/floatobject.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/frameobject.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/funcobject.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/genobject.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/graminit.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/grammar.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/import.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/intobject.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/intrcheck.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/iterobject.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/listobject.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/longintrepr.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/longobject.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/marshal.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/memoryobject.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/metagrammar.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/methodobject.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/modsupport.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/moduleobject.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/node.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/object.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/objimpl.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/opcode.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/osdefs.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/parsetok.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/patchlevel.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/pgen.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/pgenheaders.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/py_curses.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/pyarena.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/pycapsule.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/pyctype.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/pydebug.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/pyerrors.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/pyexpat.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/pyfpe.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/pygetopt.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/pymactoolbox.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/pymath.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/pymem.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/pyport.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/pystate.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/pystrcmp.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/pystrtod.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Python-ast.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Python.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/pythonrun.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/pythread.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/rangeobject.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/setobject.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/sliceobject.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/stringobject.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/structmember.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/structseq.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/symtable.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/sysmodule.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/timefuncs.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/token.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/traceback.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/tupleobject.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/ucnhash.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/unicodeobject.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/weakrefobject.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/_math.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/md5.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/rotatingtree.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/zlib/crc32.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/zlib/deflate.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/zlib/inffast.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/zlib/inffixed.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/zlib/inflate.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/zlib/inftrees.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/zlib/trees.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/zlib/zconf.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/zlib/zlib.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/zlib/zutil.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/cjkcodecs/alg_jisx0201.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/cjkcodecs/cjkcodecs.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/cjkcodecs/emu_jisx0213_2000.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/cjkcodecs/mappings_cn.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/cjkcodecs/mappings_hk.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/cjkcodecs/mappings_jisx0213_pair.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/cjkcodecs/mappings_jp.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/cjkcodecs/mappings_kr.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/cjkcodecs/mappings_tw.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/cjkcodecs/multibytecodec.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/_io/_iomodule.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Objects/stringlib/count.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Objects/stringlib/fastsearch.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Objects/stringlib/find.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Objects/stringlib/partition.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Objects/stringlib/split.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Objects/unicodetype_db.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Parser/parser.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Parser/tokenizer.h
    ${CMAKE_CURRENT_SOURCE_DIR}/PC/errmap.h
    ${CMAKE_CURRENT_SOURCE_DIR}/PC/pyconfig.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Python/importdl.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Python/thread_nt.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/_bisectmodule.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/_codecsmodule.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/_collectionsmodule.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/_csv.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/_functoolsmodule.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/_heapqmodule.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/_hotshot.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/_json.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/_localemodule.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/_lsprof.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/_math.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/_randommodule.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/_sre.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/_struct.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/_weakref.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/arraymodule.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/audioop.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/binascii.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/cmathmodule.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/cPickle.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/cStringIO.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/datetimemodule.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/errnomodule.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/future_builtins.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/gcmodule.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/imageop.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/itertoolsmodule.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/main.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/mathmodule.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/md5.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/md5module.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/mmapmodule.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/operator.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/parsermodule.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/posixmodule.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/rotatingtree.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/sha256module.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/sha512module.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/shamodule.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/signalmodule.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/stropmodule.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/symtablemodule.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/threadmodule.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/timemodule.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/xxsubtype.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/zipimport.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/zlibmodule.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/zlib/adler32.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/zlib/compress.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/zlib/crc32.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/zlib/deflate.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/zlib/gzclose.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/zlib/gzlib.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/zlib/gzread.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/zlib/gzwrite.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/zlib/infback.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/zlib/inffast.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/zlib/inflate.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/zlib/inftrees.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/zlib/trees.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/zlib/uncompr.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/zlib/zutil.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/cjkcodecs/_codecs_cn.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/cjkcodecs/_codecs_hk.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/cjkcodecs/_codecs_iso2022.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/cjkcodecs/_codecs_jp.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/cjkcodecs/_codecs_kr.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/cjkcodecs/_codecs_tw.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/cjkcodecs/multibytecodec.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/_io/_iomodule.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/_io/bufferedio.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/_io/bytesio.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/_io/fileio.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/_io/iobase.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/_io/stringio.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/_io/textio.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Objects/abstract.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Objects/boolobject.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Objects/bufferobject.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Objects/bytes_methods.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Objects/bytearrayobject.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Objects/capsule.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Objects/cellobject.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Objects/classobject.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Objects/cobject.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Objects/codeobject.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Objects/complexobject.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Objects/descrobject.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Objects/dictobject.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Objects/enumobject.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Objects/exceptions.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Objects/fileobject.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Objects/floatobject.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Objects/frameobject.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Objects/funcobject.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Objects/genobject.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Objects/intobject.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Objects/iterobject.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Objects/listobject.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Objects/longobject.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Objects/memoryobject.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Objects/methodobject.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Objects/moduleobject.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Objects/object.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Objects/obmalloc.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Objects/rangeobject.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Objects/setobject.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Objects/sliceobject.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Objects/stringobject.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Objects/structseq.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Objects/tupleobject.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Objects/typeobject.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Objects/unicodectype.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Objects/unicodeobject.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Objects/weakrefobject.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Parser/acceler.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Parser/bitset.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Parser/firstsets.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Parser/grammar.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Parser/grammar1.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Parser/listnode.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Parser/metagrammar.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Parser/myreadline.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Parser/node.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Parser/parser.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Parser/parsetok.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Parser/tokenizer.c
    ${CMAKE_CURRENT_SOURCE_DIR}/PC/_subprocess.c
    ${CMAKE_CURRENT_SOURCE_DIR}/PC/_winreg.c
    ${CMAKE_CURRENT_SOURCE_DIR}/PC/config.c
    ${CMAKE_CURRENT_SOURCE_DIR}/PC/dl_nt.c
    ${CMAKE_CURRENT_SOURCE_DIR}/PC/getpathp.c
    ${CMAKE_CURRENT_SOURCE_DIR}/PC/import_nt.c
    ${CMAKE_CURRENT_SOURCE_DIR}/PC/msvcrtmodule.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Python/_warnings.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Python/asdl.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Python/ast.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Python/bltinmodule.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Python/ceval.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Python/codecs.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Python/compile.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Python/dtoa.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Python/dynload_win.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Python/errors.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Python/formatter_string.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Python/formatter_unicode.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Python/frozen.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Python/future.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Python/getargs.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Python/getcompiler.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Python/getcopyright.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Python/getopt.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Python/getplatform.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Python/getversion.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Python/graminit.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Python/import.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Python/importdl.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Python/marshal.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Python/modsupport.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Python/mysnprintf.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Python/mystrtoul.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Python/peephole.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Python/pyarena.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Python/pyctype.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Python/pyfpe.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Python/pymath.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Python/pystate.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Python/pystrcmp.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Python/pystrtod.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Python/Python-ast.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Python/pythonrun.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Python/random.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Python/structmember.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Python/symtable.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Python/sysmodule.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Python/thread.c
    ${CMAKE_CURRENT_SOURCE_DIR}/Python/traceback.c
    ${CMAKE_CURRENT_SOURCE_DIR}/PC/python_nt.rc
    ${CMAKE_CURRENT_SOURCE_DIR}/Modules/getbuildinfo.c
)

target_include_directories(python
  PRIVATE
  $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/Include>
  $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/PC>
  $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/Python>
  $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/Modules/zlib>
  INTERFACE
  $<INSTALL_INTERFACE:include/python>
  PUBLIC
  $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/Include>
)

target_compile_definitions(python
  PRIVATE
  _CRT_SECURE_NO_WARNINGS
  _CRT_STDC_NO_DEPRECATE
  _USRDLL
  Py_BUILD_CORE
  Py_ENABLE_SHARED
)

# add_subdirectory(Modules/_ctypes)

if(${CMAKE_SIZEOF_VOID_P} EQUAL 4)
    add_custom_command(TARGET python
    PRE_BUILD
    COMMAND "C:/Program Files (x86)/MSBuild/14.0/Bin/amd64/MSBuild.exe" pcbuild.sln /p:Configuration=Release /p:Platform=win32
    WORKING_DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/PCbuild
    )
else()
    add_custom_command(TARGET python
    PRE_BUILD
    COMMAND "C:/Program Files (x86)/MSBuild/14.0/Bin/amd64/MSBuild.exe" pcbuild.sln /p:Configuration=Release /p:Platform=x64
    WORKING_DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/PCbuild
    )
endif()

include(CMakePackageConfigHelpers)
write_basic_package_version_file(
  ${CMAKE_CURRENT_BINARY_DIR}/${PROJECT_NAME}-config-version.cmake
  VERSION ${PROJECT_VERSION}
  COMPATIBILITY AnyNewerVersion
)

install(TARGETS ${PROJECT_NAME} EXPORT ${PROJECT_NAME}
  RUNTIME DESTINATION bin
  ARCHIVE DESTINATION lib
  LIBRARY DESTINATION lib
)

install(DIRECTORY
  ${CMAKE_CURRENT_SOURCE_DIR}/Include/
  DESTINATION include/python
)

install(FILES
  ${CMAKE_CURRENT_SOURCE_DIR}/PC/pyconfig.h
  DESTINATION include/python
)

install(DIRECTORY
  ${CMAKE_CURRENT_SOURCE_DIR}/PCbuild/
  DESTINATION lib/python/DLLs
  FILES_MATCHING PATTERN *.pyd
  PATTERN .vs EXCLUDE
  PATTERN amd64 EXCLUDE
  PATTERN Debug EXCLUDE
  PATTERN obj EXCLUDE
)

install(DIRECTORY
    ${CMAKE_CURRENT_SOURCE_DIR}/Lib
    DESTINATION lib/python
    PATTERN plat-* EXCLUDE
    PATTERN msilib EXCLUDE
    PATTERN lib-tk EXCLUDE
    PATTERN curses EXCLUDE
    PATTERN bsddb EXCLUDE
    PATTERN *test EXCLUDE
    PATTERN idlelib EXCLUDE
)

install(EXPORT ${PROJECT_NAME}
  FILE
  ${PROJECT_NAME}.cmake
  NAMESPACE
    ${PROJECT_NAME}::
  DESTINATION
    lib/cmake/${PROJECT_NAME}
)

install(FILES
  ${CMAKE_CURRENT_SOURCE_DIR}/cmake/${PROJECT_NAME}-config.cmake
  ${CMAKE_CURRENT_BINARY_DIR}/${PROJECT_NAME}-config-version.cmake
  DESTINATION
    lib/cmake/${PROJECT_NAME}
)

export(TARGETS ${PROJECT_NAME}
  FILE
  ${CMAKE_CURRENT_BINARY_DIR}/${PROJECT_NAME}-config.cmake
  NAMESPACE ${PROJECT_NAME}::
)
