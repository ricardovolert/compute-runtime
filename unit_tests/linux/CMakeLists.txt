# Copyright (c) 2017, Intel Corporation
#
# Permission is hereby granted, free of charge, to any person obtaining a
# copy of this software and associated documentation files (the "Software"),
# to deal in the Software without restriction, including without limitation
# the rights to use, copy, modify, merge, publish, distribute, sublicense,
# and/or sell copies of the Software, and to permit persons to whom the
# Software is furnished to do so, subject to the following conditions:
#
# The above copyright notice and this permission notice shall be included
# in all copies or substantial portions of the Software.
#
# THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS
# OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
# FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL
# THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR
# OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE,
# ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR
# OTHER DEALINGS IN THE SOFTWARE.

cmake_minimum_required(VERSION 3.2.0 FATAL_ERROR)

project(igdrcl_linux_dll_tests)

if(UNIX)
	set(IGDRCL_SRCS_linux_dll_tests 
		"${IGDRCL_SRCS_linux_dll_tests}"
		"${CMAKE_CURRENT_SOURCE_DIR}/main_linux_dll.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/drm_null_device_tests.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/mock_os_layer.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/mock_os_layer.h"
		"${IGDRCL_SOURCE_DIR}/runtime/os_interface/debug_settings_manager.cpp"
	PARENT_SCOPE)

	set(IGDRCL_SRCS_linux_tests
		"${CMAKE_CURRENT_SOURCE_DIR}/main_linux.cpp"
	PARENT_SCOPE)
endif()
