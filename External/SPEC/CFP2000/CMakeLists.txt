list(APPEND LDFLAGS -lm)
list(APPEND CPPFLAGS -DSPEC_CPU2000)
if(CMAKE_SIZEOF_VOID_P EQUAL 8)
  list(APPEND CPPFLAGS -DSPEC_CPU2000_LP64)
endif()

macro(cfp2000_subdir BENCHMARK)
  set(BENCHMARK_DIR ${TEST_SUITE_SPEC2000_ROOT}/benchspec/CFP2000/${BENCHMARK})
  set(PROG ${BENCHMARK})
  file(GLOB Source ${BENCHMARK_DIR}/src/*.c ${BENCHMARK_DIR}/src/*.cpp)
  add_subdirectory(${BENCHMARK})
endmacro()

cfp2000_subdir(177.mesa)
cfp2000_subdir(179.art)
cfp2000_subdir(183.equake)
cfp2000_subdir(188.ammp)
