## `node:6-onbuild`

```console
$ docker pull node@sha256:ab918ca4f8eb04e425796f30ede22378f9886def220ddd5cab43651d9f2902c6
```

-	Platforms:
	-	linux; amd64

### `node:6-onbuild` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.3 MB (256259168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d8c25b12402eb9c69bd5017a556b10346ba66e2fa214f89214fcfdbd59e5a15`
-	Default Command: `["npm","start"]`

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
# Wed, 18 Jan 2017 01:00:42 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 18 Jan 2017 01:00:46 GMT
RUN set -ex   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     0034A06D9D9B0064CE8ADF6BF1747F4AD2306D93     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   ; do     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";   done
# Wed, 18 Jan 2017 01:00:46 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Wed, 01 Feb 2017 17:14:29 GMT
ENV NODE_VERSION=6.9.5
# Wed, 01 Feb 2017 17:14:33 GMT
RUN curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-x64.tar.xz"   && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-x64.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-x64.tar.xz" -C /usr/local --strip-components=1   && rm "node-v$NODE_VERSION-linux-x64.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Wed, 01 Feb 2017 17:14:33 GMT
CMD ["node"]
# Wed, 01 Feb 2017 17:25:52 GMT
RUN mkdir -p /usr/src/app
# Wed, 01 Feb 2017 17:25:52 GMT
WORKDIR /usr/src/app
# Wed, 01 Feb 2017 17:25:53 GMT
ONBUILD ARG NODE_ENV
# Wed, 01 Feb 2017 17:25:53 GMT
ONBUILD ENV NODE_ENV $NODE_ENV
# Wed, 01 Feb 2017 17:25:53 GMT
ONBUILD COPY package.json /usr/src/app/
# Wed, 01 Feb 2017 17:25:54 GMT
ONBUILD RUN npm install && npm cache clean
# Wed, 01 Feb 2017 17:25:54 GMT
ONBUILD COPY . /usr/src/app
# Wed, 01 Feb 2017 17:25:54 GMT
CMD ["npm" "start"]
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
	-	`sha256:7e5867712a67ea225b93a0c0c2349cd4c96496bc3439201154f9666752781f97`  
		Last Modified: Wed, 18 Jan 2017 05:28:55 GMT  
		Size: 4.4 KB (4357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:563b602246dd20c36a6c26cf8a7ade281c354fc375841b011dce74cf2df48695`  
		Last Modified: Wed, 18 Jan 2017 05:28:55 GMT  
		Size: 97.2 KB (97212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:043696f3823666f54ba64e52c94d631a9d3f598b9870612c07ebab55dd0f7d0a`  
		Last Modified: Wed, 01 Feb 2017 17:39:45 GMT  
		Size: 13.9 MB (13935301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe604be85e7bce096ab33b9193839aa71504eaabc4994a166fe999c788bf5037`  
		Last Modified: Wed, 01 Feb 2017 17:41:57 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
