# NEWPOS 8210 toolchain

NEW8210 is a Linux based EFT POS device. By default it provides a  set of good application development tools, but at some point the tools started to be a bottleneck. So we have a set of custom tools for rapid application development targeting the mentioned platform.

## GCC Compiler

The default provided GCC compiler version is `4.3.4`, the host platforms are Windows and Linux.

Our custom build is GCC compiler `4.7.3`, the host platforms are Linux and macOS, `C++11` standard is supported to it's fullest.

Additionaly the configuraion files for `ct-ng` are available to build for any host platform.

## Application packaging

The default way of preparing the application packages is the `DownloadTool` application which requires manual effort to build packages and is limited to run on Windows only.

For our needs we have created a Python script which does the packaging automatically based on the configuration file provided. The script can run on any host platform with Python installed.

## Application signing

The default way of signing the executable binaries or other files is the `Signature Tool` JAVA application which is actually limited to run on Windows platform only and requires human interaction as well as extra terminal designated for signing purposes.

So we created our own tool which needs minimum intercation and can run on any platform without the need of having a designated terminal. It is a python script that communicates directly with the  card inserted to a USB ICC reader and signs the file that is provided in a configuration file.

# Contacts

If you are interested in any of the tools that we have, we would be happy to share our experience and help you out with setting up your project.

Email us at aplisgroup@gmail.com

Additionally we could provide assistance with configuring the CI/CD enviroment using our tools. We have our own environment running on Gitlab CI/CD and would be glad to share the video of how the process works.