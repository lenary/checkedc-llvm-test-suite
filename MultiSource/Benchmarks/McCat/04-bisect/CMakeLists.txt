set(PROG bisect)
list(APPEND LDFLAGS -lm)
set(FP_TOLERANCE 0.001)
set(STDIN_FILENAME ${CMAKE_CURRENT_SOURCE_DIR}/bisect_test.in)
llvm_multisource()
