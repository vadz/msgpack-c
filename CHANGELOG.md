2015-11-21 version 1.3.0
  * Change the license from the Apache License Version 2.0 to the
    Boost Software License, Version 1.0.(#386)
  * Remove some warnings (#365)
  * Add std::reference_wrapper support(#373, #384)
  * Improve tests (#375, #378, #379, #380)
  * Fix msvc specific problem (#376, #383)
  * Fix typos (#381)
2015-09-04 version 1.2.0
  << breaking change >>
  * Change std::vector<unsigned char> and std::array<unsigned char>
    mapped to BIN instead of ARRAY (#243)
  * Remove redundant copy (#285)

  * Add array_ref to map to ARRAY (#243)
  * Add variant type and adaptor (#349)
  * Add object::convert_if_not_nil() (#357)
  * Fix invalid offset update (#354)
  * Add C++11 support on MSVC2015(#339, #347)
  * Fix and Improve build system (#346, #350, #361, #363)
  * Import Boost.Preprocessor as a part of msgpack-c (#312)
  * Fix OSX with libc++ specific errors (#334, #362)
  * Add customized containers support (#330)
  * Add std::unique_ptr and std::shared_ptr support (#329)
  * Add missing install files (#328)
  * Add shared/static library switching option (#316)
  * Improve no throw description on C++11 (#313)
  * Import Boost.Predef as a part of msgpack-c (#312)
  * Add map based serialize support (#306)
  * Add Boost.Fusion support (#305)
  * Add v4 format RAW support (#304)
  * Fix zbuffer with empty string problem (#303)
  * Add non default constructible class support (#302, #324, #327, #331, #332, #345)
  * Add inline keyword to function (template) (#299)
  * Add EXT type supporting classes (#292, #308)
  * Fix raw_ref != comparison (#290)
  * Add object deep copy (#288)
  * Remove some warnings (#284, #322, #323, #335)
  * Improve compiler version checking (#283)
  * Add return value to object::convert() (#282)
  * Improve move semantic support in C++11 (#279, #353)
  * Add Boost.StringRef support (#278)
  * Improve CI environment (#276, #294, #338)
  * Add converting to JSON (#274, #301)
  * Fix iOS specific problem (#270)
  * Improve doxtgen document generation (#269)
  * Add Boost.Optional support (#268)
  * Fix msvc specific problem (#267, #295)
  * Add base class serialization. (#265, #277)
  * Add and improve examples. (#264, #310, #311, #341, #342, #344)
  * Fix wiki URL. (#263)
2015-04-03 version 1.1.0
  << breaking change >>
  * Remove msgpack_fwd.hpp
  * Improve user types adaptation mechanism (#262)
    Since version 1.0.0, users need to obey the correct include order.
    However, it is very difficult to maintain the correct order in big
    projects. version 1.1.0 removed this order. Users don't need to
    care about include order. Migration guide from 1.0.x to 1.1.0 has
    been written. See https://github.com/msgpack/msgpack-c/wiki

  * Fix vector<bool> size check (#251)
  * Fix inttypes.h inclusion on MSVC (#257)
  * Support documents generation by Doxygen (#259)
  * Remove C99 style variable declaration (#253)
  * Improve documents (https://github.com/msgpack/msgpack-c/wiki)
2015-03-22 version 1.0.1:
  * Fix compilation error on Mac 10.9 (#244)
  * Fix typos in documents (#240)
  * Update CHANGELOG.md for version 1.0.0 (#242)
  * Fix erb templates for the next code generation (#239)

2015-03-10 version 1.0.0:
  * Support msgpack v5 format (str, bin, and ext) https://github.com/msgpack/msgpack/blob/master/spec.md (#142)
  * Support std::tuple, std::forward_list, std::array, std::unordered_set, std::unordered_map on C++11. tr1 unordered containers are still supported (#53, #130, #137, #154, #169)
  * Update msgpack-c as a header-only library on C++ (#142)
  * Move include directory (#142)
  * Update the name of float format family on msgpack::object from 'dec' to 'f64' (#194)
  * Remove existing elements on associative containers when unpacking (#127)
  * Add an API versioning functionality https://github.com/msgpack/msgpack-c/wiki/cpp_versioning (#139)
  * Add C++11 enum class support (#205)
  * Map std::vector<char> and std::array<char> to BIN (#100)
  * Map '\0' teminated char* and char const* to STR (#206)
  * Add the new parameter on unpacking functions and classes to limit msgpack's bytestream size (https://github.com/msgpack/msgpack-c/wiki/cpp_unpacker#limit-size-of-elements) (#175)
  * Add the copy or reference choosing function on unpack() and unpacker (https://github.com/msgpack/msgpack-c/wiki/cpp_unpacker#memory-management)
  * Add the new unpack() overloads for C++11 https://github.com/msgpack/msgpack-c/wiki/cpp_unpacker (#128)
  * Add a msgpack::object::with_zone (deep) copying function (#133, #163)
  * Remove the compile-time defined limit of msgpack nest level on C++ (#218)
  * Add the new unpack() overloads that use an existing zone (#201)
  * Add the range-based for loop support on msgpack object array and map (#203)
  * Add msgpack revision getter function for 'revision' (#237)
  * Support EXT for C (#118, #129)
  * Fix unpacking buffer allocation problem when malformed data is given (#160, #185)
  * Add dll exporting function on MSVC (#162)
  * Fix msgpack::zone::allocate_no_align(). Now it allocates the memory that is not aligned as expected (#171)
  * Improve documents (https://github.com/msgpack/msgpack-c/wiki)
  * Other bug fixes and refactoring: #62, #91, #95, #97, #107, #109, #113, #117, #119, #121, #122, #123, #126, #131, #136, #138, #140, #143, #145, #146, #150, #151, #152, #156, #157, #158, #161, #165, #170, #172, #179, #180, #181, #182, #183, #192, #195, #199, #200, #207, #211, #212, #219, #222, #224, #230, #231, #232, #233, #234, #235

2014-07-02 version 0.5.9:

  * Support std::tr1 unordered containers by default (#51, #63, #68, #69)
  * Remove some warnings (#56)
  * Fix segmentation fault after malloc failures (#58, #59)
  * Fix alloc/dealloc mismatch (#52, #61)
  * Fix sample codes (#60, #64)
  * Support implicit conversion from integer to float/double (#54)
  * Improve documents (#45, #75, #82, #83)
  * Support CMake (#20, #87)
  * Remove Ruby dependencies in bootstrap (#86, #87)
  * Add FILE* buffer (#40)
  * Other bug fixes and refactoring: #39, #73, #77, #79, #80, #81, #84, #90

2013-12-23 version 0.5.8:

  * Move to the new github repository msgpack/msgpack-c
  * Support the new deserialization specification
  * fixes the problem of unpack helpers for array and map with 32bit compilers (#37, #38)
  * Other bug fixes and refactoring: #46, #41, #36, #35, #33, #32, #30, #29, #28, #27, #26, #25, #8, #3
  * Update of documents: #23, #18, #17

2011-08-08 version 0.5.7:

  * fixes compile error problem with llvm-gcc and Mac OS X Lion

2011-04-24 version 0.5.6:

  * #42 fixes double-free problem on msgpack_unpacker_release_zone

2011-02-24 version 0.5.5:

  * eliminates dependency of winsock2.h header
  * fixes msgpack_vc.postbuild.bat file
  * fixes some implicit cast warnings

2010-08-29 version 0.5.4:

  * includes msgpack_vc2008.vcproj file in source package
  * fixes type::fix_int types

2010-08-27 version 0.5.3:

  * adds type::fix_{u,}int{8,16,32,64} types
  * adds msgpack_pack_fix_{u,}int{8,16,32,64} functions
  * adds packer<Stream>::pack_fix_{u,}int{8,16,32,64} functions
  * fixes include paths

2010-07-14 version 0.5.2:

  * type::raw::str(), operator==, operator!=, operator< and operator> are now const
  * generates version.h using AC_OUTPUT macro in ./configure

2010-07-06 version 0.5.1:

  * Add msgpack_vrefbuffer_new and msgpack_vrefbuffer_free
  * Add msgpack_sbuffer_new and msgpack_sbuffer_free
  * Add msgpack_unpacker_next and msgpack_unpack_next
  * msgpack::unpack returns void
  * Add MSGPACK_VERSION{,_MAJOR,_MINOR} macros to check header version
  * Add msgpack_version{,_major,_minor} functions to check library version
  * ./configure supports --disable-cxx option not to build C++ API

2010-04-29 version 0.5.0:

  * msgpack_object_type is changed. MSGPACK_OBJECT_NIL is now 0x00.
  * New safe streaming deserializer API.
  * Add object::object(const T&) and object::operator=(const T&)
  * Add operator==(object, const T&)
  * MSGPACK_DEFINE macro defines msgpack_object(object* obj, zone* z)
  * C++ programs doesn't need to link "msgpackc" library.
