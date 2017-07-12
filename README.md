Main Author: Cloud Tsai

Copyright 2017, Dell, Inc.

Virtual Device Service 2- The Virtual Device Service 2 can simulate different kinds of devices to generate Events and Readings to Core Data Micro Service.  Furthermore, users can send commands and get responses through Command and Control Micro Service.  It’s useful when executing functional or performance tests without any real devices.
This version of Virtual Device Service is implemented based on Device Service SDK.

# Building the docker image - general information

In order to successfully build the docker image a few things are required to
be accessible from within the docker-files directory. These are:

 * service compiled and named device-virtual.jar
 * bacnet_sample_profiles
 * modbus_sample_profiles

Given the above one needs to build the service first and then copy the above
files and directories to the docker-files directory. Note that ln -s will not
work.

When the above is done the image shall build.

# Building for ARM

There is docker-files/Dockerfile.armhf available that should be used for
building the docker image for ARM architecture.

Use it as you would any other dockerfile:

```
$ docker build . -f Dockerfile.armhf
```
