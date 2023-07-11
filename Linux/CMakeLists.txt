cmake_minimum_required(VERSION 3.16.3...3.19.7 FATAL_ERROR)

project(Handy)

#-----------------------------------------------------------------------------
# Extension meta-information
set(EXTENSION_HOMEPAGE "https://www.slicer.org/wiki/Documentation/Nightly/Extensions/Handy")
set(EXTENSION_CATEGORY "Developer Tools")
set(EXTENSION_CONTRIBUTORS "Ernest Namdar (University of Toronto)")
set(EXTENSION_DESCRIPTION "A collection of python modules for Slicer")
set(EXTENSION_ICONURL "https://www.example.com/Slicer/Extensions/Handy.png")
set(EXTENSION_SCREENSHOTURLS "https://www.example.com/Slicer/Extensions/Handy/Screenshots/1.png")
set(EXTENSION_DEPENDS "NA") # Specified as a list or "NA" if no dependencies

#-----------------------------------------------------------------------------
# Extension dependencies
find_package(Slicer REQUIRED)
include(${Slicer_USE_FILE})

#-----------------------------------------------------------------------------
# Extension modules
add_subdirectory(pySlicer)
## NEXT_MODULE

#-----------------------------------------------------------------------------
include(${Slicer_EXTENSION_GENERATE_CONFIG})
include(${Slicer_EXTENSION_CPACK})
