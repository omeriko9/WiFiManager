cmake_minimum_required(VERSION 3.5)

idf_component_register(
                       SRCS "WiFiManager.cpp"
                       INCLUDE_DIRS "."
                       PRIV_REQUIRES arduino-esp32
)

# Turn off the format warning for this 3rd-party lib so -Werror can't bite
target_compile_options(${COMPONENT_LIB} PRIVATE -Wno-format)

project(WiFiManager)
