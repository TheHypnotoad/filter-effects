Filter Effects
==============

A Nokia example demonstrating the use of the different filters of Nokia Imaging
SDK with camera photos. This example app uses the camera and displays the
viewfinder for taking a picture. The taken photo is then processed with the
predefined filters. The filter properties can be manipulated and the changes can
be seen in the preview image immediately. The processed image can be saved in
JPEG format into the camera roll album. You can also select an existing photo
and apply an effect to it. 

This example application is hosted in GitHub:
https://github.com/nokia-developer/filter-effects

For more information on implementation, visit Nokia Lumia
Developer's Library:
http://developer.nokia.com/Resources/Library/Lumia/nokia-imaging-sdk/sample-projects/filter-effects.html


1. Important classes
-------------------------------------------------------------------------------

* `AbstractFilter`: The base class for the filters implemented by the
application. This abstract class implements the preview image handling and
defines the methods required to be implemented by the derived classes. The
filters implemented by this example are:
 * `CarShowFilter`: Lomo filter
 * `CartoonFilter`: Cartoon filter
 * `EightiesPopSongFilter`: Sketch filter
 * `SadHipsterFilter`: Antique and lomo filter
* `DataContext`: A singleton class holding the references to image data.
* `FilterPreviewPage`: Manages the filters and implements image management
including saving the image into the camera roll.
* `FilterPropertiesControl`: A custom user control for adjusting the filter
settings. Each filter is responsible for populating the control compontents.
This class is but a place holder with minimal implementation.
* `MainPage`: Implements the camera view finder and fetching saved images from
the file system.


2. Compatibility
-------------------------------------------------------------------------------

Compatible with Windows Phone 8 phones. The project is dependent on Nokia
Imaging SDK. The example has been tested with Nokia Lumia 920 and Nokia Lumia
620. Developed with Visual Studio 2012 Express for Windows Phone 8.

2.1 Required capabilities
-------------------------

* `ID_CAP_ISV_CAMERA`
* `ID_CAP_MEDIALIB_PHOTO`
* `ID_CAP_NETWORKING`

2.2 Known issues
----------------

None.


3. Building, installing, and running the application
-------------------------------------------------------------------------------

3.1 Preparations
----------------

Make sure you have the following installed:
* Windows Phone SDK 8.0

3.2 Using the Windows Phone 8 SDK
---------------------------------

1. Open the SLN file:
   File > Open Project, select the file FilterEffects.sln
2. Select the target 'Device'.
3. Press F5 to build the project and run it on the device.

3.3 Deploying to Windows Phone 8
--------------------------------

Please see official documentation for deploying and testing applications on
Windows Phone devices:
http://msdn.microsoft.com/en-us/library/gg588378%28v=vs.92%29.aspx


4. License
-------------------------------------------------------------------------------

See the license text file delivered with this project. The license file is also
available online at
https://github.com/nokia-developer/filter-effects/blob/master/Licence.txt


5. Related documentation
-------------------------------------------------------------------------------

* Nokia Lumia Developer's Library:
  http://www.developer.nokia.com/Resources/Library/Lumia
* Wiki article: Optimizing Imaging SDK use for rapidly changing filter
  parameters:
  http://developer.nokia.com/Community/Wiki/Optimizing_Imaging_SDK_use_for_rapidly_changing_filter_parameters


6. Version history
-------------------------------------------------------------------------------

* 1.2 Updated to support the latest version of the Nokia Imaging SDK. Theme
      support added.
* 1.1 Performance optimisations added based on Yan's wiki article (see related
      documentation)
* 1.0.1 Invalid reference paths fixed and some updates to app icons
* 1.0 First release
* 0.8 First release candidate
