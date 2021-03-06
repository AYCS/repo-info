## `docker:git`

```console
$ docker pull docker@sha256:7f1958690745fb5dec6b38309a73c3367f030753ef07d149bdef07b95dae797a
```

-	Platforms:
	-	linux; amd64

### `docker:git` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42110122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23d94ba7a3929fad5b4db424cf0abc31a43d757a42f2a19363cc51ebfa03a90e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 27 Dec 2016 18:17:25 GMT
ADD file:92ab746eb22dd3ed2b87469c719adf3c1bed7302653bbd76baafd7cfd95e911e in / 
# Wed, 04 Jan 2017 21:04:10 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl
# Wed, 04 Jan 2017 21:04:27 GMT
ENV DOCKER_BUCKET=get.docker.com
# Wed, 18 Jan 2017 22:47:58 GMT
ENV DOCKER_VERSION=1.13.0
# Wed, 18 Jan 2017 22:47:58 GMT
ENV DOCKER_SHA256=fc194bb95640b1396283e5b23b5ff9d1b69a5e418b5b3d774f303a7642162ad6
# Wed, 18 Jan 2017 22:48:02 GMT
RUN set -x 	&& curl -fSL "https://${DOCKER_BUCKET}/builds/Linux/x86_64/docker-${DOCKER_VERSION}.tgz" -o docker.tgz 	&& echo "${DOCKER_SHA256} *docker.tgz" | sha256sum -c - 	&& tar -xzvf docker.tgz 	&& mv docker/* /usr/local/bin/ 	&& rmdir docker 	&& rm docker.tgz 	&& docker -v
# Wed, 18 Jan 2017 22:48:03 GMT
COPY file:a8b1446f032ff01ac092c29a0af328f0b9d47bbee72d1049499f2a9a89ee988a in /usr/local/bin/ 
# Wed, 18 Jan 2017 22:48:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Jan 2017 22:48:04 GMT
CMD ["sh"]
# Wed, 18 Jan 2017 22:48:14 GMT
RUN apk add --no-cache 		git 		openssh-client
```

-	Layers:
	-	`sha256:0a8490d0dfd399b3a50e9aaa81dba0d425c3868762d46526b41be00886bcc28b`  
		Last Modified: Tue, 27 Dec 2016 18:19:22 GMT  
		Size: 1.9 MB (1902063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af50e60f15f49e6f8bd6fd84a5388b6de295a9e87ba9bc86878d04b5037d9b7`  
		Last Modified: Wed, 04 Jan 2017 23:28:13 GMT  
		Size: 2.2 MB (2166920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aad3b7733bb756aaa457c8f743aa0e14a6a03cd7bd0c27efb2e4edcc226142a`  
		Last Modified: Wed, 18 Jan 2017 22:48:42 GMT  
		Size: 27.7 MB (27694510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4183fcffe507113490542a166d7dff392cd4e480975fbcd6faf14e613bf89e10`  
		Last Modified: Wed, 18 Jan 2017 22:48:31 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d4078a6f7d418f191b2587beb10e27ae36b2fd27fa5e2480faf9615f9366346`  
		Last Modified: Wed, 18 Jan 2017 22:50:45 GMT  
		Size: 10.3 MB (10346140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
