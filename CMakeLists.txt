set(COMPONENT_SRCS "sqlite3.c esp32.c")
set(COMPONENT_ADD_INCLUDEDIRS "include")
set(COMPONENT_PRIV_INCLUDEDIRS "private_include")
set(COMPONENT_REQUIRES spi_flash)
register_component()

set_source_files_properties(sqlite3.c esp32.c
    PROPERTIES COMPILE_FLAGS
    "-std=gnu99 -g3 -fno-stack-protector -ffunction-sections -fdata-sections -fstrict-volatile-bitfields -mlongcalls -nostdlib -Wpointer-arith -Wno-error=unused-label -Wno-error=unused-value -Wno-error=unused-function -Wno-error=unused-but-set-variable -Wno-error=unused-variable -Wno-error=deprecated-declarations -Wno-unused-parameter -Wno-sign-compare -Wno-old-style-declaration -MMD -c -DF_CPU=240000000L -DESP32 -DCORE_DEBUG_LEVEL=0 -DNDEBUG"
)
