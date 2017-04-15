### Note this repo is lGPL due to Pastec being lGPL.

This repo is my notes on compiling a copy of pastec, first on the mac and then on iOS.

---

### Getting started on the Mac

* `git clone [this-repo]`
* `cd compile_pastec`
* `git submodules init`
* `git submodules update`

You need cmake.

* `brew install cmake`

Go into `pastec` and run `cmake .`

* `cd pastec`
* `cmake .`

Need `OpenCV`?

* `brew tap homebrew/science`
* `brew install opencv`

Need `libmicrohttpd` and `libjsoncpp`?

* `brew install libmicrohttpd`
* `brew install jsoncpp`

I had some trouble with `jsoncpp`, ended up doing: `cmake -D LIBJSONCPP_INCLUDE_DIR=/usr/local/Cellar/jsoncpp/1.8.0 .` which hooked it up to the right place.

Let's keep a mac build around

* `mkdir ../build/`
* `mkdir ../build/mac`
* `cp pastec ../build/mac`

### iOS

* OpenCV: http://docs.opencv.org/2.4/doc/tutorials/introduction/ios_install/ios_install.html or https://cocoapods.org/?q=opencv
* `libmicrohttpd` : https://github.com/cpp-ethereum-ios/libmicrohttpd-iOS
* `jsonpp` https://cocoapods.org/pods/jsoncpp
