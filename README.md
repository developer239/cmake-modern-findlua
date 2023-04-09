# CMake Modern FindLua (Sol2 3.0)

Add this repository as a submodule to your project:

```bash
git submodule add https://github.com/lua/lua.git externals/lua
git submodule add https://github.com/ThePhD/sol2.git externals/sol2
git submodule add https://github.com/developer239/cmake-modern-findlua cmake/lua
```

Find & include:
```cmake
# Find Lua
set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} "${CMAKE_SOURCE_DIR}/cmake/lua/")
find_package(Lua REQUIRED)

# Find Sol2
set(SOL2_INCLUDE_DIRS ${CMAKE_SOURCE_DIR}/externals/sol2/include)
```

Link:
```cmake
target_link_libraries(${PROJECT_NAME} ${LUA_LIBRARY})
target_include_directories(${PROJECT_NAME} PRIVATE ${LUA_INCLUDE_DIR} ${SOL2_INCLUDE_DIRS})
```
