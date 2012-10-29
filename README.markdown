# WaxSim

A wrapper around iPhoneSimulatorRemoteClient, to install and run apps in the iOS simulator.

## Installation

Compiling and installing uses the `xcodebuild` command. By default it installs the app in `/usr/local/bin`.

`xcodebuild install`

To customize the installation location use the `DSTROOT` and `INSTALL_PATH` build variables. For example, to compile into a local `bin` directory:

`xcodebuild install DSTROOT=. INSTALL_PATH=/bin`

## Use

`waxsim "/path/to/MyApp.app"`

If you want to define which family of iOS device to use:

`waxsim -f "ipad" "/path/to/MyApp.app"`

To see all usage options, type `waxsim` with no arguments:

```
usage: waxsim [options] app-path
example: waxsim -s 2.2 /path/to/app.app
Available options are:
  -s sdkVersion number of sdk to use (-s 3.1)
  -f familyDevice to use (-f ipad)
  -e VAR=valueEnvironment variable to set (-e CFFIXED_HOME=/tmp/iphonehome)
  -a DependenciesAvailable SDKs
  -v pathOutput video recording at path
  -h DependenciesPrints out this wonderful documentation!
```

## Dependencies

You need to be runnin Mac OS X running a recent version of Xcode. Testing with Xcode 4.5.

