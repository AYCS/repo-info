## `percona:latest`

```console
$ docker pull percona@sha256:2e2cb69f4347259b7a5f692d2197dc9ab56726cac97a87c74be533693825b000
```

-	Platforms:
	-	linux; amd64

### `percona:latest` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125433959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:727978cafa873527230c9d396a477cd98209936d665f82502917de3130317384`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 16 Jan 2017 20:35:09 GMT
ADD file:89ecb642d662ee7edbb868340551106d51336c7e589fdaca4111725ec64da957 in / 
# Mon, 16 Jan 2017 20:35:16 GMT
CMD ["/bin/bash"]
# Tue, 17 Jan 2017 17:16:20 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 17 Jan 2017 17:16:20 GMT
ENV GOSU_VERSION=1.7
# Tue, 17 Jan 2017 17:16:35 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Tue, 17 Jan 2017 17:16:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 17 Jan 2017 17:16:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		apt-transport-https ca-certificates 		pwgen 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Jan 2017 18:52:21 GMT
ENV GPG_KEYS=430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 	4D1BB29D63D98E422B2113B19334A25F8507EFA5
# Tue, 17 Jan 2017 18:52:24 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --export $GPG_KEYS > /etc/apt/trusted.gpg.d/percona.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 17 Jan 2017 18:52:25 GMT
RUN echo 'deb https://repo.percona.com/apt jessie main' > /etc/apt/sources.list.d/percona.list
# Tue, 17 Jan 2017 18:52:25 GMT
ENV PERCONA_MAJOR=5.7
# Tue, 07 Feb 2017 20:32:05 GMT
ENV PERCONA_VERSION=5.7.17-11-1.jessie
# Tue, 07 Feb 2017 20:32:30 GMT
RUN { 		echo percona-server-server-$PERCONA_MAJOR percona-server-server/root_password password 'unused'; 		echo percona-server-server-$PERCONA_MAJOR percona-server-server/root_password_again password 'unused'; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		percona-server-server-$PERCONA_MAJOR=$PERCONA_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Tue, 07 Feb 2017 20:32:32 GMT
RUN find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& myCnf="$(find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lE '^\[mysqld\]' 		| head -n1)" 	&& echo 'skip-host-cache\nskip-name-resolve' 		| awk '{ print } $1 == "[mysqld]" && c == 0 { c = 1; system("cat") }' "$myCnf" > /tmp/my.cnf 	&& mv /tmp/my.cnf "$myCnf"
# Tue, 07 Feb 2017 20:32:32 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 07 Feb 2017 20:32:33 GMT
COPY file:01e6982f4616ce5335aa8fc1b158e02657d5596a595c569bb9febb58755d8095 in /usr/local/bin/ 
# Tue, 07 Feb 2017 20:32:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 07 Feb 2017 20:32:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Feb 2017 20:32:36 GMT
EXPOSE 3306/tcp
# Tue, 07 Feb 2017 20:32:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:5040bd2983909aa8896b9932438c3f1479d25ae837a5f6220242a264d0221f2d`  
		Last Modified: Mon, 16 Jan 2017 20:43:26 GMT  
		Size: 51.4 MB (51361210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55370df683150a0191e0349c09e9113d3b5c06475334ccb21365bcbcc696b4ef`  
		Last Modified: Wed, 18 Jan 2017 04:29:36 GMT  
		Size: 2.0 KB (2047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fad5195d69ccfb010b2a2aa36be888eaece726ddd355ac126ef45f126e3bee99`  
		Last Modified: Wed, 18 Jan 2017 04:29:36 GMT  
		Size: 1.2 MB (1216700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1034a5fbbfc91073603066f2801c0705ed3b2ac81976f560b4854a5a1262f29`  
		Last Modified: Wed, 18 Jan 2017 04:29:34 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb46f36a6163492d45487d66f6442838de6df332309f4b43869d2a32d4bc6623`  
		Last Modified: Wed, 18 Jan 2017 04:29:35 GMT  
		Size: 6.5 MB (6467462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f411e6fbe19a856d0c77595cea66f26da319518066a697c30d679a934928141c`  
		Last Modified: Wed, 18 Jan 2017 06:43:37 GMT  
		Size: 4.7 KB (4669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4d137990906d895c15dc563fca313108939f68a0b65aea80396281a8545685`  
		Last Modified: Wed, 18 Jan 2017 06:43:34 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1afa2a8e22fdd31325ac134a0d89e9f3963c508149fd932baadac613a9a5a7`  
		Last Modified: Tue, 07 Feb 2017 20:34:03 GMT  
		Size: 66.4 MB (66378497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecce6d3964a7be90bf93904b8ed4d3910daf2a1a71a36f549bf272b3a8f4d545`  
		Last Modified: Tue, 07 Feb 2017 20:33:44 GMT  
		Size: 796.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd4a49de29bcebc326a25085f874451fd615caca9172d9e3d47029b7df9b4d18`  
		Last Modified: Tue, 07 Feb 2017 20:33:44 GMT  
		Size: 2.1 KB (2133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2083ecc2f9c9b6939d4c201ea3359c3eeeafa8de401eaf1cbff42013e58b106`  
		Last Modified: Tue, 07 Feb 2017 20:33:44 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
