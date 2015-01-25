Copyright (c) 2014 FirstZimbabweCoin Developers <br />
Copyright (c) 2009-2012 Bitcoin Developers

Distributed under the MIT/X11 software license, see the accompanying file
license.txt or http://www.opensource.org/licenses/mit-license.php.  This
product includes software developed by the OpenSSL Project for use in the
OpenSSL Toolkit (http://www.openssl.org/).  This product includes cryptographic
software written by Eric Young (eay@cryptsoft.com) and UPnP software written by
Thomas Bernard.

<h1>Build OSX</h1>

See readme-qt.rst for instructions on building FirstZimbabweCoin QT, the
graphical user interface.

All of the commands should be executed in Terminal.app.. it's in
/Applications/Utilities

You need to install XCode with all the options checked so that the compiler and
everything is available in /usr not just /Developer I think it comes on the DVD
but you can get the current version from http://developer.apple.com

1.  Clone the github tree to get the source code:

        git clone git@github.com:rat4/FirstZimbabweCoin.git FirstZimbabweCoin

2.  Download and install MacPorts from http://www.macports.org/

  1. (for 10.7 Lion)

            Edit /opt/local/etc/macports/macports.conf and uncomment "build_arch i386"

3.  Install dependencies from MacPorts

    sudo port install boost db48 openssl miniupnpc

Optionally install qrencode (and set USE_QRCODE=1):

    sudo port install qrencode

4.  Now you should be able to build FirstZimbabweCoind:

    cd FirstZimbabweCoin/src
    make -f makefile.osx

Run:

    ./FirstZimbabweCoind --help  # for a list of command-line options.

Run:

    ./FirstZimbabweCoind -daemon # to start the FirstZimbabweCoin daemon.

Run:

    ./FirstZimbabweCoind help # When the daemon is running, to get a list of RPC commands