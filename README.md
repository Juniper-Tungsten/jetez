# JetEZ - Easy SDK

**BETA**

JetEZ is an easy (EZ) and lightweight alternative to the official JET SDK with some
limitations. JetEZ creates signed JunOS install packages including any kind of
files described in a [yaml file](https://github.com/Juniper/jetez/blob/master/docs/jet-yaml.md).
This allows to install Python and SLAX scripts but also cross compiled binaries.

The [example app](https://github.com/Juniper/jetez/tree/master/example-app)
shows how to build a GO application for JunOS using JetEZ.

In order to develop and distribute JetEZ applications, you need a package
[signing certificate](https://www.juniper.net/documentation/en_US/jet1.0/topics/task/jet-app-executing-certificate-request-script.html).

```
$ jetez --help
usage: jetez [-h] --source DIR [-v VERSION] -k FILE -c FILE [-j FILE]
             [-b BUILD] [-d]

JetEZ - Easy SDK
----------------

This tool creates a JET install package (.tgz) from source directory using
the parameters from jet.yaml project description file.

optional arguments:
  -h, --help            show this help message and exit
  --source DIR          source directory
  -v VERSION, --version VERSION
                        version string
  -k FILE, --key FILE   path to signing key
  -c FILE, --cert FILE  path to signing cert
  -j FILE, --jet FILE   path to project file (default: <source>/jet.yaml)
  -b BUILD, --build BUILD
                        build directory (default: .build)
  -d, --debug           verbose logging

```

JetEZ supports to generate signed install packages for OCCAM JunOS only (FreeBSD 10 or newer)!
