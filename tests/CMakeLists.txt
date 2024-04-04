set(TEST_SOURCES test_a.c test_b.c)

create_test_sourcelist(TESTS test_driver.c ${TEST_SOURCES})
add_executable(my_test_driver test_driver.c ${TEST_SOURCES})

foreach(test_source ${TEST_SOURCES})
    get_filename_component(test_name ${test_source} NAME_WE)
    add_test(NAME ${test_name} COMMAND my_test_driver ${test_name})
endforeach()
