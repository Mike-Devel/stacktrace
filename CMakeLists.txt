# Copyright 2018 Mike Dev
# Distributed under the Boost Software License, Version 1.0.
# See accompanying file LICENSE_1_0.txt or copy at http://www.boost.org/LICENSE_1_0.txt
#
#  CAUTION!!!!
#
# This addition to Boost.Stacktrace should be considered experimental and is part
# of an ongoing effort to add CMake support Boost-wide.
#
# IT IS HIGHLY LIKELY THAT THIS FILE WILL CHANGE WITHOUT NOTICE!!!
#
# DO NOT REPLY ON THE CONTENTS OF THIS FILE!!!
#

cmake_minimum_required(VERSION 3.5)
project(BoostStacktrace LANGUAGES CXX)

add_library(boost_stacktrace INTERFACE)
#    src/addr2line.cpp
#    src/basic.cpp
#    src/noop.cpp
#    src/windbg.cpp
#    src/windbg_cached.cpp
#)
add_library(Boost::stacktrace ALIAS boost_stacktrace)

target_include_directories(boost_stacktrace INTERFACE include)

target_link_libraries(
        boost_stacktrace
    INTERFACE
        Boost::array
        Boost::config
        Boost::container_hash
        Boost::core
        Boost::static_assert
        Boost::type_traits
        Boost::winapi
)
