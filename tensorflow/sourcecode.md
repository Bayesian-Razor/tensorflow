# 目录结构

- core/ contains the main C++ code and runtimes. 具体的可以看BUILD的注释.
    - core/ops/:contains the "signatures" of the operations
    - core/kernels/:contains the "implementations" of the operations (including CPU and CUDA kernels)
    - core/framework/:contains the main abstract graph computation and other useful libraries
    - core/platform/:contains code that abstracts away the platform and other imported libraries (protobuf, etc)
- python  contains the python code
    - python/ops/ contain the core python interface
    - python/kernel_tests/ contain the unit tests and lots of example code
    - python/framework/ contains the python abstractions of graph, etc, a lot of which get serialized down to proto and/or get passed to swigged session calls.
    - python/platform/ is similar to the C++ platform, adding lightweight wrappers for python I/O, unit testing, etc.

