cmake_minimum_required(VERSION 3.13.0)

project(OtsuThresholdImageFilter)

#-----------------------------------------------------------------------------
# Extension meta-information
set(EXTENSION_HOMEPAGE "http://wiki.slicer.org/slicerWiki/index.php/Documentation/Nightly/Modules/OtsuThresholdImageFilter")
set(EXTENSION_CATEGORY "Legacy.Filtering")
set(EXTENSION_CONTRIBUTORS "Bill Lorensen (GE)")
set(EXTENSION_DESCRIPTION "This filter creates a binary thresholded image that separates an image into foreground and background components. The filter calculates the optimum threshold separating those two classes so that their combined spread (intra-class variance) is minimal (see http://en.wikipedia.org/wiki/Otsu%27s_method). Then the filter applies that threshold to the input image using the itkBinaryThresholdImageFilter. The numberOfHistogram bins can be set for the Otsu Calculator. The insideValue and outsideValue can be set for the BinaryThresholdImageFilter. The filter produces a labeled volume.\n\nThe original reference is: \n\nN.Otsu, &quot;A threshold selection method from gray level histograms,&quot; IEEE Trans.Syst.ManCybern.SMC-9,62-66 1979.")
set(EXTENSION_ICONURL "")
set(EXTENSION_SCREENSHOTURLS "")

#-----------------------------------------------------------------------------
# Extension dependencies
find_package(Slicer REQUIRED)
include(${Slicer_USE_FILE})

#-----------------------------------------------------------------------------
# Extension modules
add_subdirectory(OtsuThresholdImageFilter)
## NEXT_MODULE

#-----------------------------------------------------------------------------
include(${Slicer_EXTENSION_CPACK})
