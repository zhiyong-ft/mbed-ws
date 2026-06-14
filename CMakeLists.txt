#[[ Set name of library in lowcase]]
set(INTERNAL_LIBRARY_NAME "mbed-ws-client")

add_library(${INTERNAL_LIBRARY_NAME} INTERFACE)

#[[ Include .h files]]
target_include_directories(${INTERNAL_LIBRARY_NAME} INTERFACE ./source/)

#[[Link library to mbed-core-flags but if the library needs to use RTOS
 features, then have to be add also mbed-rtos-flags]]
target_link_libraries(${INTERNAL_LIBRARY_NAME} INTERFACE mbed-core-flags mbed-rtos-flags)