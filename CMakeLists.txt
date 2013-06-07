cmake_minimum_required(VERSION 2.8.9)

project(MyExtension)

#-----------------------------------------------------------------------------
set(EXTENSION_HOMEPAGE "http://www.slicer.org/slicerWiki/index.php/Documentation/Nightly/Extensions/MyExtension")
set(EXTENSION_CATEGORY "Examples")
set(EXTENSION_CONTRIBUTORS "Jean-Christophe Fillion-Robin (Kitware), Steve Pieper (Isomics)")
set(EXTENSION_DESCRIPTION "This is an example of extension bundling a scripted loadable module")
set(EXTENSION_ICONURL "http://viewvc.slicer.org/viewvc.cgi/Slicer4/trunk/Extensions/Testing/MyExtension/MyExtension.png?revision=21747&view=co")
set(EXTENSION_SCREENSHOTURLS "http://wiki.slicer.org/slicerWiki/images/e/e2/Slicer-r19441-MyExtension-screenshot.png")

#-----------------------------------------------------------------------------
find_package(Slicer REQUIRED)
include(${Slicer_USE_FILE})

#-----------------------------------------------------------------------------
add_subdirectory(MyCLIModule)
add_subdirectory(MyLoadableModule)
add_subdirectory(MyScriptedModule)
add_subdirectory(MyEditorEffect)

#-----------------------------------------------------------------------------
include(${Slicer_EXTENSION_CPACK})
