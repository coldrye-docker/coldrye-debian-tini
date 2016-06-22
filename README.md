
# coldrye-debian-tini

See https://hub.docker.com/r/coldrye/debian-tini/ for more information.


## Description

This image is mainly meant for containerized services that require a process reaper such as https://github.com/krallin/tini.

tini is defined as the entry point. Derived images can simply declare a CMD which will then be run by tini.


## Image Releases

Images are released for the following debian releases.

- jessie
- testing (stretch)

See https://hub.docker.com/r/coldrye/debian-tini/tags/ for a complete list.

