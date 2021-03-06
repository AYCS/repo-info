## `golang:1-alpine3.5`

```console
$ docker pull golang@sha256:82fc218338c9988b90509f8bdf2916583ab6d88be90f357f56915edf77661f02
```

-	Platforms:
	-	linux; amd64

### `golang:1-alpine3.5` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72069092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c18c8c294c1e122cf11562b43504bf679bc29edebaad7bb0f87468a0f3850bd`

```dockerfile
# Tue, 27 Dec 2016 18:17:25 GMT
ADD file:92ab746eb22dd3ed2b87469c719adf3c1bed7302653bbd76baafd7cfd95e911e in / 
# Wed, 04 Jan 2017 21:05:32 GMT
RUN apk add --no-cache ca-certificates
# Fri, 27 Jan 2017 22:38:51 GMT
ENV GOLANG_VERSION=1.7.5
# Fri, 27 Jan 2017 22:38:51 GMT
ENV GOLANG_SRC_URL=https://golang.org/dl/go1.7.5.src.tar.gz
# Fri, 27 Jan 2017 22:38:52 GMT
ENV GOLANG_SRC_SHA256=4e834513a2079f8cbbd357502cccaac9507fd00a1efe672375798858ff291815
# Fri, 27 Jan 2017 22:38:52 GMT
COPY file:b54d7d4313a41e3729d6f4b7aa6e6f33a1e99759cb2a04149fae89f8211c3a65 in / 
# Fri, 27 Jan 2017 22:38:53 GMT
COPY file:c481cf9fa54f8c27f6745f7676ba431e1a320b2ac1246c37e47a3e825746d8e6 in / 
# Fri, 27 Jan 2017 22:39:44 GMT
RUN set -ex 	&& apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 		&& export GOROOT_BOOTSTRAP="$(go env GOROOT)" 		&& wget -q "$GOLANG_SRC_URL" -O golang.tar.gz 	&& echo "$GOLANG_SRC_SHA256  golang.tar.gz" | sha256sum -c - 	&& tar -C /usr/local -xzf golang.tar.gz 	&& rm golang.tar.gz 	&& cd /usr/local/go/src 	&& patch -p2 -i /no-pic.patch 	&& patch -p2 -i /17847.patch 	&& ./make.bash 		&& rm -rf /*.patch 	&& apk del .build-deps
# Fri, 27 Jan 2017 22:39:45 GMT
ENV GOPATH=/go
# Fri, 27 Jan 2017 22:39:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Jan 2017 22:39:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 27 Jan 2017 22:39:47 GMT
WORKDIR /go
# Fri, 27 Jan 2017 22:39:48 GMT
COPY file:f6191f2c86edc9343569339f101facba47e886e33e29d70da6916ca6b1101a53 in /usr/local/bin/ 
```

-	Layers:
	-	`sha256:0a8490d0dfd399b3a50e9aaa81dba0d425c3868762d46526b41be00886bcc28b`  
		Last Modified: Tue, 27 Dec 2016 18:19:22 GMT  
		Size: 1.9 MB (1902063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb658c9d1694c3ba35ef345a0f46dcb9776452cccfa11aa7d41f288392fd6556`  
		Last Modified: Wed, 04 Jan 2017 23:49:03 GMT  
		Size: 352.7 KB (352746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e373d2997a90dc94d8608a4e58f5f5ea049f3c70ed44b21691ec91e35cc0e7`  
		Last Modified: Fri, 27 Jan 2017 22:52:57 GMT  
		Size: 436.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9ea7e9ad7d800515eff7da996b29360bee33c7abc9c1782be3a03fe6f3980a1`  
		Last Modified: Fri, 27 Jan 2017 22:52:57 GMT  
		Size: 780.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956baf7c50c165c2ffdbb0fc91b329d6b59dda6dfa363e9001f25ebf4fa9ee08`  
		Last Modified: Fri, 27 Jan 2017 22:53:19 GMT  
		Size: 69.8 MB (69811594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7bb88a6640082bab8521677dce7419ae097ff376c986ca170b06a6a2c1f5832`  
		Last Modified: Fri, 27 Jan 2017 22:52:57 GMT  
		Size: 123.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:629f5ba9ab0da00dd7b920a45aa7d3a51bd83b3ede3975da9faab03bc93cdafd`  
		Last Modified: Fri, 27 Jan 2017 22:52:57 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
