# deep_ptr : a deep-copying pointer class for C++

A deep copying smart pointer that uses type erasure to call the copy
constructor of derived types would allow the compiler-generated copy
constructor to copy an object composed of polymorphic components correctly. 

When component objects are owned by deep-copying pointers, they will be copied
correctly without any extra code being required - an end user can use the
compiler-defaults for copy, assign, move and move-assign.

See <https://groups.google.com/a/isocpp.org/forum/#!topic/std-proposals/YnUvKJATgD0>
for discussion/design.

A proposal will follow (work is currently in progress).

## Submodules
Tests use the 'catch' test framework: <https://github.com/philsquared/Catch.git>

To get the submodule run:
  
    git submodule update --init

## Building
The build uses cmake. To build and run tests, run the follwing from the console:

    cmake . && cmake --build . && ctest
