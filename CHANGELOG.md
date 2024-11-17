# Changelog

## 4.2.0
- Added possibility to show images directly from editor
- Added support for batch dimension (premium)
- Added multiple image displaying (premium)
- Added support for deeper pointers in C++ (premium)
- Settings are now stored for projects separately
- Enabled keras variables (premium)
- Fixed remote debugger image showing
- Added icon to plugin actions
- Added support for 2024.3.x release

## 4.1.0
- Added support for torchvision tensors
- Implemented image rendering in the background (no more GUI freeze)
- Optimized image rendering (2x faster)
- Improved progress bar when loading image
- Fixed thread context already set when saving image
- Fixed wrong zoom factor when transposing image
- Added support for 2024.2.x release

## 4.0.1
- Added support for PIL, PyTorch, Tensorflow
- Added apply colormap action
- Added hexadecimal display
- Added transpose image action (HWC <-> CHW)
- Added separate channel displaying
- Added force view as image action in C++
- Added help and get premium actions
- Allowed showing Mat in C++ and Java containers
- Reworked the behaviour for squeezable arrays
- Fixed messages in case of exceptions
- Support for 2024.1.x release

## 3.3.1
- Support for 2023.3.x release
- Support for CLion Nova
- Better message in case of out of memory

## 3.3.0
- Support for 2023.2.x release
- Added show settings action in the image window
- Fixed wrong extension when saving image to disk
- Icons for new IU

## 3.2.0
- Support for 2023.1.x release
- Move dialog windows a little to avoid overlapping with others
- Fixed shortcuts for popup actions
- Fixed inaccurate values for pixel close to the border
- Fixed disappearing toolbar when too small window size

## 3.1.0
- Added context menu and copy action
- Fixed save dialog showing under the image popup
- Fixed shortcuts for actions in the image dialog
- Fixed non-expiring startup notification

## 3.0.2
- Support for 2022.3.x release

## 3.0.1
- Support for 2022.2.x release

## 3.0.0
- Added support for Java, Kotlin and Android (Intellij, AndroidStudio)
- Improved experience when cancelling variable downloads

## 2.1.2
- Added support for Jupyter Notebooks vars

## 2.1.1
- Support for 2022.1.x release

## 2.1.0
- Added support for RGB images
- Added option to normalize the image
- Added option to save the image
- Remember window last position and size
- Removed pixel info when cursor exits the image

## 2.0.3
- Support for 2021.3.x release

## 2.0.2
- Added support for pointers, const variables, references and members (C++)

## 2.0.1
- Fixed syntax error while using remote interpreter

## 2.0.0
- Added support for C++ (CLion)
- Showing better variable name
- Fixed outdated notification content

## 1.4.1
- Fixed plugin crash when using OS scaling (thanks Liviu!)

## 1.4.0
- Added info about cursor position and pixel value under the cursor
- Added info about image data type
- Fixed issue with pixel disappearing when zooming big images

## 1.3.5
- Support for 2021.2.x release

## 1.3.4
- Fixed the issue with displaying image when running with Pytest

## 1.3.3
- Fixed "Can't display image" in python console once again

## 1.3.2
- Fixed issue when run configuration has different interpreter than project sdk
- Fixed update notification
- Added possibility to disable update notification
- Support for 2021.1 IDEs

## 1.3.1
- Fixed random "Can't display image" in python console
- Better plugin description and change notes

## 1.3.0
- Added possibility to show array in dialog instead of popup
- Added possibility to show array when indices are updated
- Added update notification
- Fixed issue with showing array in python console

## 1.2.1
- Fixed issue with showing array when value policy is "on demand"
- Greyed out action for not supported dtypes

## 1.2.0
- Added support for remote python interpreter
- Display arrays with expanded dims

## 1.1.0
- Remember image viewer options
- Better way to show issues
- Added progress bar if loading is long

## 1.0.0
- Initial stable release of the plugin
