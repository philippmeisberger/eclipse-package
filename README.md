Eclipse Package
===============

Utility to build Debian package from Eclipse binary distribution.

Installation
------------

There are two ways of installing Eclipse Package: Installation of the stable or latest version. The stable version is distributed through the PM Code Works APT repository and is fully tested but does not contain the latest changes.

### Installation of the stable version

Add PM Codeworks repository

    ~# wget http://apt.pm-codeworks.de/pm-codeworks.list -P /etc/apt/sources.d/

Add PM Codeworks key

    ~# wget -O - http://apt.pm-codeworks.de/pm-codeworks.de.gpg | apt-key add -
    ~# apt-get update

Install the package

    ~# apt-get install eclipse-package

### Installation of the latest version

The latest version contains the latest changes that may not have been fully tested and should therefore not be used productively. It is recommended to install the stable version.

Install required packages for building

    ~# apt-get install git devscripts

Clone this repository

    ~$ git clone https://github.com/philippmeisberger/eclipse-package.git

Build the package

    ~$ cd ./eclipse-package/
    ~$ dpkg-buildpackage -uc -us

Install the package

    ~# dpkg -i ../eclipse-package*.deb

Usage
-----

Download Eclipse .tar.gz archive file from <https://www.eclipse.org/downloads/eclipse-packages/> and execute `make-eclipsepkg` with the downloaded file as argument. The Debian package is built in the current directory.

Installation of Eclipse
-----------------------

Install package

    ~# dpkg -i eclipse*.deb

Finally install missing dependencies

    ~# apt-get install -f

Questions and suggestions
-------------------------

If you have any questions to this project just ask me via email:

<team@pm-codeworks.de>
