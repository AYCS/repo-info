## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:77c96fecce490957a136354471e4cc32d087a682b38e054ddf1cafbae660e22f
```

-	Platforms:
	-	linux; amd64

### `neo4j:enterprise` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.3 MB (131323624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6740e23e24c34bb779c776970c1f40d603bc477472cedd0f7e5855c8e61a92fb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 27 Dec 2016 18:17:13 GMT
ADD file:eeed5f514a35d18fcd9cbfe6c40c582211020bffdd53e4799018d33826fe5067 in / 
# Tue, 27 Dec 2016 18:37:54 GMT
ENV LANG=C.UTF-8
# Tue, 27 Dec 2016 18:37:55 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 27 Dec 2016 18:38:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8-openjdk/jre
# Tue, 27 Dec 2016 18:38:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Tue, 27 Dec 2016 18:38:44 GMT
ENV JAVA_VERSION=8u111
# Tue, 27 Dec 2016 18:38:45 GMT
ENV JAVA_ALPINE_VERSION=8.111.14-r0
# Tue, 27 Dec 2016 18:38:49 GMT
RUN set -x 	&& apk add --no-cache 		openjdk8-jre="$JAVA_ALPINE_VERSION" 	&& [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 27 Dec 2016 22:21:19 GMT
RUN apk add --no-cache --quiet     bash     curl
# Tue, 31 Jan 2017 17:40:06 GMT
ENV NEO4J_SHA256=20a8cda35d90c518319fdbb7aa8ecb11e306777bf8b8ff7df623cdb473b593a7
# Tue, 31 Jan 2017 17:40:06 GMT
ENV NEO4J_TARBALL=neo4j-enterprise-3.1.1-unix.tar.gz
# Tue, 31 Jan 2017 17:40:06 GMT
ARG NEO4J_URI=http://dist.neo4j.org/neo4j-enterprise-3.1.1-unix.tar.gz
# Tue, 31 Jan 2017 17:40:07 GMT
COPY file:2e411d607fa15f91ae6f4b515dde6bf3e158d34c0036556e00553ed1c50cd63d in /tmp/ 
# Tue, 31 Jan 2017 17:40:22 GMT
# ARGS: NEO4J_URI=http://dist.neo4j.org/neo4j-enterprise-3.1.1-unix.tar.gz
RUN curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -csw -     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* /var/lib/neo4j     && rm ${NEO4J_TARBALL}
# Tue, 31 Jan 2017 17:40:26 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Jan 2017 17:40:27 GMT
# ARGS: NEO4J_URI=http://dist.neo4j.org/neo4j-enterprise-3.1.1-unix.tar.gz
RUN mv data /data     && ln -s /data
# Tue, 31 Jan 2017 17:40:28 GMT
VOLUME [/data]
# Tue, 31 Jan 2017 17:40:28 GMT
COPY file:77937095ede0ebf8d922e2d061f12dc5de64a045c38a47b59579caac7c90f6f6 in /docker-entrypoint.sh 
# Tue, 31 Jan 2017 17:40:42 GMT
EXPOSE 7473/tcp 7474/tcp 7687/tcp
# Tue, 31 Jan 2017 17:40:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 31 Jan 2017 17:40:43 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f33cc0b48ea4fb2f0745def58c25483a5f6b7aed5b41ce8f1cb6e17f5723cf`  
		Last Modified: Tue, 27 Dec 2016 18:18:49 GMT  
		Size: 2.3 MB (2313090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43a564ae36a32a4575a2cc6de78b6d1b7ce5c581bca7b875d789e026198c1d55`  
		Last Modified: Tue, 27 Dec 2016 18:46:24 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efb75a810eee14e75bc372b510c025740f57b5eddae56f87dd85f0f9ef531c9f`  
		Last Modified: Tue, 27 Dec 2016 18:59:36 GMT  
		Size: 39.7 MB (39670203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97825d23288af99b02c4194ef308b44e8040eacf91d299e5f2c6eaf0b1f0a0c6`  
		Last Modified: Tue, 27 Dec 2016 22:57:48 GMT  
		Size: 1.5 MB (1455343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:120cebe9f4a9b4fdedf66e93649d1a13dad023b83ab3629b93415af963bdfaae`  
		Last Modified: Tue, 31 Jan 2017 17:43:00 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:208b1ccc4909f4963e68f4a0b01dc491e38a540d1046fd688cf6091c7aef90ad`  
		Last Modified: Tue, 31 Jan 2017 17:43:09 GMT  
		Size: 87.9 MB (87883209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7799bd1d98db6fbaa6c47eb02d2ed0ea03b65f96b9edbbf880df27838f5dd6`  
		Last Modified: Tue, 31 Jan 2017 17:43:00 GMT  
		Size: 216.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2978c3edc96a0cdc95d11aa0f18c22cb2f108b0bb7675e83183db5378bf85db1`  
		Last Modified: Tue, 31 Jan 2017 17:43:01 GMT  
		Size: 1.2 KB (1204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
