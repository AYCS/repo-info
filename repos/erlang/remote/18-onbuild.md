## `erlang:18-onbuild`

```console
$ docker pull erlang@sha256:c7c629972fe42ec0ac623320c19981f53dfae7aaf19b6d4c173f380543781247
```

-	Platforms:
	-	linux; amd64

### `erlang:18-onbuild` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.2 MB (302242066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48374acadfff36fd588dbc2dd6a86661957e3470ea22c581ea2b456853f38faf`
-	Default Command: `["rebar3","shell"]`

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
# Fri, 03 Feb 2017 19:22:50 GMT
ENV OTP_VERSION=18.3.4.5
# Fri, 03 Feb 2017 19:28:22 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-$OTP_VERSION.tar.gz" 	&& OTP_DOWNLOAD_SHA256="a27b8ff057f77305e7c9f2dbcd002232856438fd1fdf3822edd27c6f77a60ca1" 	&& runtimeDeps='libodbc1 			libsctp1' 	&& buildDeps='unixodbc-dev 			libsctp-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256 otp-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/otp-src 	&& tar -xzf otp-src.tar.gz -C /usr/src/otp-src --strip-components=1 	&& rm otp-src.tar.gz 	&& cd /usr/src/otp-src 	&& ./otp_build autoconf 	&& ./configure --enable-sctp 	&& make -j$(nproc) 	&& make install 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/otp-src /var/lib/apt/lists/*
# Fri, 03 Feb 2017 19:28:22 GMT
CMD ["erl"]
# Fri, 03 Feb 2017 19:28:22 GMT
ENV REBAR_VERSION=2.6.4
# Fri, 03 Feb 2017 19:28:26 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION##*@}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src
# Fri, 03 Feb 2017 19:28:26 GMT
ENV REBAR3_VERSION=3.3.4
# Fri, 03 Feb 2017 19:28:53 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION##*@}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a7ad962617f1e91347257b7c6c69612aee564e1172b8507947e173b8846a204d" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src
# Fri, 03 Feb 2017 19:34:35 GMT
RUN mkdir -p /usr/src/app
# Fri, 03 Feb 2017 19:34:35 GMT
WORKDIR /usr/src/app
# Fri, 03 Feb 2017 19:34:35 GMT
ONBUILD COPY rebar.config /usr/src/app/
# Fri, 03 Feb 2017 19:34:36 GMT
ONBUILD RUN rebar3 update
# Fri, 03 Feb 2017 19:34:36 GMT
ONBUILD COPY . /usr/src/app
# Fri, 03 Feb 2017 19:34:36 GMT
ONBUILD RUN rebar3 release
# Fri, 03 Feb 2017 19:34:37 GMT
CMD ["rebar3" "shell"]
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
	-	`sha256:893be01d7b7de102971d1f45a435066f8a3227aaad0816bbc1ceccf3695142e7`  
		Last Modified: Fri, 03 Feb 2017 19:39:08 GMT  
		Size: 57.7 MB (57737804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63824166a6b33b5899413b03b44496cc42a32afdb9ce2a270e54f508a31c0852`  
		Last Modified: Fri, 03 Feb 2017 19:38:56 GMT  
		Size: 200.4 KB (200357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6804cca6aa7c22d7bcf98b212fe2a5b31bf0fe10fc0852f2216ab31e467dff8`  
		Last Modified: Fri, 03 Feb 2017 19:38:57 GMT  
		Size: 2.1 MB (2081608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf2e490701e6607f2857525420d3e345997f72a66a8fcfb1473c443a2b00c55`  
		Last Modified: Fri, 03 Feb 2017 19:41:33 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
