cmake_minimum_required (VERSION 3.22)

if (POLICY CMP0141)
  cmake_policy(SET CMP0141 NEW)
  set(CMAKE_MSVC_DEBUG_INFORMATION_FORMAT "$<IF:$<AND:$<C_COMPILER_ID:MSVC>,$<CXX_COMPILER_ID:MSVC>>,$<$<CONFIG:Debug,RelWithDebInfo>:EditAndContinue>,$<$<CONFIG:Debug,RelWithDebInfo>:ProgramDatabase>>")
endif()

project ("XIVLocPipe")

add_executable (XIVLocPipe "XIVLocPipe.cpp" "XIVLocPipe.h")

set_property(TARGET XIVLocPipe PROPERTY CXX_STANDARD 20)

# TODO: Добавьте тесты и целевые объекты, если это необходимо.
