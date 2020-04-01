# pkg-puppetdb
This repository packages a puppetdb tarball as a debian package. It is used by a 'backports' jenkins job, defined in https://github.com/exoscale/jobs

## Creating a new tarball
The tarball is created from the [puppetdb repository](https://github.com/exoscale/puppetdb/tree/2.3.x). The `test` and `build` job in the `Jenkinsfile` of that repository describe how the test and tarball can be run and created respectively.
The tarball can then be copied and committed into this repository.

## Create a new version
The version of the debian package is derived from the last entry in the `debian/changelog` file. The version of the last entry will determine the version of the debian package that will be created. You will also need to rename the tarball in the root with a matching version.

The `debian/changelog` file has very strict formatting rules, so it's best to copy over an older entry and modify it.
