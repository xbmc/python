add_library(_ctypes SHARED
  ${CMAKE_CURRENT_SOURCE_DIR}/_ctypes.c
  ${CMAKE_CURRENT_SOURCE_DIR}/callbacks.c
  ${CMAKE_CURRENT_SOURCE_DIR}/callproc.c
  ${CMAKE_CURRENT_SOURCE_DIR}/cfield.c
  ${CMAKE_CURRENT_SOURCE_DIR}/ctypes.h
  ${CMAKE_CURRENT_SOURCE_DIR}/ctypes_dlfcn.h
  ${CMAKE_CURRENT_SOURCE_DIR}/malloc_closure.c
  ${CMAKE_CURRENT_SOURCE_DIR}/stgdict.c
  ${CMAKE_CURRENT_SOURCE_DIR}/libffi_msvc/ffi.c
  ${CMAKE_CURRENT_SOURCE_DIR}/libffi_msvc/ffi.h
  ${CMAKE_CURRENT_SOURCE_DIR}/libffi_msvc/ffi_common.h
  ${CMAKE_CURRENT_SOURCE_DIR}/libffi_msvc/fficonfig.h
  ${CMAKE_CURRENT_SOURCE_DIR}/libffi_msvc/ffitarget.h
  ${CMAKE_CURRENT_SOURCE_DIR}/libffi_msvc/prep_cif.c
  ${CMAKE_CURRENT_SOURCE_DIR}/libffi_msvc/types.c
)

if(${CMAKE_SIZEOF_VOID_P} EQUAL 4)
  target_sources(_ctypes PRIVATE
    ${CMAKE_CURRENT_SOURCE_DIR}/libffi_msvc/win32.c
  )
else()
  target_sources(_ctypes PRIVATE
    ${CMAKE_CURRENT_SOURCE_DIR}/libffi_msvc/win64.asm
  )
endif()