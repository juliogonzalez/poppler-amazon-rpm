[![Build Status](https://jenkins.juliogonzalez.es/job/poppler-amazon-rpm-build/badge/icon)](https://jenkins.juliogonzalez.es/job/poppler-amazon-rpm-build/)

poppler
=======

Amazon Linux RPMs for poppler <http://poppler.freedesktop.org/>

Based off the RPM package created by Marco Pesenti Gritti and upgraded by Marek Kasik

Tested on Amazon Linux 2014.03


Requirements
------------

* automake
* gcc-c++
* libtool
* cairo-devel >= 1.8.4
* lcms-devel
* libjpeg-devel
* rpmbuild


Building fresh RPMs
-------------------

Clone the repo: 

    git@github.com:juliogonzalez/poppler-amazon-rpm.git
    cd poppler-amazon-rpm

Build the poppler RPMs
---------------------

Build the RPMs:

    ./poppler-amazon-rpm

This will create the main RPM as well as several optional (glib, glib-devel, devel...)

And install:

    rpm -Uvh RPMS/$HOSTTYPE/poppler-0.12.4-3.*.$HOSTTYPE.rpm

You may use the following command:

    ./clean

To clean up the build environment (this will delete RPMs as well)
