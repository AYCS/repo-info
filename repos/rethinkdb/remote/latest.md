## `rethinkdb:latest`

```console
$ docker pull rethinkdb@sha256:4308852f1d72beeeb7b47b6c715e2df0f1d8f7063a2dc5b6c6de430e29e1bb58
```

-	Platforms:
	-	linux; amd64

### `rethinkdb:latest` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (75979083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58283079a43dc4742390580f968106f5d2cdd519e6f94050a7d0aa0987a1bd96`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 16 Jan 2017 20:35:09 GMT
ADD file:89ecb642d662ee7edbb868340551106d51336c7e589fdaca4111725ec64da957 in / 
# Mon, 16 Jan 2017 20:35:16 GMT
CMD ["/bin/bash"]
# Tue, 17 Jan 2017 20:09:27 GMT
MAINTAINER Daniel Alan Miller <dalanmiller@rethinkdb.com>
# Tue, 17 Jan 2017 20:10:08 GMT
RUN apt-key adv --keyserver pgp.mit.edu --recv-keys 1614552E5765227AEC39EFCFA7E00EF33A8F2399
# Tue, 17 Jan 2017 20:10:09 GMT
RUN echo "deb http://download.rethinkdb.com/apt jessie main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 17 Jan 2017 20:10:09 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.3.5~0jessie
# Tue, 17 Jan 2017 20:10:25 GMT
RUN apt-get update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Jan 2017 20:10:25 GMT
VOLUME [/data]
# Tue, 17 Jan 2017 20:10:26 GMT
WORKDIR /data
# Tue, 17 Jan 2017 20:10:26 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 17 Jan 2017 20:10:26 GMT
EXPOSE 28015/tcp 29015/tcp 8080/tcp
```

-	Layers:
	-	`sha256:5040bd2983909aa8896b9932438c3f1479d25ae837a5f6220242a264d0221f2d`  
		Last Modified: Mon, 16 Jan 2017 20:43:26 GMT  
		Size: 51.4 MB (51361210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:902449b396bbbafd940c336125926fe04ae010b0a63750a25565f024c8c07d20`  
		Last Modified: Wed, 18 Jan 2017 07:17:31 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a4fa5706b014d41e977e0aee118b834911b32933fffc21cc39df2470103cfc`  
		Last Modified: Wed, 18 Jan 2017 07:17:31 GMT  
		Size: 215.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d9e503a4e8ec28460695b3bad4f3e60bcb559b1699cb9c31cdcbf5387a80a1`  
		Last Modified: Wed, 18 Jan 2017 07:21:09 GMT  
		Size: 24.6 MB (24616125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f0c06b995f6a8c4bd3e6e8425e2ff3f9fb953eeb87fc81faf70dc0bf5e1f5dd`  
		Last Modified: Wed, 18 Jan 2017 07:21:01 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
