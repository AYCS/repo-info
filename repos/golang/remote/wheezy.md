## `golang:wheezy`

```console
$ docker pull golang@sha256:1874172a1902a461889ec64dfc6938e272d2d788518e1fd4f06dd9000e23cf68
```

-	Platforms:
	-	linux; amd64

### `golang:wheezy` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.3 MB (201251759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5327166fea4cb558717fb520f9966e827ff0148464d1233b2cacb1b5d319dda`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Jan 2017 20:41:52 GMT
ADD file:a341378be341bc318a57379c0a4b72f182f93ad617f08164343662e789b7244b in / 
# Mon, 16 Jan 2017 20:42:00 GMT
CMD ["/bin/bash"]
# Tue, 17 Jan 2017 00:02:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Jan 2017 00:03:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Jan 2017 00:40:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Fri, 27 Jan 2017 22:37:29 GMT
ENV GOLANG_VERSION=1.7.5
# Fri, 27 Jan 2017 22:37:30 GMT
ENV GOLANG_DOWNLOAD_URL=https://golang.org/dl/go1.7.5.linux-amd64.tar.gz
# Fri, 27 Jan 2017 22:37:30 GMT
ENV GOLANG_DOWNLOAD_SHA256=2e4dd6c44f0693bef4e7b46cc701513d74c3cc44f2419bf519d7868b12931ac3
# Fri, 27 Jan 2017 22:37:40 GMT
RUN curl -fsSL "$GOLANG_DOWNLOAD_URL" -o golang.tar.gz 	&& echo "$GOLANG_DOWNLOAD_SHA256  golang.tar.gz" | sha256sum -c - 	&& tar -C /usr/local -xzf golang.tar.gz 	&& rm golang.tar.gz
# Fri, 27 Jan 2017 22:37:41 GMT
ENV GOPATH=/go
# Fri, 27 Jan 2017 22:37:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Jan 2017 22:37:43 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 27 Jan 2017 22:37:43 GMT
WORKDIR /go
# Fri, 27 Jan 2017 22:37:44 GMT
COPY file:f6191f2c86edc9343569339f101facba47e886e33e29d70da6916ca6b1101a53 in /usr/local/bin/ 
```

-	Layers:
	-	`sha256:d9509b80c497066660d1e7a4e22ba112d025e83f6f7183d53c95bed1513938b7`  
		Last Modified: Mon, 16 Jan 2017 20:55:10 GMT  
		Size: 37.3 MB (37284485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c12b04be6f745f58154eeb7b80403f95b355ca3842d384ffb685acf20432ad`  
		Last Modified: Tue, 17 Jan 2017 00:24:03 GMT  
		Size: 6.8 MB (6823701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0998595e89ba3755e57a2e3cd79c8dd7805959a77828f622fa3b344a73ca5d50`  
		Last Modified: Tue, 17 Jan 2017 00:24:49 GMT  
		Size: 37.4 MB (37442207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1a331769dd25fbec1b25e2327f4fe4f7c91f6929ed225f5634566367acabe90`  
		Last Modified: Wed, 18 Jan 2017 03:46:49 GMT  
		Size: 36.4 MB (36448525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4df815e72d94a6d71a83f8218278394e8776d3262b818e7534e347c606a90382`  
		Last Modified: Fri, 27 Jan 2017 22:50:23 GMT  
		Size: 83.3 MB (83251364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2dee9e705a476ddf3b4b25c5cfb9eab5d167a29301e6f7d2a579b426c73eb50`  
		Last Modified: Fri, 27 Jan 2017 22:49:59 GMT  
		Size: 123.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e93e8fc0976b99b48d1a422d8ae0d446bdc841afa489110f27e08a131fdb7fb9`  
		Last Modified: Fri, 27 Jan 2017 22:49:59 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
