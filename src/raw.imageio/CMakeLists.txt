# Copyright 2008-present Contributors to the OpenImageIO project.
# SPDX-License-Identifier: BSD-3-Clause
# https://github.com/OpenImageIO/oiio

if (LIBRAW_FOUND)
    add_oiio_plugin (rawinput.cpp
                     INCLUDE_DIRS ${LibRaw_INCLUDE_DIR}
                     LINK_LIBRARIES ${LibRaw_r_LIBRARIES}
                     DEFINITIONS "-DUSE_LIBRAW=1" ${LibRaw_r_DEFINITIONS})
else ()
    message (WARNING "Raw plugin will not be built")
endif ()
