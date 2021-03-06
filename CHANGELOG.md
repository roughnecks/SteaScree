# SteaScree Changelog

## 1.5.4
* Qt 5.9.1.
* Added "JPEG Quality" spinbox for situations, when SteaScree converts image to JPEG. It happens if the input image is too large for Steam Cloud or if it has non-JPEG format. Defaults to 95.
* Slight redesign. Status field is now visible all the time.

## 1.5.3
* Now the app switches to debugging to file automatically, when the it is not ran in Qt Creator.

## 1.5.2
* Added a logic to save debug info to the debug.log file.
* Fixed the bug when the app was crashing, if the Steam user personal name (nickname) was not found in config files. Closes issue #16.
* Removed some unused methods.

## 1.4.1
* Minor UI improvement.

## 1.4.0
* Added Drag&Drop capability.
* Fixed a bug when the app crashed if QImage object was not created if the image file is corrupted or have a wrong extension. Added a new status message if there were such files in the queue and some such files were not copied.
* Fixed misleading status message when userdata directory was not found.
* Some additional minor fixes.

## 1.3.3
* Fixed a bug when personal names were not populated to the respective combobox, if there are multiple config.cfg files were found for a single user. This is completely normal, and now personal name ges extracted from the first found config. Typically, even if there are multiple configs, personal names in them are exactly the same.
* Removed some unused methods.

## 1.3.2
* Implemented check for the encoding process of incoming JPEG files. If it is a progressive, not baseline, pristine copy of file is saved to the filesystem. Otherwise, the file is internally processed by Qt, just like PNG and other supported formats. Closes issue #9.

## 1.3.1
* Well, seems like user switching never worked right. Now it does. Games listed in the combobox change on-the-fly when user ID get changed.

## 1.3.0
* Personal name is now shown in the combobox alongside user ID. Useful when a computer is shared among a number of Steam users.

## 1.2.0
* Added check for an updated version. There is an option to never offer updates.
* Tooltips.
* Minor UI improvement.

## 1.1.0
* Implemented checking of dimensions of provided screenshots. If exceptionally large screenshot is detected, now SteaScree offers user a choice to auto-resize it to the maximum size allowed by Steam (maintaining aspect ratio), skip it or even try to upload it nevertheless. Closes issue #4.
* Some bugs fixed.
* Minor UI improvement.

## 1.0.6
* Fixed a bug when screenshots weren't added to the VDF-file if latest copied screenshot was a dupe.
* Minor UI improvement.

## 1.0.5
* Significantly improved quality of generated thumbnails. Now they are even better and smoother, than those generated by Steam itself. Closes issue #1.

## 1.0.3
* Fixed a bug where screenshots with identical creation timestamps were not copied. Now, if the timestamp overlaps for several screenshots, each of them has identical basename, but different incremental integer after the underscore and before ".jpg" extension.
* Button padding are now set in-code for a more convenient binary building across different platforms.

## 1.0.2
* Initially I thought Steam generates missing thumbnails automatically. This was not the case, so since this release SteaScree takes care of them.
* Minor UI improvement.

## 1.0.1
* Game ID combo box is now editable.
* Minor UI improvement.

## 1.0.0

* Initial public release.
