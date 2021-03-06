## `redis:32bit`

```console
$ docker pull redis@sha256:edc20e674010fbed6c4dd369f8b28510a4549c25714e7f9dbb3dace7f643ae9e
```

-	Platforms:
	-	linux; amd64

### `redis:32bit` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.2 MB (78208528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b86e8e419f04b69f1354335f339fdf8089b3cd436a637be5ae38965266741027`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 16 Jan 2017 20:35:09 GMT
ADD file:89ecb642d662ee7edbb868340551106d51336c7e589fdaca4111725ec64da957 in / 
# Mon, 16 Jan 2017 20:35:16 GMT
CMD ["/bin/bash"]
# Tue, 17 Jan 2017 20:05:20 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Tue, 17 Jan 2017 20:05:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Jan 2017 20:05:32 GMT
ENV GOSU_VERSION=1.7
# Tue, 17 Jan 2017 20:05:37 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Tue, 31 Jan 2017 19:52:00 GMT
ENV REDIS_VERSION=3.2.7
# Tue, 31 Jan 2017 19:52:00 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-3.2.7.tar.gz
# Tue, 31 Jan 2017 19:52:01 GMT
ENV REDIS_DOWNLOAD_SHA1=6889af053020cd72ebb16805ead0ce9b3a69a9ef
# Tue, 31 Jan 2017 19:52:58 GMT
RUN apt-get update && apt-get install -y libc6-i386 --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2017 19:53:49 GMT
RUN set -ex 		&& buildDeps=' 		gcc 		gcc-multilib 		libc6-dev-i386 		make 	' 	&& apt-get update 	&& apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL" 	&& echo "$REDIS_DOWNLOAD_SHA1 *redis.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/redis 	&& tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1 	&& rm redis.tar.gz 		&& grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h 	&& sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h 	&& grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h 		&& make -C /usr/src/redis 32bit 	&& make -C /usr/src/redis install 		&& rm -r /usr/src/redis 		&& apt-get purge -y --auto-remove $buildDeps
# Tue, 31 Jan 2017 19:53:50 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 31 Jan 2017 19:53:51 GMT
VOLUME [/data]
# Tue, 31 Jan 2017 19:53:51 GMT
WORKDIR /data
# Tue, 31 Jan 2017 19:53:52 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Tue, 31 Jan 2017 19:53:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Jan 2017 19:53:53 GMT
EXPOSE 6379/tcp
# Tue, 31 Jan 2017 19:53:54 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:5040bd2983909aa8896b9932438c3f1479d25ae837a5f6220242a264d0221f2d`  
		Last Modified: Mon, 16 Jan 2017 20:43:26 GMT  
		Size: 51.4 MB (51361210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996f41e871db11ed71fa871e4a71e6fb918289a9c3f2500f122d901ac8566fc7`  
		Last Modified: Wed, 18 Jan 2017 07:13:42 GMT  
		Size: 2.0 KB (2037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40484248761f567a45443550fce54c4da469739890218490c717800e2dae94e`  
		Last Modified: Wed, 18 Jan 2017 07:13:46 GMT  
		Size: 16.6 MB (16617736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97af2bf2ee7313c7f635afe41a352863eef2135274d6df5e528466cb02c4455`  
		Last Modified: Wed, 18 Jan 2017 07:13:39 GMT  
		Size: 807.9 KB (807934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73dbdf73d737ce01cb5c0520011f6a98d72e30729354a07bbd29d67e615c31c4`  
		Last Modified: Tue, 31 Jan 2017 19:57:39 GMT  
		Size: 4.2 MB (4224195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c6bae7655ae33af08e16053005a854063be5a1a912518dc69dd6e0b74f5781`  
		Last Modified: Tue, 31 Jan 2017 19:57:40 GMT  
		Size: 5.2 MB (5194922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a5a8f645d4ae6d7dbb9f1d84419b6d66bbcb1036fec578c3bf257d85446830`  
		Last Modified: Tue, 31 Jan 2017 19:57:38 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7654b43e406e71fd9a5e666e8a62fcde42b91a398c69209aa11ad45aef8a5846`  
		Last Modified: Tue, 31 Jan 2017 19:57:38 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
