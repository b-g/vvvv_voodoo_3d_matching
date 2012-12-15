# 3D Matching with VVVV and Voodoo Camera Tracker

This is the technical documentation of my project [Syn Bio Ads](http://benedikt-gross.de/log/2012/04/synthetic-biology-ads/). It explains how to use the [Voodoo Camera Tracker](http://www.digilab.uni-hannover.de/docs/manual.html) to match realworld filmed footage with a virtual 3D scene in [VVVV](http://vvvv.org/). All necessary steps are explained step by step in the mini tutorial below.

[![Syn Bio Ads - Vimeo Teaser](https://raw.github.com/b-g/vvvv_voodoo_3d_matching/master/img/Syn_Bio_Ads_Vimeo_Teaser.png)](https://vimeo.com/40592029 "Watch: Syn Bio Ads on Vimeo")
[Watch on Vimeo](https://vimeo.com/40592029)


The tutorial assumens that you use provided sample image sequence `/data/frames/frame-000000.png ... ` or that you have prepared one on your.

## Voodoo Camera Tracker

1. `File -> Open -> Sequence` Chose an image sequence and chose the appropriate `Move Type`. I assume in this tutorial that the footage was filmed with a tripod (= camera was still in terms of XYZ and just the rotation of has to be matched). Hence select `rotation (camera on tripod)`.

2. `View -> Camera Parameter, Tap "Position"` Set Roll to 180°, to flip the camera from the upside down default value. Don't ask, I don't have a clue why upside down is default.

![Set Camera Parameters](https://raw.github.com/b-g/vvvv_voodoo_3d_matching/master/img/camera_settings.png "Set Camera Parameters")

3. Press the `Track` button to create a 3D scene.

4. `View -> 3D Scene Viewer` Check the result in 3D. Camera roll should be normal and not upside down.

![3D Scene Viewer](https://raw.github.com/b-g/vvvv_voodoo_3d_matching/master/img/Voodoo_Scene_Geometry.png "3D Scene Viewer")

5. `Save -> Texfile` Check the "Export All" option to get really the whole scene geometry exported.

## VVVV
![3D Scene Viewer VVVV](https://raw.github.com/b-g/vvvv_voodoo_3d_matching/master/img/VVVV.png "3D Scene Viewer VVVV")

6. Open `voodoo_player_vvvv/_root_voodoo_test.v4p` in VVVV
7. Adjust the `footage/frames` and the `voodoo file` parameters to point to the correct locations. Depending of the source footage you might have to change the framerate paramter, the example patch is set to 29.97 FPS.

That's it. From there one you are on your one :) 

Would be nice to see other projects using this technique/patch, feel free to drop an email to me.

## Links
* [Voodoo Camera Tracker](http://www.digilab.uni-hannover.de/docs/manual.html) of the Laboratorium für Informationstechnologie, University of Hannover. Official website, manual and documentation.
* Voodoo Camera Tracker [download](http://www.viscoda.com/index.php/en/voodoo-download)
* [VVVV](http://vvvv.org/)

## Acknowledgements
Special thanks to: The makers of Voodoo Camera Tracker that they made the software free to use for non commercial projects! And [Joreg](http://vvvv.org/users/joreg) who helped me to figure out how to translate the matrix defintions from Voodoo to VVVV speak!