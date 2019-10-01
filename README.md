# Usage

```bash
git submodule add https://github.com/cad420/external.cmake.git scripts
```

```cmake
# install build scripts
find_package(Git)
execute_process(COMMAND ${GIT_EXECUTABLE} submodule update --init --recursive)
# install external modules
include(scripts/external.cmake)
vm_external_module(
  GIT_REPOSITORY https://github.com/cad420/stbi
  GIT_TAG        master
)

```

```cmake
add_executable(my_exec ${MY_SRC})
vm_target_dependency(my_exec stbi PUBLIC)     # or PRIVATE
```

```cpp
#include <stb/stb_image.h>
#include <stb/stb_image_write.h>

// do whatever you want
```
