Otsu Threshold Image Filter
===========================

This module is _NOT_ actively supported or maintained (See [#3401](http://na-mic.org/Mantis/view.php?id=3401)).
The associated code has been copied from Slicer [r23589](http://viewvc.slicer.org/viewvc.cgi/Slicer4?view=revision&revision=23589)

Note also the code will _NOT_ compile is its current state. The CMakeLists.txt
will have to be tweaked.

Description
-----------

This filter creates a binary thresholded image that separates an image into foreground and background components. The filter calculates the optimum threshold separating those two classes so that their combined spread (intra-class variance) is minimal (see http://en.wikipedia.org/wiki/Otsu%27s_method).  Then the filter applies that threshold to the input image using the itkBinaryThresholdImageFilter. The numberOfHistogram bins can be set for the Otsu Calculator. The insideValue and outsideValue can be set for the BinaryThresholdImageFilter.  The filter produces a labeled volume.\n\nThe original reference is: \n\nN.Otsu, "A threshold selection method from gray level histograms," IEEE Trans.Syst.ManCybern.SMC-9,62-66 1979.

Contributors
------------

Bill Lorensen (GE)

Acknowledgements
----------------

This command module was derived from Insight/Examples (copyright) Insight Software Consortium

Licensing
---------
Materials in this repository are distributed under the following licenses:

* All software is licensed under BSD style license, with extensions to cover
contributions and other issues specific to 3D Slicer. 
See License.txt file for details.
