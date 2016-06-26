# coldrye-debian-tini

[![coldrye/debian-tini](http://dockeri.co/image/coldrye/debian-tini)](https://hub.docker.com/r/coldrye/debian-tini/)


## Description

This packages Debian in various releases based on coldrye/debian ready for deployment of containerized services
with a predefined entry point.


## Image Releases

Images are released for the following debian releases.

- jessie
- testing (stretch)

See https://hub.docker.com/r/coldrye/debian-tini/tags/ for a complete list.


## Additional Packages


### Init

- [krallin/tini](https://github.com/krallin/tini)


## Entry Point

The entry point it set to ["/usr/local/sbin/tini", "-vv", "-q", "--"].

Derived images simply provide a command (CMD) to be executed by ``tini``, e.g.

```
CMD ["/run.sh"]
```

Please note that the executed command must not detach itself.

