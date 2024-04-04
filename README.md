cmake -S . -B build -DENABLE_TESTING:BOOL=ON

cmake --build build --target my_test_driver

cmake --build build --target test
