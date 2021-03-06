set(CMAKE_SHARED_LIBRARY_SUFFIX .so)

set(ARROW_SRCS
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/array.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/builder.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/pretty_print.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/array/builder_adaptive.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/array/builder_base.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/array/builder_binary.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/array/builder_decimal.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/array/builder_dict.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/array/builder_nested.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/array/builder_primitive.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/array/builder_union.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/array/concatenate.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/array/dict_internal.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/array/diff.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/array/validate.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/buffer.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/compare.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/extension_type.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/memory_pool.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/pretty_print.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/record_batch.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/result.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/scalar.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/sparse_tensor.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/status.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/table.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/table_builder.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/tensor.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/type.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/visitor.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/csv/converter.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/csv/chunker.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/csv/column_builder.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/csv/options.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/csv/parser.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/csv/reader.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/filesystem/filesystem.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/filesystem/localfs.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/filesystem/mockfs.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/filesystem/path_util.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/filesystem/util_internal.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/json/options.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/json/chunked_builder.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/json/chunker.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/json/converter.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/json/parser.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/json/reader.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/io/buffered.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/io/compressed.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/io/file.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/io/interfaces.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/io/memory.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/testing/util.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/util/basic_decimal.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/util/bit_util.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/util/compression.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/util/cpu_info.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/util/decimal.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/util/int_util.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/util/io_util.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/util/logging.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/util/key_value_metadata.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/util/memory.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/util/string.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/util/string_builder.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/util/task_group.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/util/thread_pool.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/util/trie.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/util/utf8.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/vendored/datetime/tz.cpp
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/ipc/dictionary.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/ipc/feather.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/ipc/json_integration.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/ipc/json_internal.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/ipc/json_simple.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/ipc/message.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/ipc/metadata_internal.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/ipc/reader.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/ipc/options.cc
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/ipc/writer.cc)

set_property(SOURCE util/io_util.cc
           APPEND_STRING
           PROPERTY COMPILE_FLAGS " -Wno-unused-macros -stdlib=libc++")

# make clean will delete the generated file
set_source_files_properties(${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/ipc/Message_generated.h PROPERTIES GENERATED TRUE)
set_source_files_properties(${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/ipc/File_generated.h PROPERTIES GENERATED TRUE)
set_source_files_properties(${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/ipc/Schema_generated.h PROPERTIES GENERATED TRUE)
set_source_files_properties(${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/ipc/Tensor_generated.h PROPERTIES GENERATED TRUE)
set_source_files_properties(${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/ipc/SparseTensor_generated.h PROPERTIES GENERATED TRUE)
set_source_files_properties(${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/ipc/feather_generated.h PROPERTIES GENERATED TRUE)

set(FBS_OUTPUT_FILES
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/ipc/Message_generated.h
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/ipc/File_generated.h
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/ipc/Schema_generated.h
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/ipc/Tensor_generated.h
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/ipc/SparseTensor_generated.h
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/ipc/feather_generated.h)

set(FBS_SRC
    ${CMAKE_BINARY_DIR}/arrow-src/format/Message.fbs
    ${CMAKE_BINARY_DIR}/arrow-src/format/File.fbs
    ${CMAKE_BINARY_DIR}/arrow-src/format/Schema.fbs
    ${CMAKE_BINARY_DIR}/arrow-src/format/Tensor.fbs
    ${CMAKE_BINARY_DIR}/arrow-src/format/SparseTensor.fbs
    ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/ipc/feather.fbs)

include_directories(src)
set(ARROW_BUILD_STATIC ON)
if (PSP_WASM_BUILD)
    set(CMAKE_POSITION_INDEPENDENT_CODE OFF)
elseif(PSP_CPP_BUILD OR PSP_PYTHON_BUILD)
    set(CMAKE_POSITION_INDEPENDENT_CODE ON)
endif()
add_library(arrow STATIC ${ARROW_SRCS})
target_compile_definitions(arrow PUBLIC ARROW_NO_DEPRECATED_API)
target_compile_definitions(arrow PUBLIC ARROW_STATIC)

# will need built boost filesystem and system .lib to work, even though
# perspective itself does not use those dependencies
target_link_libraries(arrow
    ${double-conversion_LIBRARIES}
    ${Boost_FILESYSTEM_LIBRARY}
    ${Boost_SYSTEM_LIBRARY}
    ${ARROW_TEST_LINK_TOOLCHAIN})

find_package(Flatbuffers)

add_custom_command(OUTPUT ${FBS_OUTPUT_FILES}
                   COMMAND ${FLATBUFFERS_COMPILER}
                           -c
                           -o
                           ${CMAKE_BINARY_DIR}/arrow-src/cpp/src/arrow/ipc/
                           ${FBS_SRC}
                   DEPENDS ${FLATBUFFERS_COMPILER}
                   COMMENT "Running flatc compiler on ${FBS_SRC}"
                   VERBATIM)

add_custom_target(arrow_fb_files DEPENDS ${FBS_OUTPUT_FILES})
add_dependencies(arrow arrow_fb_files)
