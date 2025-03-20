# sssh
Sam's SSH Wrapper by sam.k.tan@oracle.com

# Overview

A simple shell script that wraps around SSH. If a connection fails the host key verification, it will prompt the user with the option to delete the existing key.

# Background

I do a lot of demos and I regularly rebuild and reinstall systems using the same pool of IP addresses. I wrote this script to avoid having to manually edit the `known_hosts` file.

# Installation

Just run the following command from your shell and then use `ssh` as per normal.

`alias ssh=<path to sssh folder>/sssh`

# Caveats

Note that `ssh` does not return a specific error code for the host key verification failed condition; instead it returns a 255 code for _any_ error including if you provided the wrong public/private key pairs or if the connection terminated unexpectedly. So this script cannot determine what may have caused a connection to fail, do not automatically delete the host key until you have confirmed exactly what caused the connection error.

/END
