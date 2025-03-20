# sssh
Sam's SSH Wrapper

# Overview

A simple shell script that wraps around SSH. If a connection fails the host key verification, it will prompt the user with the option to delete the existing key.

# Background

I do a lot of demos and I regularly rebuild and reinstall systems using the same pool of IP addresses. I wrote this script to avoid having to manually edit the `known_hosts` file.

# Installation

Just run the following command from your shell and then use `ssh` as per normal.

`alias ssh=<path to sssh folder>/sssh`
