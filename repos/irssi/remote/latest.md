## `irssi:latest`

```console
$ docker pull irssi@sha256:4c3e0e9f904ec00104d6e491e9324f8460741de35850be53667919bf68f12b4d
```

-	Platforms:
	-	linux; amd64

### `irssi:latest` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.4 MB (97415571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efaae7dab9aeb8e63f95ff8a4140ba9131a1775d7eace9f5d9c09d82183692bb`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Jan 2017 20:35:09 GMT
ADD file:89ecb642d662ee7edbb868340551106d51336c7e589fdaca4111725ec64da957 in / 
# Mon, 16 Jan 2017 20:35:16 GMT
CMD ["/bin/bash"]
# Tue, 17 Jan 2017 00:47:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libglib2.0-0 		libwww-perl 		perl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Jan 2017 00:47:28 GMT
ENV HOME=/home/user
# Tue, 17 Jan 2017 00:47:29 GMT
RUN useradd --create-home --home-dir $HOME user 	&& mkdir -p $HOME/.irssi 	&& chown -R user:user $HOME
# Tue, 17 Jan 2017 00:47:29 GMT
ENV LANG=C.UTF-8
# Tue, 07 Feb 2017 19:55:57 GMT
ENV IRSSI_VERSION=1.0.1
# Tue, 07 Feb 2017 19:56:53 GMT
RUN buildDeps=' 		autoconf 		automake 		bzip2 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		make 		pkg-config 		xz-utils 	' 	&& set -x 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz 	&& wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1 	&& gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz 	&& rm -r "$GNUPGHOME" /tmp/irssi.tar.xz.asc 	&& mkdir -p /usr/src/irssi 	&& tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1 	&& rm /tmp/irssi.tar.xz 	&& cd /usr/src/irssi 	&& ./configure 		--enable-true-color 		--with-bot 		--with-proxy 		--with-socks 	&& make -j$(nproc) 	&& make install 	&& rm -rf /usr/src/irssi 	&& apt-get purge -y --auto-remove $buildDeps
# Tue, 07 Feb 2017 19:56:53 GMT
WORKDIR /home/user
# Tue, 07 Feb 2017 19:56:54 GMT
VOLUME [/home/user/.irssi]
# Tue, 07 Feb 2017 19:56:54 GMT
USER [user]
# Tue, 07 Feb 2017 19:56:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:5040bd2983909aa8896b9932438c3f1479d25ae837a5f6220242a264d0221f2d`  
		Last Modified: Mon, 16 Jan 2017 20:43:26 GMT  
		Size: 51.4 MB (51361210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06777db5e105cc0415b734dfe2028b029422171ff3f51dc9a8afeab8e7676ce5`  
		Last Modified: Wed, 18 Jan 2017 04:13:09 GMT  
		Size: 32.3 MB (32253970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48011afb85960c91df7ab455cb886d7f86b6214d17f854f972dc94929025adfa`  
		Last Modified: Wed, 18 Jan 2017 04:12:57 GMT  
		Size: 4.4 KB (4362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a990b2ff435a957ed6e6c70c2d0c6acc22afaa442397464b4db5a359a1dffa7c`  
		Last Modified: Tue, 07 Feb 2017 19:58:04 GMT  
		Size: 13.8 MB (13796029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
