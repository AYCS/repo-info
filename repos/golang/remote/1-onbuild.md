## `golang:1-onbuild`

```console
$ docker pull golang@sha256:5b6a035146e3715b51e3b03b8d97539e4c50dafa7b8c3d760c9a40d8de2093c5
```

-	Platforms:
	-	linux; amd64

### `golang:1-onbuild` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.3 MB (255313706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4602a51f65cf932ffb1ae0c1ba1d939e2e6af530e7ef00ad33cd331736efccd3`
-	Default Command: `["go-wrapper","run"]`

```dockerfile
# Mon, 16 Jan 2017 20:35:09 GMT
ADD file:89ecb642d662ee7edbb868340551106d51336c7e589fdaca4111725ec64da957 in / 
# Mon, 16 Jan 2017 20:35:16 GMT
CMD ["/bin/bash"]
# Tue, 17 Jan 2017 00:00:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Jan 2017 00:01:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Jan 2017 00:40:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Fri, 27 Jan 2017 22:37:08 GMT
ENV GOLANG_VERSION=1.7.5
# Fri, 27 Jan 2017 22:37:09 GMT
ENV GOLANG_DOWNLOAD_URL=https://golang.org/dl/go1.7.5.linux-amd64.tar.gz
# Fri, 27 Jan 2017 22:37:10 GMT
ENV GOLANG_DOWNLOAD_SHA256=2e4dd6c44f0693bef4e7b46cc701513d74c3cc44f2419bf519d7868b12931ac3
# Fri, 27 Jan 2017 22:37:20 GMT
RUN curl -fsSL "$GOLANG_DOWNLOAD_URL" -o golang.tar.gz 	&& echo "$GOLANG_DOWNLOAD_SHA256  golang.tar.gz" | sha256sum -c - 	&& tar -C /usr/local -xzf golang.tar.gz 	&& rm golang.tar.gz
# Fri, 27 Jan 2017 22:37:21 GMT
ENV GOPATH=/go
# Fri, 27 Jan 2017 22:37:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Jan 2017 22:37:22 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 27 Jan 2017 22:37:23 GMT
WORKDIR /go
# Fri, 27 Jan 2017 22:37:24 GMT
COPY file:f6191f2c86edc9343569339f101facba47e886e33e29d70da6916ca6b1101a53 in /usr/local/bin/ 
# Fri, 27 Jan 2017 22:37:25 GMT
RUN mkdir -p /go/src/app
# Fri, 27 Jan 2017 22:37:26 GMT
WORKDIR /go/src/app
# Fri, 27 Jan 2017 22:37:26 GMT
CMD ["go-wrapper" "run"]
# Fri, 27 Jan 2017 22:37:27 GMT
ONBUILD COPY . /go/src/app
# Fri, 27 Jan 2017 22:37:27 GMT
ONBUILD RUN go-wrapper download
# Fri, 27 Jan 2017 22:37:28 GMT
ONBUILD RUN go-wrapper install
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
	-	`sha256:86b681f75ff656775b833d40e824f47d5b46215fd8a2e829b2b9cf89b28a1628`  
		Last Modified: Wed, 18 Jan 2017 03:45:10 GMT  
		Size: 59.7 MB (59661679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:379455b45ee9f44b21a56cc6ad0fa6a9bab5e63a73bc5df84c08064b3eed2684`  
		Last Modified: Fri, 27 Jan 2017 22:47:53 GMT  
		Size: 83.3 MB (83251361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cec794755987d2cd56c5cb8a7d0d017ec1a0df7dec4f0d9da0183d7c51fc0b3`  
		Last Modified: Fri, 27 Jan 2017 22:47:23 GMT  
		Size: 123.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66e8958dcb38803888b44e06301730bf613d5518bb858d424fa889036662a11d`  
		Last Modified: Fri, 27 Jan 2017 22:47:23 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f060b9ab9f00d7f42e19d2e3f74c32249d2e341db66e12c01edc505900397236`  
		Last Modified: Fri, 27 Jan 2017 22:48:56 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
