set(PLUGLIB_SRC
    "aaplane.h"
    "always.h"
    "BITTYPE.H"
    "bool.h"
    "borlandc.h"
    "chunkio.cpp"
    "chunkio.h"
    "errclass.h"
    "EULER.CPP"
    "EULER.H"
    "hashcalc.h"
    "hsv.cpp"
    "hsv.h"
    "iostruct.h"
    "jshell.cpp"
    "matrix3d.cpp"
    "matrix3d.h"
    "matrix4.cpp"
    "matrix4.h"
    "nodefilt.cpp"
    "nodefilt.h"
    "nodelist.cpp"
    "nodelist.h"
    "noinit.h"
    "palette.cpp"
    "palette.h"
    "plane.h"
    "PROGRESS.H"
    "rawfile.cpp"
    "rawfile.h"
    "realcrc.cpp"
    "realcrc.h"
    "rgb.cpp"
    "rgb.h"
    "uarray.h"
    "Vector.CPP"
    "Vector.H"
    "vector2.h"
    "vector3.h"
    "vector3i.h"
    "vector4.h"
    "visualc.h"
    "w3d_file.h"
    "w3dquat.cpp"
    "w3dquat.h"
    "watcom.h"
    "win.h"
    "wwfile.h"
    "wwmath.cpp"
    "wwmath.h"
    "WWmatrix3.cpp"
    "WWmatrix3.h"
)

add_library(core_pluglib STATIC)
set_target_properties(core_pluglib PROPERTIES OUTPUT_NAME pluglib)

target_sources(core_pluglib PRIVATE ${PLUGLIB_SRC})

target_link_libraries(core_pluglib PUBLIC
    core_utility
)

target_link_libraries(core_pluglib PRIVATE
    maxsdk
)
