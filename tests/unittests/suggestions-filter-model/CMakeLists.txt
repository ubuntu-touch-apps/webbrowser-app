set(TEST tst_SuggestionsFilterModelTests)
add_executable(${TEST} tst_SuggestionsFilterModelTests.cpp)
include_directories(${webbrowser-app_SOURCE_DIR})
qt5_use_modules(${TEST} Test)
target_link_libraries(${TEST} webbrowser-app-models)
add_test(${TEST} ${CMAKE_CURRENT_BINARY_DIR}/${TEST} -xunitxml -o ${TEST}.xml)
