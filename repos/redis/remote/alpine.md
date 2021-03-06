## `redis:alpine`

```console
$ docker pull redis@sha256:95f0c9434f37db0a4f9563379184ff4895685d2381e2d81bd10dfcbcadfc095f
```

-	Platforms:
	-	linux; amd64

### `redis:alpine` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8124003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:147b1b8460d23e3d8a24b3503a9947ffdee6aaf520e4d41cfd8b045715809188`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 27 Dec 2016 18:17:25 GMT
ADD file:92ab746eb22dd3ed2b87469c719adf3c1bed7302653bbd76baafd7cfd95e911e in / 
# Wed, 04 Jan 2017 21:32:52 GMT
RUN addgroup -S redis && adduser -S -G redis redis
# Wed, 04 Jan 2017 21:32:54 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 31 Jan 2017 19:53:55 GMT
ENV REDIS_VERSION=3.2.7
# Tue, 31 Jan 2017 19:53:55 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-3.2.7.tar.gz
# Tue, 31 Jan 2017 19:53:56 GMT
ENV REDIS_DOWNLOAD_SHA1=6889af053020cd72ebb16805ead0ce9b3a69a9ef
# Tue, 31 Jan 2017 19:54:41 GMT
RUN set -ex 		&& apk add --no-cache --virtual .build-deps 		gcc 		linux-headers 		make 		musl-dev 		tar 		&& wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL" 	&& echo "$REDIS_DOWNLOAD_SHA1 *redis.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/redis 	&& tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1 	&& rm redis.tar.gz 		&& grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h 	&& sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h 	&& grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h 		&& make -C /usr/src/redis 	&& make -C /usr/src/redis install 		&& rm -r /usr/src/redis 		&& apk del .build-deps
# Tue, 31 Jan 2017 19:54:42 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 31 Jan 2017 19:54:43 GMT
VOLUME [/data]
# Tue, 31 Jan 2017 19:54:43 GMT
WORKDIR /data
# Tue, 31 Jan 2017 19:54:44 GMT
COPY file:9b596974f478088dc2d2bf2906046f6c8872ecff3c716abd89850fd50ec90c47 in /usr/local/bin/ 
# Tue, 31 Jan 2017 19:54:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Jan 2017 19:54:45 GMT
EXPOSE 6379/tcp
# Tue, 31 Jan 2017 19:54:46 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:0a8490d0dfd399b3a50e9aaa81dba0d425c3868762d46526b41be00886bcc28b`  
		Last Modified: Tue, 27 Dec 2016 18:19:22 GMT  
		Size: 1.9 MB (1902063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d0e817ebe24b8370ee8853b4a95ffea8b7bfb4f38f36d5bcea30175e7184ed`  
		Last Modified: Thu, 05 Jan 2017 00:56:22 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f2a4f935feb715baf7666a365ec66e8fa0709a25411be7d204948fb6ad181da`  
		Last Modified: Thu, 05 Jan 2017 00:56:20 GMT  
		Size: 7.7 KB (7677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4664c32a79d32f195fc3f4442b3ff916aa75313783af317aecfef2954584864d`  
		Last Modified: Tue, 31 Jan 2017 19:58:47 GMT  
		Size: 6.2 MB (6212527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de138f8bbe03b430fd66093f458f7460015f9bfc24536689b6bc246b830a2b9e`  
		Last Modified: Tue, 31 Jan 2017 19:58:46 GMT  
		Size: 99.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c82352e732c0c9c0bacacdb400365b085b20b5ecf8c2b610f5768a2ac9933976`  
		Last Modified: Tue, 31 Jan 2017 19:58:45 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
