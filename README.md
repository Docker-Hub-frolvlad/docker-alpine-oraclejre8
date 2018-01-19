[![Docker Stars](https://img.shields.io/docker/stars/frolvlad/alpine-oraclejre8.svg?style=flat-square)](https://hub.docker.com/r/frolvlad/alpine-oraclejre8/)
[![Docker Pulls](https://img.shields.io/docker/pulls/frolvlad/alpine-oraclejre8.svg?style=flat-square)](https://hub.docker.com/r/frolvlad/alpine-oraclejre8/)


OracleJRE 8 Docker image
========================

This image is based on Alpine Linux image, which is only a 5MB image, and contains
[OracleJRE 8](http://www.oracle.com/technetwork/java/javase/overview/index.html).

You must accept the
[Oracle Binary Code License Agreement for Java SE](http://www.oracle.com/technetwork/java/javase/terms/license/index.html)
to use this image (see
[frolvlad/docker-alpine-oraclejdk8/issue-6](https://github.com/frol/docker-alpine-oraclejdk8/issues/6)
for details).

JRE bundle contains lots of unnecessary for Docker image stuff, so it was cleaned up. There are 3
tags: `full` (only src tarballs get removed), `cleaned` (desktop parts get cleaned), `slim`
(everything but jvm is removed). `master` branch refers to `slim` tag, but `latest`
tag points to `cleaned`.

`slim` (`master` branch) download image size is:

[![](https://images.microbadger.com/badges/image/frolvlad/alpine-oraclejre8:slim.svg)](http://microbadger.com/images/frolvlad/alpine-oraclejre8:slim "Get your own image badge on microbadger.com")

`cleaned` (`latest` tag) download image size is:

[![](https://images.microbadger.com/badges/image/frolvlad/alpine-oraclejre8:cleaned.svg)](http://microbadger.com/images/frolvlad/alpine-oraclejre8:cleaned "Get your own image badge on microbadger.com")

`full` download image size is:

[![](https://images.microbadger.com/badges/image/frolvlad/alpine-oraclejre8:full.svg)](http://microbadger.com/images/frolvlad/alpine-oraclejre8:full "Get your own image badge on microbadger.com")

In case you need to compile Java code with Oracle JDK, consider using
[`frolvlad/alpine-oraclejdk8`](https://github.com/frol/docker-alpine-oraclejdk8)
image.


Usage Example
-------------

NOTE: You will need to have a compiled Java application (`Main.class`) to run this.

```bash
$ docker run --rm -v "$(pwd)":/mnt --workdir /mnt frolvlad/alpine-oraclejre8:slim java Main
```

Once you have run this command you will get printed 'Hello World' from Java!
