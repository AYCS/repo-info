## `perl:latest`

```console
$ docker pull perl@sha256:645e95dbfe327af60265bad563e9d7936af785c02bbc2d9645d67037b0fc5aa7
```

-	Platforms:
	-	linux; amd64

### `perl:latest` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.9 MB (254946619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d4b5b34b6df5df63ea686aa287280463e943cb6dd871c90b7c443c4f714afc7`
-	Default Command: `["perl5.24.0","-de0"]`

```dockerfile
# Mon, 16 Jan 2017 20:35:09 GMT
ADD file:89ecb642d662ee7edbb868340551106d51336c7e589fdaca4111725ec64da957 in / 
# Mon, 16 Jan 2017 20:35:16 GMT
CMD ["/bin/bash"]
# Tue, 17 Jan 2017 00:00:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Jan 2017 00:01:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Jan 2017 00:04:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libncurses-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Jan 2017 01:14:49 GMT
MAINTAINER Peter Martini <PeterCMartini@GMail.com>
# Wed, 18 Jan 2017 01:14:53 GMT
RUN apt-get update     && apt-get install -y curl procps     && rm -fr /var/lib/apt/lists/*
# Wed, 18 Jan 2017 01:14:54 GMT
RUN mkdir /usr/src/perl
# Wed, 18 Jan 2017 01:14:54 GMT
COPY file:21749e9b9dd48119d6468e64e9fc7ba979cd3bac662c7c9978b4a6d3262fa809 in /usr/src/perl/ 
# Wed, 18 Jan 2017 01:14:55 GMT
WORKDIR /usr/src/perl
# Wed, 18 Jan 2017 01:20:08 GMT
RUN curl -SL https://cpan.metacpan.org/authors/id/R/RJ/RJBS/perl-5.24.0.tar.bz2 -o perl-5.24.0.tar.bz2     && echo '298fa605138c1a00dab95643130ae0edab369b4d *perl-5.24.0.tar.bz2' | sha1sum -c -     && tar --strip-components=1 -xjf perl-5.24.0.tar.bz2 -C /usr/src/perl     && rm perl-5.24.0.tar.bz2     && cat *.patch | patch -p1     && ./Configure -Duse64bitall -Duseshrplib  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://raw.githubusercontent.com/miyagawa/cpanminus/master/cpanm     && chmod +x cpanm     && ./cpanm App::cpanminus     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /tmp/*
# Wed, 18 Jan 2017 01:20:09 GMT
WORKDIR /root
# Wed, 18 Jan 2017 01:20:09 GMT
CMD ["perl5.24.0" "-de0"]
```

-	Layers:
	-	`sha256:5040bd2983909aa8896b9932438c3f1479d25ae837a5f6220242a264d0221f2d`  
		Last Modified: Mon, 16 Jan 2017 20:43:26 GMT  
		Size: 51.4 MB (51361210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce5728aad85a763fe3c419db16885eb6f7a670a42824ea618414b8fb309ccde`  
		Last Modified: Tue, 17 Jan 2017 00:19:41 GMT  
		Size: 18.5 MB (18535441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76610ec20bf5892e24cebd4153c7668284aa1d1151b7c3b0c7d50c579aa5ce75`  
		Last Modified: Tue, 17 Jan 2017 00:20:34 GMT  
		Size: 42.5 MB (42502406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f3db4b5710849a53bc2eea0b6f0895c494d751c38c597404d805da82b3f37c`  
		Last Modified: Tue, 17 Jan 2017 00:26:00 GMT  
		Size: 129.8 MB (129823115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd98f3830f39f3210769228a69ee1e89354e3d0e25f035db1b2b4b5d35d40bbe`  
		Last Modified: Wed, 18 Jan 2017 07:16:41 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfd49e437fdcd67ead51686fb18040108968f82d7b7600033ccc57c6ae233d12`  
		Last Modified: Wed, 18 Jan 2017 07:16:40 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:557c98e4affd8112b80e1c5951a8b112181d6b3fad701fef78dba500c9105477`  
		Last Modified: Wed, 18 Jan 2017 07:16:41 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc4338a9cd414182adca529ddfc8cc3e89693070aa730d3a7127c42e02ab7c2`  
		Last Modified: Wed, 18 Jan 2017 07:16:49 GMT  
		Size: 12.7 MB (12723755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
