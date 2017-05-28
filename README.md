Eclipse Package
===============

Utility to build Debian package from Eclipse binary distribution.

Installation
------------

Add PM Codeworks repository

    ~# wget http://apt.pm-codeworks.de/pm-codeworks.list -P /etc/apt/sources.d/

Add PM Codeworks key

    ~# wget -O - http://apt.pm-codeworks.de/pm-codeworks.de.gpg | apt-key add -
    ~# apt-get update

Install the package

    ~# apt-get install eclipse-package

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
