set(TEST t_adtf_file_reader) #to not exceed 260 chars on path under windows...

set(TEST_FILES_DIR "${CMAKE_CURRENT_LIST_DIR}/../files")
add_definitions(-DTEST_FILES_DIR="${TEST_FILES_DIR}")


add_executable(${TEST} tester_adtf_file_reader.cpp)
target_link_libraries(${TEST} gtest gtest_main adtf_file)
ifhd_test(${TEST} ${TEST})
set_target_properties(${TEST} PROPERTIES FOLDER test/adtf_file)
