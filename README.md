
[Conan.io](https://conan.io) package for [POSIX Threads for Windows](https://sourceforge.net/projects/pthreads4w/) project

The packages generated with this **conanfile** can be found in [Bintray](https://bintray.com/tum-ubitrack/public-conan/pthreads4w%3Aulricheck).

## For Users: Use this package

### Basic setup

    $ conan install pthreads4w/2.9.1@ulricheck/stable

### Project setup

If you handle multiple dependencies in your project is better to add a *conanfile.txt*

    [requires]
    pthreads4w/2.9.1@ulricheck/stable

    [generators]
    txt

Complete the installation of requirements for your project running:

    $ mkdir build && cd build && conan install ..

Note: It is recommended that you run conan install from a build directory and not the root of the project directory.  This is because conan generates *conanbuildinfo* files specific to a single build configuration which by default comes from an autodetected default profile located in ~/.conan/profiles/default .  If you pass different build configuration options to conan install, it will generate different *conanbuildinfo* files.  Thus, they should not be added to the root of the project, nor committed to git.

## For Packagers: Publish this Package

The example below shows the commands used to publish to ulricheck conan repository. To publish to your own conan respository (for example, after forking this git repository), you will need to change the commands below accordingly.

## Build and package

The following command both runs all the steps of the conan file, and publishes the package to the local system cache.  This includes downloading dependencies from "build_requires" and "requires", and then running the build() method.

    $ conan create ulricheck/stable

## Add Remote

    $ conan remote add tum-ubitrack "https://api.bintray.com/conan/tum-ubitrack/public-conan"

## Upload

    $ conan upload pthreads4w/2.9.1@ulricheck/stable --all -r tum-ubitrack

## Conan Recipe License

NOTE: The conan recipe license applies only to the files of this recipe, which can be used to build and package the software.
It does *not* in any way apply or is related to the actual software being packaged.

[MIT](https://github.com/ulricheck/conan-glog/blob/testing/0.3.5/LICENSE.md)
