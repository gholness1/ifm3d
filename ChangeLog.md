## Changes between ifm3d 0.3.1 and 0.3.2

* CMake build scripts now look for opencv in tools module since the image
  buffer header includes an opencv header

## Changes between ifm3d 0.3.0 and 0.3.1

* Fixed regression on 14.04 - no compiler support for std::put_time (#3)

## Changes between ifm3d 0.2.0 and 0.3.0

* Support for NTP (on O3X)
* Added simple viewer sub-command to the `ifm3d` command-line program. This
  viewer will render the point cloud and color each pixel with the normalized
  amplitude value registered to that point.

## Changes between ifm3d 0.1.0 and 0.2.0

* Added software trigger support to O3X
* Added support for ifm Vision Assistant compatible import/export functions for
  O3X cameras
* Optimization to `ifm3d` cmd line tool when passed either `--help` or
  `version`. It will no longer try to connect to the device first, which makes
  this much more responsive and convenient for when no h/w is plugged in.
* Added the ability to explicitly choose OpenCV 2.4 or OpenCV 3 at
  cmake/compile time.
* Modifications to enable the library to build under Ubuntu 14.04 (C++11
  instead of C++14 and gcc 4.8. Big thanks to @aaronhoy at Fetch Robotics for
  [his work](https://github.com/aaronhoy/ifm3d/commit/b2e894e3a4f4afc227b7d33993f0a85e4078d513)
* Added a new build-time utility
  [ifm3d-dpkg-deps.py](cmake/utils/ifm3d-dpkg-deps.py.in) to auto-generate
  debian dependencies for the binary packages. This is needed because, for how
  we are building multiple shared libraries across multiple debian packages,
  cmake's stanard wrapper to `dpkg-shlibdeps` does not work for us (for several
  reasons).

## This file has started tracking ifm3d at 0.1.0

* Initial (alpha) release
