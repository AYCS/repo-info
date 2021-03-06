<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `redmine`

-	[`redmine:3.1.7`](#redmine317)
-	[`redmine:3.1`](#redmine31)
-	[`redmine:3.1.7-passenger`](#redmine317-passenger)
-	[`redmine:3.1-passenger`](#redmine31-passenger)
-	[`redmine:3.2.5`](#redmine325)
-	[`redmine:3.2`](#redmine32)
-	[`redmine:3.2.5-passenger`](#redmine325-passenger)
-	[`redmine:3.2-passenger`](#redmine32-passenger)
-	[`redmine:3.3.2`](#redmine332)
-	[`redmine:3.3`](#redmine33)
-	[`redmine:3`](#redmine3)
-	[`redmine:latest`](#redminelatest)
-	[`redmine:3.3.2-passenger`](#redmine332-passenger)
-	[`redmine:3.3-passenger`](#redmine33-passenger)
-	[`redmine:3-passenger`](#redmine3-passenger)
-	[`redmine:passenger`](#redminepassenger)

## `redmine:3.1.7`

```console
$ docker pull redmine@sha256:4c74438f981e5fe13d8a2e60f47fc9bde972f011758b9fa3cd20473538acf1f3
```

-	Platforms:
	-	linux; amd64

### `redmine:3.1.7` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.5 MB (237478176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:659a3150cef92758de0ca23d46a07aaf3281b382615ce540ef8752f809d6528d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 16 Jan 2017 20:35:09 GMT
ADD file:89ecb642d662ee7edbb868340551106d51336c7e589fdaca4111725ec64da957 in / 
# Mon, 16 Jan 2017 20:35:16 GMT
CMD ["/bin/bash"]
# Tue, 17 Jan 2017 20:12:19 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Jan 2017 20:12:20 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 17 Jan 2017 20:17:55 GMT
ENV RUBY_MAJOR=2.2
# Tue, 17 Jan 2017 20:17:55 GMT
ENV RUBY_VERSION=2.2.6
# Tue, 17 Jan 2017 20:17:55 GMT
ENV RUBY_DOWNLOAD_SHA256=9414ecc0d09cf71c9a24e8dc82fcc87919ac7359fb08db2791d6c32bfd157339
# Wed, 25 Jan 2017 18:08:18 GMT
ENV RUBYGEMS_VERSION=2.6.10
# Wed, 25 Jan 2017 18:10:49 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& ./configure --disable-install-doc --enable-shared 	&& make -j"$(nproc)" 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION"
# Wed, 25 Jan 2017 18:10:49 GMT
ENV BUNDLER_VERSION=1.14.3
# Wed, 25 Jan 2017 18:10:50 GMT
RUN gem install bundler --version "$BUNDLER_VERSION"
# Wed, 25 Jan 2017 18:10:51 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 25 Jan 2017 18:10:51 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 25 Jan 2017 18:10:51 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Jan 2017 18:10:52 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Wed, 25 Jan 2017 18:10:52 GMT
CMD ["irb"]
# Wed, 25 Jan 2017 19:07:25 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Wed, 25 Jan 2017 19:07:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2017 19:07:34 GMT
ENV GOSU_VERSION=1.7
# Wed, 25 Jan 2017 19:07:39 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Wed, 25 Jan 2017 19:07:39 GMT
ENV TINI_VERSION=v0.9.0
# Wed, 25 Jan 2017 19:07:42 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Wed, 25 Jan 2017 19:08:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2017 19:08:14 GMT
ENV RAILS_ENV=production
# Wed, 25 Jan 2017 19:08:14 GMT
WORKDIR /usr/src/redmine
# Wed, 25 Jan 2017 19:08:15 GMT
ENV REDMINE_VERSION=3.1.7
# Wed, 25 Jan 2017 19:08:15 GMT
ENV REDMINE_DOWNLOAD_MD5=625b7705b70521a205491a53f6df506a
# Wed, 25 Jan 2017 19:08:20 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Wed, 25 Jan 2017 19:10:38 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Wed, 25 Jan 2017 19:10:39 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 25 Jan 2017 19:10:40 GMT
COPY file:5efb6ca648b54af01740423ca0fdde905eae0ce732d8f2683c79dcf93e0e86c5 in / 
# Wed, 25 Jan 2017 19:10:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 25 Jan 2017 19:10:41 GMT
EXPOSE 3000/tcp
# Wed, 25 Jan 2017 19:10:41 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5040bd2983909aa8896b9932438c3f1479d25ae837a5f6220242a264d0221f2d`  
		Last Modified: Mon, 16 Jan 2017 20:43:26 GMT  
		Size: 51.4 MB (51361210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596ec0bfbfe79e6bf8ba516cc80f14487c52f661c1c8f1dfdef2535f165beb56`  
		Last Modified: Wed, 18 Jan 2017 07:25:44 GMT  
		Size: 10.0 MB (9994242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330c0f0b9895c0a3df4249a9e2fe344e00dc43a4d9aac66506818ee0a8408043`  
		Last Modified: Wed, 18 Jan 2017 07:25:33 GMT  
		Size: 204.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759aaf3bf184b4692bcec722e430b1de0efcc5ebde1900ed83ef473c51d13d25`  
		Last Modified: Wed, 25 Jan 2017 18:33:14 GMT  
		Size: 33.3 MB (33326682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d391bd471e9bc64130a292130fcc4209eda0d1104ace90657ee4a56936cce2`  
		Last Modified: Wed, 25 Jan 2017 18:33:04 GMT  
		Size: 631.7 KB (631727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d548a23aa17d0f8419147686fdfa8b4f1637c6d592d2e13747c673f78a94b3c`  
		Last Modified: Wed, 25 Jan 2017 18:33:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548bf7ed54c4db146a49c6c74fd814210ff67320823ebf8dd5a5bae27bb62bb0`  
		Last Modified: Wed, 25 Jan 2017 19:16:08 GMT  
		Size: 2.0 KB (2043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42efbdc1be57cd208a79d1d7e3d07d83ecb18ae788b4f4b2ef0d6e4fdc86e4c0`  
		Last Modified: Wed, 25 Jan 2017 19:16:11 GMT  
		Size: 13.9 MB (13863641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c31ff7009497607f6e6e568d32553e37836e372cde3c5e53014f911ad6d69e`  
		Last Modified: Wed, 25 Jan 2017 19:16:06 GMT  
		Size: 807.9 KB (807934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdc0aa7eb6c6b4772890ecd81a8544f69d86e7aecf56b6be1c25088e4a4208e`  
		Last Modified: Wed, 25 Jan 2017 19:16:05 GMT  
		Size: 7.1 KB (7122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2bb7220f9b536cc758b25d7b5a65d33622e72ea714030de7cfcdb4e5ab9ae3`  
		Last Modified: Wed, 25 Jan 2017 19:16:22 GMT  
		Size: 58.2 MB (58213014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bd5e9fe51eb83c0111790e7dda6c778aa07e6d7699168b08dbc2c50680d231`  
		Last Modified: Wed, 25 Jan 2017 19:16:03 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15e90cfd31c4b0355bf7e9788a0a9d2ab7c2efb859af8806f2e510513669df4e`  
		Last Modified: Wed, 25 Jan 2017 19:16:04 GMT  
		Size: 2.3 MB (2273002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e883b45f83744b5f30735e7eeab28576446a7bed2ff97d39b5283116d2d171d`  
		Last Modified: Wed, 25 Jan 2017 19:16:22 GMT  
		Size: 67.0 MB (66995536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89bd3f9da8b1815cfbe74860d236a442fb1015102917a079c6ef6e956ea42b0b`  
		Last Modified: Wed, 25 Jan 2017 19:16:03 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:3.1`

```console
$ docker pull redmine@sha256:4c74438f981e5fe13d8a2e60f47fc9bde972f011758b9fa3cd20473538acf1f3
```

-	Platforms:
	-	linux; amd64

### `redmine:3.1` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.5 MB (237478176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:659a3150cef92758de0ca23d46a07aaf3281b382615ce540ef8752f809d6528d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 16 Jan 2017 20:35:09 GMT
ADD file:89ecb642d662ee7edbb868340551106d51336c7e589fdaca4111725ec64da957 in / 
# Mon, 16 Jan 2017 20:35:16 GMT
CMD ["/bin/bash"]
# Tue, 17 Jan 2017 20:12:19 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Jan 2017 20:12:20 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 17 Jan 2017 20:17:55 GMT
ENV RUBY_MAJOR=2.2
# Tue, 17 Jan 2017 20:17:55 GMT
ENV RUBY_VERSION=2.2.6
# Tue, 17 Jan 2017 20:17:55 GMT
ENV RUBY_DOWNLOAD_SHA256=9414ecc0d09cf71c9a24e8dc82fcc87919ac7359fb08db2791d6c32bfd157339
# Wed, 25 Jan 2017 18:08:18 GMT
ENV RUBYGEMS_VERSION=2.6.10
# Wed, 25 Jan 2017 18:10:49 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& ./configure --disable-install-doc --enable-shared 	&& make -j"$(nproc)" 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION"
# Wed, 25 Jan 2017 18:10:49 GMT
ENV BUNDLER_VERSION=1.14.3
# Wed, 25 Jan 2017 18:10:50 GMT
RUN gem install bundler --version "$BUNDLER_VERSION"
# Wed, 25 Jan 2017 18:10:51 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 25 Jan 2017 18:10:51 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 25 Jan 2017 18:10:51 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Jan 2017 18:10:52 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Wed, 25 Jan 2017 18:10:52 GMT
CMD ["irb"]
# Wed, 25 Jan 2017 19:07:25 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Wed, 25 Jan 2017 19:07:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2017 19:07:34 GMT
ENV GOSU_VERSION=1.7
# Wed, 25 Jan 2017 19:07:39 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Wed, 25 Jan 2017 19:07:39 GMT
ENV TINI_VERSION=v0.9.0
# Wed, 25 Jan 2017 19:07:42 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Wed, 25 Jan 2017 19:08:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2017 19:08:14 GMT
ENV RAILS_ENV=production
# Wed, 25 Jan 2017 19:08:14 GMT
WORKDIR /usr/src/redmine
# Wed, 25 Jan 2017 19:08:15 GMT
ENV REDMINE_VERSION=3.1.7
# Wed, 25 Jan 2017 19:08:15 GMT
ENV REDMINE_DOWNLOAD_MD5=625b7705b70521a205491a53f6df506a
# Wed, 25 Jan 2017 19:08:20 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Wed, 25 Jan 2017 19:10:38 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Wed, 25 Jan 2017 19:10:39 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 25 Jan 2017 19:10:40 GMT
COPY file:5efb6ca648b54af01740423ca0fdde905eae0ce732d8f2683c79dcf93e0e86c5 in / 
# Wed, 25 Jan 2017 19:10:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 25 Jan 2017 19:10:41 GMT
EXPOSE 3000/tcp
# Wed, 25 Jan 2017 19:10:41 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5040bd2983909aa8896b9932438c3f1479d25ae837a5f6220242a264d0221f2d`  
		Last Modified: Mon, 16 Jan 2017 20:43:26 GMT  
		Size: 51.4 MB (51361210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596ec0bfbfe79e6bf8ba516cc80f14487c52f661c1c8f1dfdef2535f165beb56`  
		Last Modified: Wed, 18 Jan 2017 07:25:44 GMT  
		Size: 10.0 MB (9994242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330c0f0b9895c0a3df4249a9e2fe344e00dc43a4d9aac66506818ee0a8408043`  
		Last Modified: Wed, 18 Jan 2017 07:25:33 GMT  
		Size: 204.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759aaf3bf184b4692bcec722e430b1de0efcc5ebde1900ed83ef473c51d13d25`  
		Last Modified: Wed, 25 Jan 2017 18:33:14 GMT  
		Size: 33.3 MB (33326682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d391bd471e9bc64130a292130fcc4209eda0d1104ace90657ee4a56936cce2`  
		Last Modified: Wed, 25 Jan 2017 18:33:04 GMT  
		Size: 631.7 KB (631727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d548a23aa17d0f8419147686fdfa8b4f1637c6d592d2e13747c673f78a94b3c`  
		Last Modified: Wed, 25 Jan 2017 18:33:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548bf7ed54c4db146a49c6c74fd814210ff67320823ebf8dd5a5bae27bb62bb0`  
		Last Modified: Wed, 25 Jan 2017 19:16:08 GMT  
		Size: 2.0 KB (2043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42efbdc1be57cd208a79d1d7e3d07d83ecb18ae788b4f4b2ef0d6e4fdc86e4c0`  
		Last Modified: Wed, 25 Jan 2017 19:16:11 GMT  
		Size: 13.9 MB (13863641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c31ff7009497607f6e6e568d32553e37836e372cde3c5e53014f911ad6d69e`  
		Last Modified: Wed, 25 Jan 2017 19:16:06 GMT  
		Size: 807.9 KB (807934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdc0aa7eb6c6b4772890ecd81a8544f69d86e7aecf56b6be1c25088e4a4208e`  
		Last Modified: Wed, 25 Jan 2017 19:16:05 GMT  
		Size: 7.1 KB (7122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2bb7220f9b536cc758b25d7b5a65d33622e72ea714030de7cfcdb4e5ab9ae3`  
		Last Modified: Wed, 25 Jan 2017 19:16:22 GMT  
		Size: 58.2 MB (58213014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bd5e9fe51eb83c0111790e7dda6c778aa07e6d7699168b08dbc2c50680d231`  
		Last Modified: Wed, 25 Jan 2017 19:16:03 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15e90cfd31c4b0355bf7e9788a0a9d2ab7c2efb859af8806f2e510513669df4e`  
		Last Modified: Wed, 25 Jan 2017 19:16:04 GMT  
		Size: 2.3 MB (2273002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e883b45f83744b5f30735e7eeab28576446a7bed2ff97d39b5283116d2d171d`  
		Last Modified: Wed, 25 Jan 2017 19:16:22 GMT  
		Size: 67.0 MB (66995536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89bd3f9da8b1815cfbe74860d236a442fb1015102917a079c6ef6e956ea42b0b`  
		Last Modified: Wed, 25 Jan 2017 19:16:03 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:3.1.7-passenger`

```console
$ docker pull redmine@sha256:8eebb91028ecd7a0854068906beddeae9612488fa08915a6ec62690818a86d5b
```

-	Platforms:
	-	linux; amd64

### `redmine:3.1.7-passenger` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.0 MB (257049337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d74ad67312ac29cbfee742e23c387ce59dc0782030e15c43b445129510f09327`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Mon, 16 Jan 2017 20:35:09 GMT
ADD file:89ecb642d662ee7edbb868340551106d51336c7e589fdaca4111725ec64da957 in / 
# Mon, 16 Jan 2017 20:35:16 GMT
CMD ["/bin/bash"]
# Tue, 17 Jan 2017 20:12:19 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Jan 2017 20:12:20 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 17 Jan 2017 20:17:55 GMT
ENV RUBY_MAJOR=2.2
# Tue, 17 Jan 2017 20:17:55 GMT
ENV RUBY_VERSION=2.2.6
# Tue, 17 Jan 2017 20:17:55 GMT
ENV RUBY_DOWNLOAD_SHA256=9414ecc0d09cf71c9a24e8dc82fcc87919ac7359fb08db2791d6c32bfd157339
# Wed, 25 Jan 2017 18:08:18 GMT
ENV RUBYGEMS_VERSION=2.6.10
# Wed, 25 Jan 2017 18:10:49 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& ./configure --disable-install-doc --enable-shared 	&& make -j"$(nproc)" 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION"
# Wed, 25 Jan 2017 18:10:49 GMT
ENV BUNDLER_VERSION=1.14.3
# Wed, 25 Jan 2017 18:10:50 GMT
RUN gem install bundler --version "$BUNDLER_VERSION"
# Wed, 25 Jan 2017 18:10:51 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 25 Jan 2017 18:10:51 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 25 Jan 2017 18:10:51 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Jan 2017 18:10:52 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Wed, 25 Jan 2017 18:10:52 GMT
CMD ["irb"]
# Wed, 25 Jan 2017 19:07:25 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Wed, 25 Jan 2017 19:07:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2017 19:07:34 GMT
ENV GOSU_VERSION=1.7
# Wed, 25 Jan 2017 19:07:39 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Wed, 25 Jan 2017 19:07:39 GMT
ENV TINI_VERSION=v0.9.0
# Wed, 25 Jan 2017 19:07:42 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Wed, 25 Jan 2017 19:08:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2017 19:08:14 GMT
ENV RAILS_ENV=production
# Wed, 25 Jan 2017 19:08:14 GMT
WORKDIR /usr/src/redmine
# Wed, 25 Jan 2017 19:08:15 GMT
ENV REDMINE_VERSION=3.1.7
# Wed, 25 Jan 2017 19:08:15 GMT
ENV REDMINE_DOWNLOAD_MD5=625b7705b70521a205491a53f6df506a
# Wed, 25 Jan 2017 19:08:20 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Wed, 25 Jan 2017 19:10:38 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Wed, 25 Jan 2017 19:10:39 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 25 Jan 2017 19:10:40 GMT
COPY file:5efb6ca648b54af01740423ca0fdde905eae0ce732d8f2683c79dcf93e0e86c5 in / 
# Wed, 25 Jan 2017 19:10:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 25 Jan 2017 19:10:41 GMT
EXPOSE 3000/tcp
# Wed, 25 Jan 2017 19:10:41 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Wed, 25 Jan 2017 19:10:42 GMT
ENV PASSENGER_VERSION=5.1.2
# Wed, 25 Jan 2017 19:10:55 GMT
RUN buildDeps=' 		make 	' 	&& set -x 	&& apt-get update && apt-get install -y --no-install-recommends $buildDeps && rm -rf /var/lib/apt/lists/* 	&& gem install passenger --version "$PASSENGER_VERSION" 	&& apt-get purge -y --auto-remove $buildDeps
# Wed, 08 Feb 2017 21:47:09 GMT
RUN set -x 	&& passenger-config install-agent 	&& passenger-config download-nginx-engine
# Wed, 08 Feb 2017 21:47:10 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:5040bd2983909aa8896b9932438c3f1479d25ae837a5f6220242a264d0221f2d`  
		Last Modified: Mon, 16 Jan 2017 20:43:26 GMT  
		Size: 51.4 MB (51361210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596ec0bfbfe79e6bf8ba516cc80f14487c52f661c1c8f1dfdef2535f165beb56`  
		Last Modified: Wed, 18 Jan 2017 07:25:44 GMT  
		Size: 10.0 MB (9994242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330c0f0b9895c0a3df4249a9e2fe344e00dc43a4d9aac66506818ee0a8408043`  
		Last Modified: Wed, 18 Jan 2017 07:25:33 GMT  
		Size: 204.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759aaf3bf184b4692bcec722e430b1de0efcc5ebde1900ed83ef473c51d13d25`  
		Last Modified: Wed, 25 Jan 2017 18:33:14 GMT  
		Size: 33.3 MB (33326682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d391bd471e9bc64130a292130fcc4209eda0d1104ace90657ee4a56936cce2`  
		Last Modified: Wed, 25 Jan 2017 18:33:04 GMT  
		Size: 631.7 KB (631727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d548a23aa17d0f8419147686fdfa8b4f1637c6d592d2e13747c673f78a94b3c`  
		Last Modified: Wed, 25 Jan 2017 18:33:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548bf7ed54c4db146a49c6c74fd814210ff67320823ebf8dd5a5bae27bb62bb0`  
		Last Modified: Wed, 25 Jan 2017 19:16:08 GMT  
		Size: 2.0 KB (2043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42efbdc1be57cd208a79d1d7e3d07d83ecb18ae788b4f4b2ef0d6e4fdc86e4c0`  
		Last Modified: Wed, 25 Jan 2017 19:16:11 GMT  
		Size: 13.9 MB (13863641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c31ff7009497607f6e6e568d32553e37836e372cde3c5e53014f911ad6d69e`  
		Last Modified: Wed, 25 Jan 2017 19:16:06 GMT  
		Size: 807.9 KB (807934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdc0aa7eb6c6b4772890ecd81a8544f69d86e7aecf56b6be1c25088e4a4208e`  
		Last Modified: Wed, 25 Jan 2017 19:16:05 GMT  
		Size: 7.1 KB (7122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2bb7220f9b536cc758b25d7b5a65d33622e72ea714030de7cfcdb4e5ab9ae3`  
		Last Modified: Wed, 25 Jan 2017 19:16:22 GMT  
		Size: 58.2 MB (58213014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bd5e9fe51eb83c0111790e7dda6c778aa07e6d7699168b08dbc2c50680d231`  
		Last Modified: Wed, 25 Jan 2017 19:16:03 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15e90cfd31c4b0355bf7e9788a0a9d2ab7c2efb859af8806f2e510513669df4e`  
		Last Modified: Wed, 25 Jan 2017 19:16:04 GMT  
		Size: 2.3 MB (2273002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e883b45f83744b5f30735e7eeab28576446a7bed2ff97d39b5283116d2d171d`  
		Last Modified: Wed, 25 Jan 2017 19:16:22 GMT  
		Size: 67.0 MB (66995536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89bd3f9da8b1815cfbe74860d236a442fb1015102917a079c6ef6e956ea42b0b`  
		Last Modified: Wed, 25 Jan 2017 19:16:03 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64bef608e1afc0bfcc262567f25c3ba7a3f316c6ab684e53ff4f5a59eca3917`  
		Last Modified: Wed, 25 Jan 2017 19:17:00 GMT  
		Size: 15.5 MB (15504951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5a130dacc1ea6e98347b8b908fd11364388e02a863d29e6a0b0abd5e0c7b5f`  
		Last Modified: Wed, 08 Feb 2017 21:48:10 GMT  
		Size: 4.1 MB (4066210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:3.1-passenger`

```console
$ docker pull redmine@sha256:8eebb91028ecd7a0854068906beddeae9612488fa08915a6ec62690818a86d5b
```

-	Platforms:
	-	linux; amd64

### `redmine:3.1-passenger` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.0 MB (257049337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d74ad67312ac29cbfee742e23c387ce59dc0782030e15c43b445129510f09327`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Mon, 16 Jan 2017 20:35:09 GMT
ADD file:89ecb642d662ee7edbb868340551106d51336c7e589fdaca4111725ec64da957 in / 
# Mon, 16 Jan 2017 20:35:16 GMT
CMD ["/bin/bash"]
# Tue, 17 Jan 2017 20:12:19 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Jan 2017 20:12:20 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 17 Jan 2017 20:17:55 GMT
ENV RUBY_MAJOR=2.2
# Tue, 17 Jan 2017 20:17:55 GMT
ENV RUBY_VERSION=2.2.6
# Tue, 17 Jan 2017 20:17:55 GMT
ENV RUBY_DOWNLOAD_SHA256=9414ecc0d09cf71c9a24e8dc82fcc87919ac7359fb08db2791d6c32bfd157339
# Wed, 25 Jan 2017 18:08:18 GMT
ENV RUBYGEMS_VERSION=2.6.10
# Wed, 25 Jan 2017 18:10:49 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& ./configure --disable-install-doc --enable-shared 	&& make -j"$(nproc)" 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION"
# Wed, 25 Jan 2017 18:10:49 GMT
ENV BUNDLER_VERSION=1.14.3
# Wed, 25 Jan 2017 18:10:50 GMT
RUN gem install bundler --version "$BUNDLER_VERSION"
# Wed, 25 Jan 2017 18:10:51 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 25 Jan 2017 18:10:51 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 25 Jan 2017 18:10:51 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Jan 2017 18:10:52 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Wed, 25 Jan 2017 18:10:52 GMT
CMD ["irb"]
# Wed, 25 Jan 2017 19:07:25 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Wed, 25 Jan 2017 19:07:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2017 19:07:34 GMT
ENV GOSU_VERSION=1.7
# Wed, 25 Jan 2017 19:07:39 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Wed, 25 Jan 2017 19:07:39 GMT
ENV TINI_VERSION=v0.9.0
# Wed, 25 Jan 2017 19:07:42 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Wed, 25 Jan 2017 19:08:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2017 19:08:14 GMT
ENV RAILS_ENV=production
# Wed, 25 Jan 2017 19:08:14 GMT
WORKDIR /usr/src/redmine
# Wed, 25 Jan 2017 19:08:15 GMT
ENV REDMINE_VERSION=3.1.7
# Wed, 25 Jan 2017 19:08:15 GMT
ENV REDMINE_DOWNLOAD_MD5=625b7705b70521a205491a53f6df506a
# Wed, 25 Jan 2017 19:08:20 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Wed, 25 Jan 2017 19:10:38 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Wed, 25 Jan 2017 19:10:39 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 25 Jan 2017 19:10:40 GMT
COPY file:5efb6ca648b54af01740423ca0fdde905eae0ce732d8f2683c79dcf93e0e86c5 in / 
# Wed, 25 Jan 2017 19:10:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 25 Jan 2017 19:10:41 GMT
EXPOSE 3000/tcp
# Wed, 25 Jan 2017 19:10:41 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Wed, 25 Jan 2017 19:10:42 GMT
ENV PASSENGER_VERSION=5.1.2
# Wed, 25 Jan 2017 19:10:55 GMT
RUN buildDeps=' 		make 	' 	&& set -x 	&& apt-get update && apt-get install -y --no-install-recommends $buildDeps && rm -rf /var/lib/apt/lists/* 	&& gem install passenger --version "$PASSENGER_VERSION" 	&& apt-get purge -y --auto-remove $buildDeps
# Wed, 08 Feb 2017 21:47:09 GMT
RUN set -x 	&& passenger-config install-agent 	&& passenger-config download-nginx-engine
# Wed, 08 Feb 2017 21:47:10 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:5040bd2983909aa8896b9932438c3f1479d25ae837a5f6220242a264d0221f2d`  
		Last Modified: Mon, 16 Jan 2017 20:43:26 GMT  
		Size: 51.4 MB (51361210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596ec0bfbfe79e6bf8ba516cc80f14487c52f661c1c8f1dfdef2535f165beb56`  
		Last Modified: Wed, 18 Jan 2017 07:25:44 GMT  
		Size: 10.0 MB (9994242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330c0f0b9895c0a3df4249a9e2fe344e00dc43a4d9aac66506818ee0a8408043`  
		Last Modified: Wed, 18 Jan 2017 07:25:33 GMT  
		Size: 204.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759aaf3bf184b4692bcec722e430b1de0efcc5ebde1900ed83ef473c51d13d25`  
		Last Modified: Wed, 25 Jan 2017 18:33:14 GMT  
		Size: 33.3 MB (33326682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d391bd471e9bc64130a292130fcc4209eda0d1104ace90657ee4a56936cce2`  
		Last Modified: Wed, 25 Jan 2017 18:33:04 GMT  
		Size: 631.7 KB (631727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d548a23aa17d0f8419147686fdfa8b4f1637c6d592d2e13747c673f78a94b3c`  
		Last Modified: Wed, 25 Jan 2017 18:33:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548bf7ed54c4db146a49c6c74fd814210ff67320823ebf8dd5a5bae27bb62bb0`  
		Last Modified: Wed, 25 Jan 2017 19:16:08 GMT  
		Size: 2.0 KB (2043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42efbdc1be57cd208a79d1d7e3d07d83ecb18ae788b4f4b2ef0d6e4fdc86e4c0`  
		Last Modified: Wed, 25 Jan 2017 19:16:11 GMT  
		Size: 13.9 MB (13863641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c31ff7009497607f6e6e568d32553e37836e372cde3c5e53014f911ad6d69e`  
		Last Modified: Wed, 25 Jan 2017 19:16:06 GMT  
		Size: 807.9 KB (807934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdc0aa7eb6c6b4772890ecd81a8544f69d86e7aecf56b6be1c25088e4a4208e`  
		Last Modified: Wed, 25 Jan 2017 19:16:05 GMT  
		Size: 7.1 KB (7122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2bb7220f9b536cc758b25d7b5a65d33622e72ea714030de7cfcdb4e5ab9ae3`  
		Last Modified: Wed, 25 Jan 2017 19:16:22 GMT  
		Size: 58.2 MB (58213014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bd5e9fe51eb83c0111790e7dda6c778aa07e6d7699168b08dbc2c50680d231`  
		Last Modified: Wed, 25 Jan 2017 19:16:03 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15e90cfd31c4b0355bf7e9788a0a9d2ab7c2efb859af8806f2e510513669df4e`  
		Last Modified: Wed, 25 Jan 2017 19:16:04 GMT  
		Size: 2.3 MB (2273002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e883b45f83744b5f30735e7eeab28576446a7bed2ff97d39b5283116d2d171d`  
		Last Modified: Wed, 25 Jan 2017 19:16:22 GMT  
		Size: 67.0 MB (66995536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89bd3f9da8b1815cfbe74860d236a442fb1015102917a079c6ef6e956ea42b0b`  
		Last Modified: Wed, 25 Jan 2017 19:16:03 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64bef608e1afc0bfcc262567f25c3ba7a3f316c6ab684e53ff4f5a59eca3917`  
		Last Modified: Wed, 25 Jan 2017 19:17:00 GMT  
		Size: 15.5 MB (15504951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5a130dacc1ea6e98347b8b908fd11364388e02a863d29e6a0b0abd5e0c7b5f`  
		Last Modified: Wed, 08 Feb 2017 21:48:10 GMT  
		Size: 4.1 MB (4066210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:3.2.5`

```console
$ docker pull redmine@sha256:f8089a43e29971a19ee1ab6bad31f6f72039bb39a8ed19d009bb46c8740c03b0
```

-	Platforms:
	-	linux; amd64

### `redmine:3.2.5` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246332604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e84f17cd11e4f1a3d1fd8e5c9f73cc2518a990b229888870b7327282df6cbc2a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 16 Jan 2017 20:35:09 GMT
ADD file:89ecb642d662ee7edbb868340551106d51336c7e589fdaca4111725ec64da957 in / 
# Mon, 16 Jan 2017 20:35:16 GMT
CMD ["/bin/bash"]
# Tue, 17 Jan 2017 20:12:19 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Jan 2017 20:12:20 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 17 Jan 2017 20:17:55 GMT
ENV RUBY_MAJOR=2.2
# Tue, 17 Jan 2017 20:17:55 GMT
ENV RUBY_VERSION=2.2.6
# Tue, 17 Jan 2017 20:17:55 GMT
ENV RUBY_DOWNLOAD_SHA256=9414ecc0d09cf71c9a24e8dc82fcc87919ac7359fb08db2791d6c32bfd157339
# Wed, 25 Jan 2017 18:08:18 GMT
ENV RUBYGEMS_VERSION=2.6.10
# Wed, 25 Jan 2017 18:10:49 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& ./configure --disable-install-doc --enable-shared 	&& make -j"$(nproc)" 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION"
# Wed, 25 Jan 2017 18:10:49 GMT
ENV BUNDLER_VERSION=1.14.3
# Wed, 25 Jan 2017 18:10:50 GMT
RUN gem install bundler --version "$BUNDLER_VERSION"
# Wed, 25 Jan 2017 18:10:51 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 25 Jan 2017 18:10:51 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 25 Jan 2017 18:10:51 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Jan 2017 18:10:52 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Wed, 25 Jan 2017 18:10:52 GMT
CMD ["irb"]
# Wed, 25 Jan 2017 19:07:25 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Wed, 25 Jan 2017 19:07:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2017 19:07:34 GMT
ENV GOSU_VERSION=1.7
# Wed, 25 Jan 2017 19:07:39 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Wed, 25 Jan 2017 19:07:39 GMT
ENV TINI_VERSION=v0.9.0
# Wed, 25 Jan 2017 19:07:42 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Wed, 25 Jan 2017 19:08:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2017 19:08:14 GMT
ENV RAILS_ENV=production
# Wed, 25 Jan 2017 19:08:14 GMT
WORKDIR /usr/src/redmine
# Wed, 25 Jan 2017 19:10:58 GMT
ENV REDMINE_VERSION=3.2.5
# Wed, 25 Jan 2017 19:10:59 GMT
ENV REDMINE_DOWNLOAD_MD5=67e84e64828ebdea363443f9ee7c52ec
# Wed, 25 Jan 2017 19:11:03 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Wed, 25 Jan 2017 19:13:01 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Wed, 25 Jan 2017 19:13:02 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 25 Jan 2017 19:13:03 GMT
COPY file:5efb6ca648b54af01740423ca0fdde905eae0ce732d8f2683c79dcf93e0e86c5 in / 
# Wed, 25 Jan 2017 19:13:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 25 Jan 2017 19:13:04 GMT
EXPOSE 3000/tcp
# Wed, 25 Jan 2017 19:13:04 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5040bd2983909aa8896b9932438c3f1479d25ae837a5f6220242a264d0221f2d`  
		Last Modified: Mon, 16 Jan 2017 20:43:26 GMT  
		Size: 51.4 MB (51361210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596ec0bfbfe79e6bf8ba516cc80f14487c52f661c1c8f1dfdef2535f165beb56`  
		Last Modified: Wed, 18 Jan 2017 07:25:44 GMT  
		Size: 10.0 MB (9994242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330c0f0b9895c0a3df4249a9e2fe344e00dc43a4d9aac66506818ee0a8408043`  
		Last Modified: Wed, 18 Jan 2017 07:25:33 GMT  
		Size: 204.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759aaf3bf184b4692bcec722e430b1de0efcc5ebde1900ed83ef473c51d13d25`  
		Last Modified: Wed, 25 Jan 2017 18:33:14 GMT  
		Size: 33.3 MB (33326682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d391bd471e9bc64130a292130fcc4209eda0d1104ace90657ee4a56936cce2`  
		Last Modified: Wed, 25 Jan 2017 18:33:04 GMT  
		Size: 631.7 KB (631727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d548a23aa17d0f8419147686fdfa8b4f1637c6d592d2e13747c673f78a94b3c`  
		Last Modified: Wed, 25 Jan 2017 18:33:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548bf7ed54c4db146a49c6c74fd814210ff67320823ebf8dd5a5bae27bb62bb0`  
		Last Modified: Wed, 25 Jan 2017 19:16:08 GMT  
		Size: 2.0 KB (2043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42efbdc1be57cd208a79d1d7e3d07d83ecb18ae788b4f4b2ef0d6e4fdc86e4c0`  
		Last Modified: Wed, 25 Jan 2017 19:16:11 GMT  
		Size: 13.9 MB (13863641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c31ff7009497607f6e6e568d32553e37836e372cde3c5e53014f911ad6d69e`  
		Last Modified: Wed, 25 Jan 2017 19:16:06 GMT  
		Size: 807.9 KB (807934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdc0aa7eb6c6b4772890ecd81a8544f69d86e7aecf56b6be1c25088e4a4208e`  
		Last Modified: Wed, 25 Jan 2017 19:16:05 GMT  
		Size: 7.1 KB (7122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2bb7220f9b536cc758b25d7b5a65d33622e72ea714030de7cfcdb4e5ab9ae3`  
		Last Modified: Wed, 25 Jan 2017 19:16:22 GMT  
		Size: 58.2 MB (58213014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bd5e9fe51eb83c0111790e7dda6c778aa07e6d7699168b08dbc2c50680d231`  
		Last Modified: Wed, 25 Jan 2017 19:16:03 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d62e264e6f76678222bde23499b572b04b45b35b8b77002fa1075993ae909d`  
		Last Modified: Wed, 25 Jan 2017 19:17:36 GMT  
		Size: 2.3 MB (2334508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b700576a1cef435f0011cdc1bcde9012d651e2b46cff99ab46f01f0d5dcc4ea4`  
		Last Modified: Wed, 25 Jan 2017 19:17:49 GMT  
		Size: 75.8 MB (75788457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39ddd2d6aa6fbf28d32c47f3144058873eb54f0e087a2e525055802d16a55f0`  
		Last Modified: Wed, 25 Jan 2017 19:17:36 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:3.2`

```console
$ docker pull redmine@sha256:f8089a43e29971a19ee1ab6bad31f6f72039bb39a8ed19d009bb46c8740c03b0
```

-	Platforms:
	-	linux; amd64

### `redmine:3.2` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246332604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e84f17cd11e4f1a3d1fd8e5c9f73cc2518a990b229888870b7327282df6cbc2a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 16 Jan 2017 20:35:09 GMT
ADD file:89ecb642d662ee7edbb868340551106d51336c7e589fdaca4111725ec64da957 in / 
# Mon, 16 Jan 2017 20:35:16 GMT
CMD ["/bin/bash"]
# Tue, 17 Jan 2017 20:12:19 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Jan 2017 20:12:20 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 17 Jan 2017 20:17:55 GMT
ENV RUBY_MAJOR=2.2
# Tue, 17 Jan 2017 20:17:55 GMT
ENV RUBY_VERSION=2.2.6
# Tue, 17 Jan 2017 20:17:55 GMT
ENV RUBY_DOWNLOAD_SHA256=9414ecc0d09cf71c9a24e8dc82fcc87919ac7359fb08db2791d6c32bfd157339
# Wed, 25 Jan 2017 18:08:18 GMT
ENV RUBYGEMS_VERSION=2.6.10
# Wed, 25 Jan 2017 18:10:49 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& ./configure --disable-install-doc --enable-shared 	&& make -j"$(nproc)" 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION"
# Wed, 25 Jan 2017 18:10:49 GMT
ENV BUNDLER_VERSION=1.14.3
# Wed, 25 Jan 2017 18:10:50 GMT
RUN gem install bundler --version "$BUNDLER_VERSION"
# Wed, 25 Jan 2017 18:10:51 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 25 Jan 2017 18:10:51 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 25 Jan 2017 18:10:51 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Jan 2017 18:10:52 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Wed, 25 Jan 2017 18:10:52 GMT
CMD ["irb"]
# Wed, 25 Jan 2017 19:07:25 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Wed, 25 Jan 2017 19:07:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2017 19:07:34 GMT
ENV GOSU_VERSION=1.7
# Wed, 25 Jan 2017 19:07:39 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Wed, 25 Jan 2017 19:07:39 GMT
ENV TINI_VERSION=v0.9.0
# Wed, 25 Jan 2017 19:07:42 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Wed, 25 Jan 2017 19:08:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2017 19:08:14 GMT
ENV RAILS_ENV=production
# Wed, 25 Jan 2017 19:08:14 GMT
WORKDIR /usr/src/redmine
# Wed, 25 Jan 2017 19:10:58 GMT
ENV REDMINE_VERSION=3.2.5
# Wed, 25 Jan 2017 19:10:59 GMT
ENV REDMINE_DOWNLOAD_MD5=67e84e64828ebdea363443f9ee7c52ec
# Wed, 25 Jan 2017 19:11:03 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Wed, 25 Jan 2017 19:13:01 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Wed, 25 Jan 2017 19:13:02 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 25 Jan 2017 19:13:03 GMT
COPY file:5efb6ca648b54af01740423ca0fdde905eae0ce732d8f2683c79dcf93e0e86c5 in / 
# Wed, 25 Jan 2017 19:13:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 25 Jan 2017 19:13:04 GMT
EXPOSE 3000/tcp
# Wed, 25 Jan 2017 19:13:04 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5040bd2983909aa8896b9932438c3f1479d25ae837a5f6220242a264d0221f2d`  
		Last Modified: Mon, 16 Jan 2017 20:43:26 GMT  
		Size: 51.4 MB (51361210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596ec0bfbfe79e6bf8ba516cc80f14487c52f661c1c8f1dfdef2535f165beb56`  
		Last Modified: Wed, 18 Jan 2017 07:25:44 GMT  
		Size: 10.0 MB (9994242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330c0f0b9895c0a3df4249a9e2fe344e00dc43a4d9aac66506818ee0a8408043`  
		Last Modified: Wed, 18 Jan 2017 07:25:33 GMT  
		Size: 204.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759aaf3bf184b4692bcec722e430b1de0efcc5ebde1900ed83ef473c51d13d25`  
		Last Modified: Wed, 25 Jan 2017 18:33:14 GMT  
		Size: 33.3 MB (33326682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d391bd471e9bc64130a292130fcc4209eda0d1104ace90657ee4a56936cce2`  
		Last Modified: Wed, 25 Jan 2017 18:33:04 GMT  
		Size: 631.7 KB (631727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d548a23aa17d0f8419147686fdfa8b4f1637c6d592d2e13747c673f78a94b3c`  
		Last Modified: Wed, 25 Jan 2017 18:33:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548bf7ed54c4db146a49c6c74fd814210ff67320823ebf8dd5a5bae27bb62bb0`  
		Last Modified: Wed, 25 Jan 2017 19:16:08 GMT  
		Size: 2.0 KB (2043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42efbdc1be57cd208a79d1d7e3d07d83ecb18ae788b4f4b2ef0d6e4fdc86e4c0`  
		Last Modified: Wed, 25 Jan 2017 19:16:11 GMT  
		Size: 13.9 MB (13863641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c31ff7009497607f6e6e568d32553e37836e372cde3c5e53014f911ad6d69e`  
		Last Modified: Wed, 25 Jan 2017 19:16:06 GMT  
		Size: 807.9 KB (807934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdc0aa7eb6c6b4772890ecd81a8544f69d86e7aecf56b6be1c25088e4a4208e`  
		Last Modified: Wed, 25 Jan 2017 19:16:05 GMT  
		Size: 7.1 KB (7122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2bb7220f9b536cc758b25d7b5a65d33622e72ea714030de7cfcdb4e5ab9ae3`  
		Last Modified: Wed, 25 Jan 2017 19:16:22 GMT  
		Size: 58.2 MB (58213014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bd5e9fe51eb83c0111790e7dda6c778aa07e6d7699168b08dbc2c50680d231`  
		Last Modified: Wed, 25 Jan 2017 19:16:03 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d62e264e6f76678222bde23499b572b04b45b35b8b77002fa1075993ae909d`  
		Last Modified: Wed, 25 Jan 2017 19:17:36 GMT  
		Size: 2.3 MB (2334508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b700576a1cef435f0011cdc1bcde9012d651e2b46cff99ab46f01f0d5dcc4ea4`  
		Last Modified: Wed, 25 Jan 2017 19:17:49 GMT  
		Size: 75.8 MB (75788457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39ddd2d6aa6fbf28d32c47f3144058873eb54f0e087a2e525055802d16a55f0`  
		Last Modified: Wed, 25 Jan 2017 19:17:36 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:3.2.5-passenger`

```console
$ docker pull redmine@sha256:64f1c55f45bacedfce17cff986c91ad86df1c6a392ff008cbe9dc8c88bceaabe
```

-	Platforms:
	-	linux; amd64

### `redmine:3.2.5-passenger` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.9 MB (265903854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9beedd7ec70a50056a651af92980c3aeb6e9e232a1059eac38629e0e9bff1541`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Mon, 16 Jan 2017 20:35:09 GMT
ADD file:89ecb642d662ee7edbb868340551106d51336c7e589fdaca4111725ec64da957 in / 
# Mon, 16 Jan 2017 20:35:16 GMT
CMD ["/bin/bash"]
# Tue, 17 Jan 2017 20:12:19 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Jan 2017 20:12:20 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 17 Jan 2017 20:17:55 GMT
ENV RUBY_MAJOR=2.2
# Tue, 17 Jan 2017 20:17:55 GMT
ENV RUBY_VERSION=2.2.6
# Tue, 17 Jan 2017 20:17:55 GMT
ENV RUBY_DOWNLOAD_SHA256=9414ecc0d09cf71c9a24e8dc82fcc87919ac7359fb08db2791d6c32bfd157339
# Wed, 25 Jan 2017 18:08:18 GMT
ENV RUBYGEMS_VERSION=2.6.10
# Wed, 25 Jan 2017 18:10:49 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& ./configure --disable-install-doc --enable-shared 	&& make -j"$(nproc)" 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION"
# Wed, 25 Jan 2017 18:10:49 GMT
ENV BUNDLER_VERSION=1.14.3
# Wed, 25 Jan 2017 18:10:50 GMT
RUN gem install bundler --version "$BUNDLER_VERSION"
# Wed, 25 Jan 2017 18:10:51 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 25 Jan 2017 18:10:51 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 25 Jan 2017 18:10:51 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Jan 2017 18:10:52 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Wed, 25 Jan 2017 18:10:52 GMT
CMD ["irb"]
# Wed, 25 Jan 2017 19:07:25 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Wed, 25 Jan 2017 19:07:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2017 19:07:34 GMT
ENV GOSU_VERSION=1.7
# Wed, 25 Jan 2017 19:07:39 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Wed, 25 Jan 2017 19:07:39 GMT
ENV TINI_VERSION=v0.9.0
# Wed, 25 Jan 2017 19:07:42 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Wed, 25 Jan 2017 19:08:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2017 19:08:14 GMT
ENV RAILS_ENV=production
# Wed, 25 Jan 2017 19:08:14 GMT
WORKDIR /usr/src/redmine
# Wed, 25 Jan 2017 19:10:58 GMT
ENV REDMINE_VERSION=3.2.5
# Wed, 25 Jan 2017 19:10:59 GMT
ENV REDMINE_DOWNLOAD_MD5=67e84e64828ebdea363443f9ee7c52ec
# Wed, 25 Jan 2017 19:11:03 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Wed, 25 Jan 2017 19:13:01 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Wed, 25 Jan 2017 19:13:02 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 25 Jan 2017 19:13:03 GMT
COPY file:5efb6ca648b54af01740423ca0fdde905eae0ce732d8f2683c79dcf93e0e86c5 in / 
# Wed, 25 Jan 2017 19:13:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 25 Jan 2017 19:13:04 GMT
EXPOSE 3000/tcp
# Wed, 25 Jan 2017 19:13:04 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Wed, 25 Jan 2017 19:13:05 GMT
ENV PASSENGER_VERSION=5.1.2
# Wed, 25 Jan 2017 19:13:18 GMT
RUN buildDeps=' 		make 	' 	&& set -x 	&& apt-get update && apt-get install -y --no-install-recommends $buildDeps && rm -rf /var/lib/apt/lists/* 	&& gem install passenger --version "$PASSENGER_VERSION" 	&& apt-get purge -y --auto-remove $buildDeps
# Wed, 08 Feb 2017 21:47:12 GMT
RUN set -x 	&& passenger-config install-agent 	&& passenger-config download-nginx-engine
# Wed, 08 Feb 2017 21:47:13 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:5040bd2983909aa8896b9932438c3f1479d25ae837a5f6220242a264d0221f2d`  
		Last Modified: Mon, 16 Jan 2017 20:43:26 GMT  
		Size: 51.4 MB (51361210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596ec0bfbfe79e6bf8ba516cc80f14487c52f661c1c8f1dfdef2535f165beb56`  
		Last Modified: Wed, 18 Jan 2017 07:25:44 GMT  
		Size: 10.0 MB (9994242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330c0f0b9895c0a3df4249a9e2fe344e00dc43a4d9aac66506818ee0a8408043`  
		Last Modified: Wed, 18 Jan 2017 07:25:33 GMT  
		Size: 204.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759aaf3bf184b4692bcec722e430b1de0efcc5ebde1900ed83ef473c51d13d25`  
		Last Modified: Wed, 25 Jan 2017 18:33:14 GMT  
		Size: 33.3 MB (33326682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d391bd471e9bc64130a292130fcc4209eda0d1104ace90657ee4a56936cce2`  
		Last Modified: Wed, 25 Jan 2017 18:33:04 GMT  
		Size: 631.7 KB (631727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d548a23aa17d0f8419147686fdfa8b4f1637c6d592d2e13747c673f78a94b3c`  
		Last Modified: Wed, 25 Jan 2017 18:33:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548bf7ed54c4db146a49c6c74fd814210ff67320823ebf8dd5a5bae27bb62bb0`  
		Last Modified: Wed, 25 Jan 2017 19:16:08 GMT  
		Size: 2.0 KB (2043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42efbdc1be57cd208a79d1d7e3d07d83ecb18ae788b4f4b2ef0d6e4fdc86e4c0`  
		Last Modified: Wed, 25 Jan 2017 19:16:11 GMT  
		Size: 13.9 MB (13863641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c31ff7009497607f6e6e568d32553e37836e372cde3c5e53014f911ad6d69e`  
		Last Modified: Wed, 25 Jan 2017 19:16:06 GMT  
		Size: 807.9 KB (807934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdc0aa7eb6c6b4772890ecd81a8544f69d86e7aecf56b6be1c25088e4a4208e`  
		Last Modified: Wed, 25 Jan 2017 19:16:05 GMT  
		Size: 7.1 KB (7122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2bb7220f9b536cc758b25d7b5a65d33622e72ea714030de7cfcdb4e5ab9ae3`  
		Last Modified: Wed, 25 Jan 2017 19:16:22 GMT  
		Size: 58.2 MB (58213014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bd5e9fe51eb83c0111790e7dda6c778aa07e6d7699168b08dbc2c50680d231`  
		Last Modified: Wed, 25 Jan 2017 19:16:03 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d62e264e6f76678222bde23499b572b04b45b35b8b77002fa1075993ae909d`  
		Last Modified: Wed, 25 Jan 2017 19:17:36 GMT  
		Size: 2.3 MB (2334508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b700576a1cef435f0011cdc1bcde9012d651e2b46cff99ab46f01f0d5dcc4ea4`  
		Last Modified: Wed, 25 Jan 2017 19:17:49 GMT  
		Size: 75.8 MB (75788457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39ddd2d6aa6fbf28d32c47f3144058873eb54f0e087a2e525055802d16a55f0`  
		Last Modified: Wed, 25 Jan 2017 19:17:36 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:babb98cd4cd7fe96f282ca254392192d3a7d29197f9ad6014e772e4cc2fd57b5`  
		Last Modified: Wed, 25 Jan 2017 19:18:27 GMT  
		Size: 15.5 MB (15505032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d84015c5e544842a400d11b8f03a796e0bf5b557d31dbf1837fd744450a774cb`  
		Last Modified: Wed, 08 Feb 2017 21:49:20 GMT  
		Size: 4.1 MB (4066218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:3.2-passenger`

```console
$ docker pull redmine@sha256:64f1c55f45bacedfce17cff986c91ad86df1c6a392ff008cbe9dc8c88bceaabe
```

-	Platforms:
	-	linux; amd64

### `redmine:3.2-passenger` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.9 MB (265903854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9beedd7ec70a50056a651af92980c3aeb6e9e232a1059eac38629e0e9bff1541`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Mon, 16 Jan 2017 20:35:09 GMT
ADD file:89ecb642d662ee7edbb868340551106d51336c7e589fdaca4111725ec64da957 in / 
# Mon, 16 Jan 2017 20:35:16 GMT
CMD ["/bin/bash"]
# Tue, 17 Jan 2017 20:12:19 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Jan 2017 20:12:20 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 17 Jan 2017 20:17:55 GMT
ENV RUBY_MAJOR=2.2
# Tue, 17 Jan 2017 20:17:55 GMT
ENV RUBY_VERSION=2.2.6
# Tue, 17 Jan 2017 20:17:55 GMT
ENV RUBY_DOWNLOAD_SHA256=9414ecc0d09cf71c9a24e8dc82fcc87919ac7359fb08db2791d6c32bfd157339
# Wed, 25 Jan 2017 18:08:18 GMT
ENV RUBYGEMS_VERSION=2.6.10
# Wed, 25 Jan 2017 18:10:49 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& ./configure --disable-install-doc --enable-shared 	&& make -j"$(nproc)" 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION"
# Wed, 25 Jan 2017 18:10:49 GMT
ENV BUNDLER_VERSION=1.14.3
# Wed, 25 Jan 2017 18:10:50 GMT
RUN gem install bundler --version "$BUNDLER_VERSION"
# Wed, 25 Jan 2017 18:10:51 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 25 Jan 2017 18:10:51 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 25 Jan 2017 18:10:51 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Jan 2017 18:10:52 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Wed, 25 Jan 2017 18:10:52 GMT
CMD ["irb"]
# Wed, 25 Jan 2017 19:07:25 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Wed, 25 Jan 2017 19:07:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2017 19:07:34 GMT
ENV GOSU_VERSION=1.7
# Wed, 25 Jan 2017 19:07:39 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Wed, 25 Jan 2017 19:07:39 GMT
ENV TINI_VERSION=v0.9.0
# Wed, 25 Jan 2017 19:07:42 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Wed, 25 Jan 2017 19:08:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2017 19:08:14 GMT
ENV RAILS_ENV=production
# Wed, 25 Jan 2017 19:08:14 GMT
WORKDIR /usr/src/redmine
# Wed, 25 Jan 2017 19:10:58 GMT
ENV REDMINE_VERSION=3.2.5
# Wed, 25 Jan 2017 19:10:59 GMT
ENV REDMINE_DOWNLOAD_MD5=67e84e64828ebdea363443f9ee7c52ec
# Wed, 25 Jan 2017 19:11:03 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Wed, 25 Jan 2017 19:13:01 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Wed, 25 Jan 2017 19:13:02 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 25 Jan 2017 19:13:03 GMT
COPY file:5efb6ca648b54af01740423ca0fdde905eae0ce732d8f2683c79dcf93e0e86c5 in / 
# Wed, 25 Jan 2017 19:13:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 25 Jan 2017 19:13:04 GMT
EXPOSE 3000/tcp
# Wed, 25 Jan 2017 19:13:04 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Wed, 25 Jan 2017 19:13:05 GMT
ENV PASSENGER_VERSION=5.1.2
# Wed, 25 Jan 2017 19:13:18 GMT
RUN buildDeps=' 		make 	' 	&& set -x 	&& apt-get update && apt-get install -y --no-install-recommends $buildDeps && rm -rf /var/lib/apt/lists/* 	&& gem install passenger --version "$PASSENGER_VERSION" 	&& apt-get purge -y --auto-remove $buildDeps
# Wed, 08 Feb 2017 21:47:12 GMT
RUN set -x 	&& passenger-config install-agent 	&& passenger-config download-nginx-engine
# Wed, 08 Feb 2017 21:47:13 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:5040bd2983909aa8896b9932438c3f1479d25ae837a5f6220242a264d0221f2d`  
		Last Modified: Mon, 16 Jan 2017 20:43:26 GMT  
		Size: 51.4 MB (51361210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596ec0bfbfe79e6bf8ba516cc80f14487c52f661c1c8f1dfdef2535f165beb56`  
		Last Modified: Wed, 18 Jan 2017 07:25:44 GMT  
		Size: 10.0 MB (9994242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330c0f0b9895c0a3df4249a9e2fe344e00dc43a4d9aac66506818ee0a8408043`  
		Last Modified: Wed, 18 Jan 2017 07:25:33 GMT  
		Size: 204.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759aaf3bf184b4692bcec722e430b1de0efcc5ebde1900ed83ef473c51d13d25`  
		Last Modified: Wed, 25 Jan 2017 18:33:14 GMT  
		Size: 33.3 MB (33326682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d391bd471e9bc64130a292130fcc4209eda0d1104ace90657ee4a56936cce2`  
		Last Modified: Wed, 25 Jan 2017 18:33:04 GMT  
		Size: 631.7 KB (631727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d548a23aa17d0f8419147686fdfa8b4f1637c6d592d2e13747c673f78a94b3c`  
		Last Modified: Wed, 25 Jan 2017 18:33:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548bf7ed54c4db146a49c6c74fd814210ff67320823ebf8dd5a5bae27bb62bb0`  
		Last Modified: Wed, 25 Jan 2017 19:16:08 GMT  
		Size: 2.0 KB (2043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42efbdc1be57cd208a79d1d7e3d07d83ecb18ae788b4f4b2ef0d6e4fdc86e4c0`  
		Last Modified: Wed, 25 Jan 2017 19:16:11 GMT  
		Size: 13.9 MB (13863641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c31ff7009497607f6e6e568d32553e37836e372cde3c5e53014f911ad6d69e`  
		Last Modified: Wed, 25 Jan 2017 19:16:06 GMT  
		Size: 807.9 KB (807934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdc0aa7eb6c6b4772890ecd81a8544f69d86e7aecf56b6be1c25088e4a4208e`  
		Last Modified: Wed, 25 Jan 2017 19:16:05 GMT  
		Size: 7.1 KB (7122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2bb7220f9b536cc758b25d7b5a65d33622e72ea714030de7cfcdb4e5ab9ae3`  
		Last Modified: Wed, 25 Jan 2017 19:16:22 GMT  
		Size: 58.2 MB (58213014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bd5e9fe51eb83c0111790e7dda6c778aa07e6d7699168b08dbc2c50680d231`  
		Last Modified: Wed, 25 Jan 2017 19:16:03 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d62e264e6f76678222bde23499b572b04b45b35b8b77002fa1075993ae909d`  
		Last Modified: Wed, 25 Jan 2017 19:17:36 GMT  
		Size: 2.3 MB (2334508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b700576a1cef435f0011cdc1bcde9012d651e2b46cff99ab46f01f0d5dcc4ea4`  
		Last Modified: Wed, 25 Jan 2017 19:17:49 GMT  
		Size: 75.8 MB (75788457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39ddd2d6aa6fbf28d32c47f3144058873eb54f0e087a2e525055802d16a55f0`  
		Last Modified: Wed, 25 Jan 2017 19:17:36 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:babb98cd4cd7fe96f282ca254392192d3a7d29197f9ad6014e772e4cc2fd57b5`  
		Last Modified: Wed, 25 Jan 2017 19:18:27 GMT  
		Size: 15.5 MB (15505032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d84015c5e544842a400d11b8f03a796e0bf5b557d31dbf1837fd744450a774cb`  
		Last Modified: Wed, 08 Feb 2017 21:49:20 GMT  
		Size: 4.1 MB (4066218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:3.3.2`

```console
$ docker pull redmine@sha256:b30cbded7ec15fda443b0b7ebda9de49a328f41001e11c0d283ea557e06f1225
```

-	Platforms:
	-	linux; amd64

### `redmine:3.3.2` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 MB (246374974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d77e501729aad31ae586e72e4f2eafcaadafa6cc379f332c8e768f889272a9f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 16 Jan 2017 20:35:09 GMT
ADD file:89ecb642d662ee7edbb868340551106d51336c7e589fdaca4111725ec64da957 in / 
# Mon, 16 Jan 2017 20:35:16 GMT
CMD ["/bin/bash"]
# Tue, 17 Jan 2017 20:12:19 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Jan 2017 20:12:20 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 17 Jan 2017 20:17:55 GMT
ENV RUBY_MAJOR=2.2
# Tue, 17 Jan 2017 20:17:55 GMT
ENV RUBY_VERSION=2.2.6
# Tue, 17 Jan 2017 20:17:55 GMT
ENV RUBY_DOWNLOAD_SHA256=9414ecc0d09cf71c9a24e8dc82fcc87919ac7359fb08db2791d6c32bfd157339
# Wed, 25 Jan 2017 18:08:18 GMT
ENV RUBYGEMS_VERSION=2.6.10
# Wed, 25 Jan 2017 18:10:49 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& ./configure --disable-install-doc --enable-shared 	&& make -j"$(nproc)" 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION"
# Wed, 25 Jan 2017 18:10:49 GMT
ENV BUNDLER_VERSION=1.14.3
# Wed, 25 Jan 2017 18:10:50 GMT
RUN gem install bundler --version "$BUNDLER_VERSION"
# Wed, 25 Jan 2017 18:10:51 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 25 Jan 2017 18:10:51 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 25 Jan 2017 18:10:51 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Jan 2017 18:10:52 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Wed, 25 Jan 2017 18:10:52 GMT
CMD ["irb"]
# Wed, 25 Jan 2017 19:07:25 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Wed, 25 Jan 2017 19:07:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2017 19:07:34 GMT
ENV GOSU_VERSION=1.7
# Wed, 25 Jan 2017 19:07:39 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Wed, 25 Jan 2017 19:07:39 GMT
ENV TINI_VERSION=v0.9.0
# Wed, 25 Jan 2017 19:07:42 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Wed, 25 Jan 2017 19:08:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2017 19:08:14 GMT
ENV RAILS_ENV=production
# Wed, 25 Jan 2017 19:08:14 GMT
WORKDIR /usr/src/redmine
# Wed, 25 Jan 2017 19:13:21 GMT
ENV REDMINE_VERSION=3.3.2
# Wed, 25 Jan 2017 19:13:21 GMT
ENV REDMINE_DOWNLOAD_MD5=8e403981dc3a19a42ee978f055be62ca
# Wed, 25 Jan 2017 19:13:25 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Wed, 25 Jan 2017 19:15:29 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Wed, 25 Jan 2017 19:15:30 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 25 Jan 2017 19:15:30 GMT
COPY file:5efb6ca648b54af01740423ca0fdde905eae0ce732d8f2683c79dcf93e0e86c5 in / 
# Wed, 25 Jan 2017 19:15:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 25 Jan 2017 19:15:31 GMT
EXPOSE 3000/tcp
# Wed, 25 Jan 2017 19:15:31 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5040bd2983909aa8896b9932438c3f1479d25ae837a5f6220242a264d0221f2d`  
		Last Modified: Mon, 16 Jan 2017 20:43:26 GMT  
		Size: 51.4 MB (51361210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596ec0bfbfe79e6bf8ba516cc80f14487c52f661c1c8f1dfdef2535f165beb56`  
		Last Modified: Wed, 18 Jan 2017 07:25:44 GMT  
		Size: 10.0 MB (9994242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330c0f0b9895c0a3df4249a9e2fe344e00dc43a4d9aac66506818ee0a8408043`  
		Last Modified: Wed, 18 Jan 2017 07:25:33 GMT  
		Size: 204.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759aaf3bf184b4692bcec722e430b1de0efcc5ebde1900ed83ef473c51d13d25`  
		Last Modified: Wed, 25 Jan 2017 18:33:14 GMT  
		Size: 33.3 MB (33326682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d391bd471e9bc64130a292130fcc4209eda0d1104ace90657ee4a56936cce2`  
		Last Modified: Wed, 25 Jan 2017 18:33:04 GMT  
		Size: 631.7 KB (631727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d548a23aa17d0f8419147686fdfa8b4f1637c6d592d2e13747c673f78a94b3c`  
		Last Modified: Wed, 25 Jan 2017 18:33:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548bf7ed54c4db146a49c6c74fd814210ff67320823ebf8dd5a5bae27bb62bb0`  
		Last Modified: Wed, 25 Jan 2017 19:16:08 GMT  
		Size: 2.0 KB (2043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42efbdc1be57cd208a79d1d7e3d07d83ecb18ae788b4f4b2ef0d6e4fdc86e4c0`  
		Last Modified: Wed, 25 Jan 2017 19:16:11 GMT  
		Size: 13.9 MB (13863641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c31ff7009497607f6e6e568d32553e37836e372cde3c5e53014f911ad6d69e`  
		Last Modified: Wed, 25 Jan 2017 19:16:06 GMT  
		Size: 807.9 KB (807934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdc0aa7eb6c6b4772890ecd81a8544f69d86e7aecf56b6be1c25088e4a4208e`  
		Last Modified: Wed, 25 Jan 2017 19:16:05 GMT  
		Size: 7.1 KB (7122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2bb7220f9b536cc758b25d7b5a65d33622e72ea714030de7cfcdb4e5ab9ae3`  
		Last Modified: Wed, 25 Jan 2017 19:16:22 GMT  
		Size: 58.2 MB (58213014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bd5e9fe51eb83c0111790e7dda6c778aa07e6d7699168b08dbc2c50680d231`  
		Last Modified: Wed, 25 Jan 2017 19:16:03 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc502bf8c5ab1e8a7c2277b45dff3cb372c79eea75c1ee27de940d8c0ad49159`  
		Last Modified: Wed, 25 Jan 2017 19:19:04 GMT  
		Size: 2.4 MB (2376996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c88d95529382256ccc7d960f0581829e24584a7722aca63ee4cc10e38ab0f4f0`  
		Last Modified: Wed, 25 Jan 2017 19:19:16 GMT  
		Size: 75.8 MB (75788340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3560bd24100c45be977767a24def1c6c3d241299c530a8d890ca8002a10cd52b`  
		Last Modified: Wed, 25 Jan 2017 19:19:02 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:3.3`

```console
$ docker pull redmine@sha256:b30cbded7ec15fda443b0b7ebda9de49a328f41001e11c0d283ea557e06f1225
```

-	Platforms:
	-	linux; amd64

### `redmine:3.3` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 MB (246374974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d77e501729aad31ae586e72e4f2eafcaadafa6cc379f332c8e768f889272a9f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 16 Jan 2017 20:35:09 GMT
ADD file:89ecb642d662ee7edbb868340551106d51336c7e589fdaca4111725ec64da957 in / 
# Mon, 16 Jan 2017 20:35:16 GMT
CMD ["/bin/bash"]
# Tue, 17 Jan 2017 20:12:19 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Jan 2017 20:12:20 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 17 Jan 2017 20:17:55 GMT
ENV RUBY_MAJOR=2.2
# Tue, 17 Jan 2017 20:17:55 GMT
ENV RUBY_VERSION=2.2.6
# Tue, 17 Jan 2017 20:17:55 GMT
ENV RUBY_DOWNLOAD_SHA256=9414ecc0d09cf71c9a24e8dc82fcc87919ac7359fb08db2791d6c32bfd157339
# Wed, 25 Jan 2017 18:08:18 GMT
ENV RUBYGEMS_VERSION=2.6.10
# Wed, 25 Jan 2017 18:10:49 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& ./configure --disable-install-doc --enable-shared 	&& make -j"$(nproc)" 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION"
# Wed, 25 Jan 2017 18:10:49 GMT
ENV BUNDLER_VERSION=1.14.3
# Wed, 25 Jan 2017 18:10:50 GMT
RUN gem install bundler --version "$BUNDLER_VERSION"
# Wed, 25 Jan 2017 18:10:51 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 25 Jan 2017 18:10:51 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 25 Jan 2017 18:10:51 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Jan 2017 18:10:52 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Wed, 25 Jan 2017 18:10:52 GMT
CMD ["irb"]
# Wed, 25 Jan 2017 19:07:25 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Wed, 25 Jan 2017 19:07:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2017 19:07:34 GMT
ENV GOSU_VERSION=1.7
# Wed, 25 Jan 2017 19:07:39 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Wed, 25 Jan 2017 19:07:39 GMT
ENV TINI_VERSION=v0.9.0
# Wed, 25 Jan 2017 19:07:42 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Wed, 25 Jan 2017 19:08:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2017 19:08:14 GMT
ENV RAILS_ENV=production
# Wed, 25 Jan 2017 19:08:14 GMT
WORKDIR /usr/src/redmine
# Wed, 25 Jan 2017 19:13:21 GMT
ENV REDMINE_VERSION=3.3.2
# Wed, 25 Jan 2017 19:13:21 GMT
ENV REDMINE_DOWNLOAD_MD5=8e403981dc3a19a42ee978f055be62ca
# Wed, 25 Jan 2017 19:13:25 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Wed, 25 Jan 2017 19:15:29 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Wed, 25 Jan 2017 19:15:30 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 25 Jan 2017 19:15:30 GMT
COPY file:5efb6ca648b54af01740423ca0fdde905eae0ce732d8f2683c79dcf93e0e86c5 in / 
# Wed, 25 Jan 2017 19:15:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 25 Jan 2017 19:15:31 GMT
EXPOSE 3000/tcp
# Wed, 25 Jan 2017 19:15:31 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5040bd2983909aa8896b9932438c3f1479d25ae837a5f6220242a264d0221f2d`  
		Last Modified: Mon, 16 Jan 2017 20:43:26 GMT  
		Size: 51.4 MB (51361210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596ec0bfbfe79e6bf8ba516cc80f14487c52f661c1c8f1dfdef2535f165beb56`  
		Last Modified: Wed, 18 Jan 2017 07:25:44 GMT  
		Size: 10.0 MB (9994242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330c0f0b9895c0a3df4249a9e2fe344e00dc43a4d9aac66506818ee0a8408043`  
		Last Modified: Wed, 18 Jan 2017 07:25:33 GMT  
		Size: 204.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759aaf3bf184b4692bcec722e430b1de0efcc5ebde1900ed83ef473c51d13d25`  
		Last Modified: Wed, 25 Jan 2017 18:33:14 GMT  
		Size: 33.3 MB (33326682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d391bd471e9bc64130a292130fcc4209eda0d1104ace90657ee4a56936cce2`  
		Last Modified: Wed, 25 Jan 2017 18:33:04 GMT  
		Size: 631.7 KB (631727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d548a23aa17d0f8419147686fdfa8b4f1637c6d592d2e13747c673f78a94b3c`  
		Last Modified: Wed, 25 Jan 2017 18:33:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548bf7ed54c4db146a49c6c74fd814210ff67320823ebf8dd5a5bae27bb62bb0`  
		Last Modified: Wed, 25 Jan 2017 19:16:08 GMT  
		Size: 2.0 KB (2043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42efbdc1be57cd208a79d1d7e3d07d83ecb18ae788b4f4b2ef0d6e4fdc86e4c0`  
		Last Modified: Wed, 25 Jan 2017 19:16:11 GMT  
		Size: 13.9 MB (13863641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c31ff7009497607f6e6e568d32553e37836e372cde3c5e53014f911ad6d69e`  
		Last Modified: Wed, 25 Jan 2017 19:16:06 GMT  
		Size: 807.9 KB (807934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdc0aa7eb6c6b4772890ecd81a8544f69d86e7aecf56b6be1c25088e4a4208e`  
		Last Modified: Wed, 25 Jan 2017 19:16:05 GMT  
		Size: 7.1 KB (7122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2bb7220f9b536cc758b25d7b5a65d33622e72ea714030de7cfcdb4e5ab9ae3`  
		Last Modified: Wed, 25 Jan 2017 19:16:22 GMT  
		Size: 58.2 MB (58213014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bd5e9fe51eb83c0111790e7dda6c778aa07e6d7699168b08dbc2c50680d231`  
		Last Modified: Wed, 25 Jan 2017 19:16:03 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc502bf8c5ab1e8a7c2277b45dff3cb372c79eea75c1ee27de940d8c0ad49159`  
		Last Modified: Wed, 25 Jan 2017 19:19:04 GMT  
		Size: 2.4 MB (2376996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c88d95529382256ccc7d960f0581829e24584a7722aca63ee4cc10e38ab0f4f0`  
		Last Modified: Wed, 25 Jan 2017 19:19:16 GMT  
		Size: 75.8 MB (75788340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3560bd24100c45be977767a24def1c6c3d241299c530a8d890ca8002a10cd52b`  
		Last Modified: Wed, 25 Jan 2017 19:19:02 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:3`

```console
$ docker pull redmine@sha256:b30cbded7ec15fda443b0b7ebda9de49a328f41001e11c0d283ea557e06f1225
```

-	Platforms:
	-	linux; amd64

### `redmine:3` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 MB (246374974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d77e501729aad31ae586e72e4f2eafcaadafa6cc379f332c8e768f889272a9f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 16 Jan 2017 20:35:09 GMT
ADD file:89ecb642d662ee7edbb868340551106d51336c7e589fdaca4111725ec64da957 in / 
# Mon, 16 Jan 2017 20:35:16 GMT
CMD ["/bin/bash"]
# Tue, 17 Jan 2017 20:12:19 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Jan 2017 20:12:20 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 17 Jan 2017 20:17:55 GMT
ENV RUBY_MAJOR=2.2
# Tue, 17 Jan 2017 20:17:55 GMT
ENV RUBY_VERSION=2.2.6
# Tue, 17 Jan 2017 20:17:55 GMT
ENV RUBY_DOWNLOAD_SHA256=9414ecc0d09cf71c9a24e8dc82fcc87919ac7359fb08db2791d6c32bfd157339
# Wed, 25 Jan 2017 18:08:18 GMT
ENV RUBYGEMS_VERSION=2.6.10
# Wed, 25 Jan 2017 18:10:49 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& ./configure --disable-install-doc --enable-shared 	&& make -j"$(nproc)" 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION"
# Wed, 25 Jan 2017 18:10:49 GMT
ENV BUNDLER_VERSION=1.14.3
# Wed, 25 Jan 2017 18:10:50 GMT
RUN gem install bundler --version "$BUNDLER_VERSION"
# Wed, 25 Jan 2017 18:10:51 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 25 Jan 2017 18:10:51 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 25 Jan 2017 18:10:51 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Jan 2017 18:10:52 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Wed, 25 Jan 2017 18:10:52 GMT
CMD ["irb"]
# Wed, 25 Jan 2017 19:07:25 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Wed, 25 Jan 2017 19:07:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2017 19:07:34 GMT
ENV GOSU_VERSION=1.7
# Wed, 25 Jan 2017 19:07:39 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Wed, 25 Jan 2017 19:07:39 GMT
ENV TINI_VERSION=v0.9.0
# Wed, 25 Jan 2017 19:07:42 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Wed, 25 Jan 2017 19:08:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2017 19:08:14 GMT
ENV RAILS_ENV=production
# Wed, 25 Jan 2017 19:08:14 GMT
WORKDIR /usr/src/redmine
# Wed, 25 Jan 2017 19:13:21 GMT
ENV REDMINE_VERSION=3.3.2
# Wed, 25 Jan 2017 19:13:21 GMT
ENV REDMINE_DOWNLOAD_MD5=8e403981dc3a19a42ee978f055be62ca
# Wed, 25 Jan 2017 19:13:25 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Wed, 25 Jan 2017 19:15:29 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Wed, 25 Jan 2017 19:15:30 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 25 Jan 2017 19:15:30 GMT
COPY file:5efb6ca648b54af01740423ca0fdde905eae0ce732d8f2683c79dcf93e0e86c5 in / 
# Wed, 25 Jan 2017 19:15:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 25 Jan 2017 19:15:31 GMT
EXPOSE 3000/tcp
# Wed, 25 Jan 2017 19:15:31 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5040bd2983909aa8896b9932438c3f1479d25ae837a5f6220242a264d0221f2d`  
		Last Modified: Mon, 16 Jan 2017 20:43:26 GMT  
		Size: 51.4 MB (51361210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596ec0bfbfe79e6bf8ba516cc80f14487c52f661c1c8f1dfdef2535f165beb56`  
		Last Modified: Wed, 18 Jan 2017 07:25:44 GMT  
		Size: 10.0 MB (9994242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330c0f0b9895c0a3df4249a9e2fe344e00dc43a4d9aac66506818ee0a8408043`  
		Last Modified: Wed, 18 Jan 2017 07:25:33 GMT  
		Size: 204.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759aaf3bf184b4692bcec722e430b1de0efcc5ebde1900ed83ef473c51d13d25`  
		Last Modified: Wed, 25 Jan 2017 18:33:14 GMT  
		Size: 33.3 MB (33326682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d391bd471e9bc64130a292130fcc4209eda0d1104ace90657ee4a56936cce2`  
		Last Modified: Wed, 25 Jan 2017 18:33:04 GMT  
		Size: 631.7 KB (631727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d548a23aa17d0f8419147686fdfa8b4f1637c6d592d2e13747c673f78a94b3c`  
		Last Modified: Wed, 25 Jan 2017 18:33:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548bf7ed54c4db146a49c6c74fd814210ff67320823ebf8dd5a5bae27bb62bb0`  
		Last Modified: Wed, 25 Jan 2017 19:16:08 GMT  
		Size: 2.0 KB (2043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42efbdc1be57cd208a79d1d7e3d07d83ecb18ae788b4f4b2ef0d6e4fdc86e4c0`  
		Last Modified: Wed, 25 Jan 2017 19:16:11 GMT  
		Size: 13.9 MB (13863641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c31ff7009497607f6e6e568d32553e37836e372cde3c5e53014f911ad6d69e`  
		Last Modified: Wed, 25 Jan 2017 19:16:06 GMT  
		Size: 807.9 KB (807934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdc0aa7eb6c6b4772890ecd81a8544f69d86e7aecf56b6be1c25088e4a4208e`  
		Last Modified: Wed, 25 Jan 2017 19:16:05 GMT  
		Size: 7.1 KB (7122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2bb7220f9b536cc758b25d7b5a65d33622e72ea714030de7cfcdb4e5ab9ae3`  
		Last Modified: Wed, 25 Jan 2017 19:16:22 GMT  
		Size: 58.2 MB (58213014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bd5e9fe51eb83c0111790e7dda6c778aa07e6d7699168b08dbc2c50680d231`  
		Last Modified: Wed, 25 Jan 2017 19:16:03 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc502bf8c5ab1e8a7c2277b45dff3cb372c79eea75c1ee27de940d8c0ad49159`  
		Last Modified: Wed, 25 Jan 2017 19:19:04 GMT  
		Size: 2.4 MB (2376996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c88d95529382256ccc7d960f0581829e24584a7722aca63ee4cc10e38ab0f4f0`  
		Last Modified: Wed, 25 Jan 2017 19:19:16 GMT  
		Size: 75.8 MB (75788340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3560bd24100c45be977767a24def1c6c3d241299c530a8d890ca8002a10cd52b`  
		Last Modified: Wed, 25 Jan 2017 19:19:02 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:latest`

```console
$ docker pull redmine@sha256:b30cbded7ec15fda443b0b7ebda9de49a328f41001e11c0d283ea557e06f1225
```

-	Platforms:
	-	linux; amd64

### `redmine:latest` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 MB (246374974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d77e501729aad31ae586e72e4f2eafcaadafa6cc379f332c8e768f889272a9f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 16 Jan 2017 20:35:09 GMT
ADD file:89ecb642d662ee7edbb868340551106d51336c7e589fdaca4111725ec64da957 in / 
# Mon, 16 Jan 2017 20:35:16 GMT
CMD ["/bin/bash"]
# Tue, 17 Jan 2017 20:12:19 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Jan 2017 20:12:20 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 17 Jan 2017 20:17:55 GMT
ENV RUBY_MAJOR=2.2
# Tue, 17 Jan 2017 20:17:55 GMT
ENV RUBY_VERSION=2.2.6
# Tue, 17 Jan 2017 20:17:55 GMT
ENV RUBY_DOWNLOAD_SHA256=9414ecc0d09cf71c9a24e8dc82fcc87919ac7359fb08db2791d6c32bfd157339
# Wed, 25 Jan 2017 18:08:18 GMT
ENV RUBYGEMS_VERSION=2.6.10
# Wed, 25 Jan 2017 18:10:49 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& ./configure --disable-install-doc --enable-shared 	&& make -j"$(nproc)" 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION"
# Wed, 25 Jan 2017 18:10:49 GMT
ENV BUNDLER_VERSION=1.14.3
# Wed, 25 Jan 2017 18:10:50 GMT
RUN gem install bundler --version "$BUNDLER_VERSION"
# Wed, 25 Jan 2017 18:10:51 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 25 Jan 2017 18:10:51 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 25 Jan 2017 18:10:51 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Jan 2017 18:10:52 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Wed, 25 Jan 2017 18:10:52 GMT
CMD ["irb"]
# Wed, 25 Jan 2017 19:07:25 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Wed, 25 Jan 2017 19:07:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2017 19:07:34 GMT
ENV GOSU_VERSION=1.7
# Wed, 25 Jan 2017 19:07:39 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Wed, 25 Jan 2017 19:07:39 GMT
ENV TINI_VERSION=v0.9.0
# Wed, 25 Jan 2017 19:07:42 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Wed, 25 Jan 2017 19:08:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2017 19:08:14 GMT
ENV RAILS_ENV=production
# Wed, 25 Jan 2017 19:08:14 GMT
WORKDIR /usr/src/redmine
# Wed, 25 Jan 2017 19:13:21 GMT
ENV REDMINE_VERSION=3.3.2
# Wed, 25 Jan 2017 19:13:21 GMT
ENV REDMINE_DOWNLOAD_MD5=8e403981dc3a19a42ee978f055be62ca
# Wed, 25 Jan 2017 19:13:25 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Wed, 25 Jan 2017 19:15:29 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Wed, 25 Jan 2017 19:15:30 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 25 Jan 2017 19:15:30 GMT
COPY file:5efb6ca648b54af01740423ca0fdde905eae0ce732d8f2683c79dcf93e0e86c5 in / 
# Wed, 25 Jan 2017 19:15:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 25 Jan 2017 19:15:31 GMT
EXPOSE 3000/tcp
# Wed, 25 Jan 2017 19:15:31 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5040bd2983909aa8896b9932438c3f1479d25ae837a5f6220242a264d0221f2d`  
		Last Modified: Mon, 16 Jan 2017 20:43:26 GMT  
		Size: 51.4 MB (51361210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596ec0bfbfe79e6bf8ba516cc80f14487c52f661c1c8f1dfdef2535f165beb56`  
		Last Modified: Wed, 18 Jan 2017 07:25:44 GMT  
		Size: 10.0 MB (9994242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330c0f0b9895c0a3df4249a9e2fe344e00dc43a4d9aac66506818ee0a8408043`  
		Last Modified: Wed, 18 Jan 2017 07:25:33 GMT  
		Size: 204.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759aaf3bf184b4692bcec722e430b1de0efcc5ebde1900ed83ef473c51d13d25`  
		Last Modified: Wed, 25 Jan 2017 18:33:14 GMT  
		Size: 33.3 MB (33326682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d391bd471e9bc64130a292130fcc4209eda0d1104ace90657ee4a56936cce2`  
		Last Modified: Wed, 25 Jan 2017 18:33:04 GMT  
		Size: 631.7 KB (631727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d548a23aa17d0f8419147686fdfa8b4f1637c6d592d2e13747c673f78a94b3c`  
		Last Modified: Wed, 25 Jan 2017 18:33:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548bf7ed54c4db146a49c6c74fd814210ff67320823ebf8dd5a5bae27bb62bb0`  
		Last Modified: Wed, 25 Jan 2017 19:16:08 GMT  
		Size: 2.0 KB (2043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42efbdc1be57cd208a79d1d7e3d07d83ecb18ae788b4f4b2ef0d6e4fdc86e4c0`  
		Last Modified: Wed, 25 Jan 2017 19:16:11 GMT  
		Size: 13.9 MB (13863641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c31ff7009497607f6e6e568d32553e37836e372cde3c5e53014f911ad6d69e`  
		Last Modified: Wed, 25 Jan 2017 19:16:06 GMT  
		Size: 807.9 KB (807934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdc0aa7eb6c6b4772890ecd81a8544f69d86e7aecf56b6be1c25088e4a4208e`  
		Last Modified: Wed, 25 Jan 2017 19:16:05 GMT  
		Size: 7.1 KB (7122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2bb7220f9b536cc758b25d7b5a65d33622e72ea714030de7cfcdb4e5ab9ae3`  
		Last Modified: Wed, 25 Jan 2017 19:16:22 GMT  
		Size: 58.2 MB (58213014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bd5e9fe51eb83c0111790e7dda6c778aa07e6d7699168b08dbc2c50680d231`  
		Last Modified: Wed, 25 Jan 2017 19:16:03 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc502bf8c5ab1e8a7c2277b45dff3cb372c79eea75c1ee27de940d8c0ad49159`  
		Last Modified: Wed, 25 Jan 2017 19:19:04 GMT  
		Size: 2.4 MB (2376996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c88d95529382256ccc7d960f0581829e24584a7722aca63ee4cc10e38ab0f4f0`  
		Last Modified: Wed, 25 Jan 2017 19:19:16 GMT  
		Size: 75.8 MB (75788340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3560bd24100c45be977767a24def1c6c3d241299c530a8d890ca8002a10cd52b`  
		Last Modified: Wed, 25 Jan 2017 19:19:02 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:3.3.2-passenger`

```console
$ docker pull redmine@sha256:959f658676033254221d5db8fd4970fc7037eeec4b87a1c4266f71db94d8f685
```

-	Platforms:
	-	linux; amd64

### `redmine:3.3.2-passenger` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.9 MB (265946222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64c6305b6d97f2bc923df2ef9e671a81602af45f07392a67ed3a466b8a9d16d0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Mon, 16 Jan 2017 20:35:09 GMT
ADD file:89ecb642d662ee7edbb868340551106d51336c7e589fdaca4111725ec64da957 in / 
# Mon, 16 Jan 2017 20:35:16 GMT
CMD ["/bin/bash"]
# Tue, 17 Jan 2017 20:12:19 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Jan 2017 20:12:20 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 17 Jan 2017 20:17:55 GMT
ENV RUBY_MAJOR=2.2
# Tue, 17 Jan 2017 20:17:55 GMT
ENV RUBY_VERSION=2.2.6
# Tue, 17 Jan 2017 20:17:55 GMT
ENV RUBY_DOWNLOAD_SHA256=9414ecc0d09cf71c9a24e8dc82fcc87919ac7359fb08db2791d6c32bfd157339
# Wed, 25 Jan 2017 18:08:18 GMT
ENV RUBYGEMS_VERSION=2.6.10
# Wed, 25 Jan 2017 18:10:49 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& ./configure --disable-install-doc --enable-shared 	&& make -j"$(nproc)" 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION"
# Wed, 25 Jan 2017 18:10:49 GMT
ENV BUNDLER_VERSION=1.14.3
# Wed, 25 Jan 2017 18:10:50 GMT
RUN gem install bundler --version "$BUNDLER_VERSION"
# Wed, 25 Jan 2017 18:10:51 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 25 Jan 2017 18:10:51 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 25 Jan 2017 18:10:51 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Jan 2017 18:10:52 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Wed, 25 Jan 2017 18:10:52 GMT
CMD ["irb"]
# Wed, 25 Jan 2017 19:07:25 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Wed, 25 Jan 2017 19:07:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2017 19:07:34 GMT
ENV GOSU_VERSION=1.7
# Wed, 25 Jan 2017 19:07:39 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Wed, 25 Jan 2017 19:07:39 GMT
ENV TINI_VERSION=v0.9.0
# Wed, 25 Jan 2017 19:07:42 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Wed, 25 Jan 2017 19:08:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2017 19:08:14 GMT
ENV RAILS_ENV=production
# Wed, 25 Jan 2017 19:08:14 GMT
WORKDIR /usr/src/redmine
# Wed, 25 Jan 2017 19:13:21 GMT
ENV REDMINE_VERSION=3.3.2
# Wed, 25 Jan 2017 19:13:21 GMT
ENV REDMINE_DOWNLOAD_MD5=8e403981dc3a19a42ee978f055be62ca
# Wed, 25 Jan 2017 19:13:25 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Wed, 25 Jan 2017 19:15:29 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Wed, 25 Jan 2017 19:15:30 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 25 Jan 2017 19:15:30 GMT
COPY file:5efb6ca648b54af01740423ca0fdde905eae0ce732d8f2683c79dcf93e0e86c5 in / 
# Wed, 25 Jan 2017 19:15:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 25 Jan 2017 19:15:31 GMT
EXPOSE 3000/tcp
# Wed, 25 Jan 2017 19:15:31 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Wed, 25 Jan 2017 19:15:32 GMT
ENV PASSENGER_VERSION=5.1.2
# Wed, 25 Jan 2017 19:15:44 GMT
RUN buildDeps=' 		make 	' 	&& set -x 	&& apt-get update && apt-get install -y --no-install-recommends $buildDeps && rm -rf /var/lib/apt/lists/* 	&& gem install passenger --version "$PASSENGER_VERSION" 	&& apt-get purge -y --auto-remove $buildDeps
# Wed, 08 Feb 2017 21:47:16 GMT
RUN set -x 	&& passenger-config install-agent 	&& passenger-config download-nginx-engine
# Wed, 08 Feb 2017 21:47:16 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:5040bd2983909aa8896b9932438c3f1479d25ae837a5f6220242a264d0221f2d`  
		Last Modified: Mon, 16 Jan 2017 20:43:26 GMT  
		Size: 51.4 MB (51361210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596ec0bfbfe79e6bf8ba516cc80f14487c52f661c1c8f1dfdef2535f165beb56`  
		Last Modified: Wed, 18 Jan 2017 07:25:44 GMT  
		Size: 10.0 MB (9994242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330c0f0b9895c0a3df4249a9e2fe344e00dc43a4d9aac66506818ee0a8408043`  
		Last Modified: Wed, 18 Jan 2017 07:25:33 GMT  
		Size: 204.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759aaf3bf184b4692bcec722e430b1de0efcc5ebde1900ed83ef473c51d13d25`  
		Last Modified: Wed, 25 Jan 2017 18:33:14 GMT  
		Size: 33.3 MB (33326682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d391bd471e9bc64130a292130fcc4209eda0d1104ace90657ee4a56936cce2`  
		Last Modified: Wed, 25 Jan 2017 18:33:04 GMT  
		Size: 631.7 KB (631727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d548a23aa17d0f8419147686fdfa8b4f1637c6d592d2e13747c673f78a94b3c`  
		Last Modified: Wed, 25 Jan 2017 18:33:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548bf7ed54c4db146a49c6c74fd814210ff67320823ebf8dd5a5bae27bb62bb0`  
		Last Modified: Wed, 25 Jan 2017 19:16:08 GMT  
		Size: 2.0 KB (2043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42efbdc1be57cd208a79d1d7e3d07d83ecb18ae788b4f4b2ef0d6e4fdc86e4c0`  
		Last Modified: Wed, 25 Jan 2017 19:16:11 GMT  
		Size: 13.9 MB (13863641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c31ff7009497607f6e6e568d32553e37836e372cde3c5e53014f911ad6d69e`  
		Last Modified: Wed, 25 Jan 2017 19:16:06 GMT  
		Size: 807.9 KB (807934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdc0aa7eb6c6b4772890ecd81a8544f69d86e7aecf56b6be1c25088e4a4208e`  
		Last Modified: Wed, 25 Jan 2017 19:16:05 GMT  
		Size: 7.1 KB (7122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2bb7220f9b536cc758b25d7b5a65d33622e72ea714030de7cfcdb4e5ab9ae3`  
		Last Modified: Wed, 25 Jan 2017 19:16:22 GMT  
		Size: 58.2 MB (58213014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bd5e9fe51eb83c0111790e7dda6c778aa07e6d7699168b08dbc2c50680d231`  
		Last Modified: Wed, 25 Jan 2017 19:16:03 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc502bf8c5ab1e8a7c2277b45dff3cb372c79eea75c1ee27de940d8c0ad49159`  
		Last Modified: Wed, 25 Jan 2017 19:19:04 GMT  
		Size: 2.4 MB (2376996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c88d95529382256ccc7d960f0581829e24584a7722aca63ee4cc10e38ab0f4f0`  
		Last Modified: Wed, 25 Jan 2017 19:19:16 GMT  
		Size: 75.8 MB (75788340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3560bd24100c45be977767a24def1c6c3d241299c530a8d890ca8002a10cd52b`  
		Last Modified: Wed, 25 Jan 2017 19:19:02 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a504b1ab29b87afe3b50301a15e91deac52d6d24518dc169f2e34684583c744`  
		Last Modified: Wed, 25 Jan 2017 19:20:27 GMT  
		Size: 15.5 MB (15505038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6710dbee80e095f670b73b200725457f1524b95ee61fe60882888433cb29cc43`  
		Last Modified: Wed, 08 Feb 2017 21:51:00 GMT  
		Size: 4.1 MB (4066210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:3.3-passenger`

```console
$ docker pull redmine@sha256:959f658676033254221d5db8fd4970fc7037eeec4b87a1c4266f71db94d8f685
```

-	Platforms:
	-	linux; amd64

### `redmine:3.3-passenger` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.9 MB (265946222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64c6305b6d97f2bc923df2ef9e671a81602af45f07392a67ed3a466b8a9d16d0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Mon, 16 Jan 2017 20:35:09 GMT
ADD file:89ecb642d662ee7edbb868340551106d51336c7e589fdaca4111725ec64da957 in / 
# Mon, 16 Jan 2017 20:35:16 GMT
CMD ["/bin/bash"]
# Tue, 17 Jan 2017 20:12:19 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Jan 2017 20:12:20 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 17 Jan 2017 20:17:55 GMT
ENV RUBY_MAJOR=2.2
# Tue, 17 Jan 2017 20:17:55 GMT
ENV RUBY_VERSION=2.2.6
# Tue, 17 Jan 2017 20:17:55 GMT
ENV RUBY_DOWNLOAD_SHA256=9414ecc0d09cf71c9a24e8dc82fcc87919ac7359fb08db2791d6c32bfd157339
# Wed, 25 Jan 2017 18:08:18 GMT
ENV RUBYGEMS_VERSION=2.6.10
# Wed, 25 Jan 2017 18:10:49 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& ./configure --disable-install-doc --enable-shared 	&& make -j"$(nproc)" 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION"
# Wed, 25 Jan 2017 18:10:49 GMT
ENV BUNDLER_VERSION=1.14.3
# Wed, 25 Jan 2017 18:10:50 GMT
RUN gem install bundler --version "$BUNDLER_VERSION"
# Wed, 25 Jan 2017 18:10:51 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 25 Jan 2017 18:10:51 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 25 Jan 2017 18:10:51 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Jan 2017 18:10:52 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Wed, 25 Jan 2017 18:10:52 GMT
CMD ["irb"]
# Wed, 25 Jan 2017 19:07:25 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Wed, 25 Jan 2017 19:07:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2017 19:07:34 GMT
ENV GOSU_VERSION=1.7
# Wed, 25 Jan 2017 19:07:39 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Wed, 25 Jan 2017 19:07:39 GMT
ENV TINI_VERSION=v0.9.0
# Wed, 25 Jan 2017 19:07:42 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Wed, 25 Jan 2017 19:08:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2017 19:08:14 GMT
ENV RAILS_ENV=production
# Wed, 25 Jan 2017 19:08:14 GMT
WORKDIR /usr/src/redmine
# Wed, 25 Jan 2017 19:13:21 GMT
ENV REDMINE_VERSION=3.3.2
# Wed, 25 Jan 2017 19:13:21 GMT
ENV REDMINE_DOWNLOAD_MD5=8e403981dc3a19a42ee978f055be62ca
# Wed, 25 Jan 2017 19:13:25 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Wed, 25 Jan 2017 19:15:29 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Wed, 25 Jan 2017 19:15:30 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 25 Jan 2017 19:15:30 GMT
COPY file:5efb6ca648b54af01740423ca0fdde905eae0ce732d8f2683c79dcf93e0e86c5 in / 
# Wed, 25 Jan 2017 19:15:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 25 Jan 2017 19:15:31 GMT
EXPOSE 3000/tcp
# Wed, 25 Jan 2017 19:15:31 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Wed, 25 Jan 2017 19:15:32 GMT
ENV PASSENGER_VERSION=5.1.2
# Wed, 25 Jan 2017 19:15:44 GMT
RUN buildDeps=' 		make 	' 	&& set -x 	&& apt-get update && apt-get install -y --no-install-recommends $buildDeps && rm -rf /var/lib/apt/lists/* 	&& gem install passenger --version "$PASSENGER_VERSION" 	&& apt-get purge -y --auto-remove $buildDeps
# Wed, 08 Feb 2017 21:47:16 GMT
RUN set -x 	&& passenger-config install-agent 	&& passenger-config download-nginx-engine
# Wed, 08 Feb 2017 21:47:16 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:5040bd2983909aa8896b9932438c3f1479d25ae837a5f6220242a264d0221f2d`  
		Last Modified: Mon, 16 Jan 2017 20:43:26 GMT  
		Size: 51.4 MB (51361210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596ec0bfbfe79e6bf8ba516cc80f14487c52f661c1c8f1dfdef2535f165beb56`  
		Last Modified: Wed, 18 Jan 2017 07:25:44 GMT  
		Size: 10.0 MB (9994242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330c0f0b9895c0a3df4249a9e2fe344e00dc43a4d9aac66506818ee0a8408043`  
		Last Modified: Wed, 18 Jan 2017 07:25:33 GMT  
		Size: 204.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759aaf3bf184b4692bcec722e430b1de0efcc5ebde1900ed83ef473c51d13d25`  
		Last Modified: Wed, 25 Jan 2017 18:33:14 GMT  
		Size: 33.3 MB (33326682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d391bd471e9bc64130a292130fcc4209eda0d1104ace90657ee4a56936cce2`  
		Last Modified: Wed, 25 Jan 2017 18:33:04 GMT  
		Size: 631.7 KB (631727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d548a23aa17d0f8419147686fdfa8b4f1637c6d592d2e13747c673f78a94b3c`  
		Last Modified: Wed, 25 Jan 2017 18:33:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548bf7ed54c4db146a49c6c74fd814210ff67320823ebf8dd5a5bae27bb62bb0`  
		Last Modified: Wed, 25 Jan 2017 19:16:08 GMT  
		Size: 2.0 KB (2043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42efbdc1be57cd208a79d1d7e3d07d83ecb18ae788b4f4b2ef0d6e4fdc86e4c0`  
		Last Modified: Wed, 25 Jan 2017 19:16:11 GMT  
		Size: 13.9 MB (13863641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c31ff7009497607f6e6e568d32553e37836e372cde3c5e53014f911ad6d69e`  
		Last Modified: Wed, 25 Jan 2017 19:16:06 GMT  
		Size: 807.9 KB (807934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdc0aa7eb6c6b4772890ecd81a8544f69d86e7aecf56b6be1c25088e4a4208e`  
		Last Modified: Wed, 25 Jan 2017 19:16:05 GMT  
		Size: 7.1 KB (7122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2bb7220f9b536cc758b25d7b5a65d33622e72ea714030de7cfcdb4e5ab9ae3`  
		Last Modified: Wed, 25 Jan 2017 19:16:22 GMT  
		Size: 58.2 MB (58213014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bd5e9fe51eb83c0111790e7dda6c778aa07e6d7699168b08dbc2c50680d231`  
		Last Modified: Wed, 25 Jan 2017 19:16:03 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc502bf8c5ab1e8a7c2277b45dff3cb372c79eea75c1ee27de940d8c0ad49159`  
		Last Modified: Wed, 25 Jan 2017 19:19:04 GMT  
		Size: 2.4 MB (2376996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c88d95529382256ccc7d960f0581829e24584a7722aca63ee4cc10e38ab0f4f0`  
		Last Modified: Wed, 25 Jan 2017 19:19:16 GMT  
		Size: 75.8 MB (75788340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3560bd24100c45be977767a24def1c6c3d241299c530a8d890ca8002a10cd52b`  
		Last Modified: Wed, 25 Jan 2017 19:19:02 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a504b1ab29b87afe3b50301a15e91deac52d6d24518dc169f2e34684583c744`  
		Last Modified: Wed, 25 Jan 2017 19:20:27 GMT  
		Size: 15.5 MB (15505038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6710dbee80e095f670b73b200725457f1524b95ee61fe60882888433cb29cc43`  
		Last Modified: Wed, 08 Feb 2017 21:51:00 GMT  
		Size: 4.1 MB (4066210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:3-passenger`

```console
$ docker pull redmine@sha256:959f658676033254221d5db8fd4970fc7037eeec4b87a1c4266f71db94d8f685
```

-	Platforms:
	-	linux; amd64

### `redmine:3-passenger` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.9 MB (265946222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64c6305b6d97f2bc923df2ef9e671a81602af45f07392a67ed3a466b8a9d16d0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Mon, 16 Jan 2017 20:35:09 GMT
ADD file:89ecb642d662ee7edbb868340551106d51336c7e589fdaca4111725ec64da957 in / 
# Mon, 16 Jan 2017 20:35:16 GMT
CMD ["/bin/bash"]
# Tue, 17 Jan 2017 20:12:19 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Jan 2017 20:12:20 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 17 Jan 2017 20:17:55 GMT
ENV RUBY_MAJOR=2.2
# Tue, 17 Jan 2017 20:17:55 GMT
ENV RUBY_VERSION=2.2.6
# Tue, 17 Jan 2017 20:17:55 GMT
ENV RUBY_DOWNLOAD_SHA256=9414ecc0d09cf71c9a24e8dc82fcc87919ac7359fb08db2791d6c32bfd157339
# Wed, 25 Jan 2017 18:08:18 GMT
ENV RUBYGEMS_VERSION=2.6.10
# Wed, 25 Jan 2017 18:10:49 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& ./configure --disable-install-doc --enable-shared 	&& make -j"$(nproc)" 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION"
# Wed, 25 Jan 2017 18:10:49 GMT
ENV BUNDLER_VERSION=1.14.3
# Wed, 25 Jan 2017 18:10:50 GMT
RUN gem install bundler --version "$BUNDLER_VERSION"
# Wed, 25 Jan 2017 18:10:51 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 25 Jan 2017 18:10:51 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 25 Jan 2017 18:10:51 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Jan 2017 18:10:52 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Wed, 25 Jan 2017 18:10:52 GMT
CMD ["irb"]
# Wed, 25 Jan 2017 19:07:25 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Wed, 25 Jan 2017 19:07:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2017 19:07:34 GMT
ENV GOSU_VERSION=1.7
# Wed, 25 Jan 2017 19:07:39 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Wed, 25 Jan 2017 19:07:39 GMT
ENV TINI_VERSION=v0.9.0
# Wed, 25 Jan 2017 19:07:42 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Wed, 25 Jan 2017 19:08:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2017 19:08:14 GMT
ENV RAILS_ENV=production
# Wed, 25 Jan 2017 19:08:14 GMT
WORKDIR /usr/src/redmine
# Wed, 25 Jan 2017 19:13:21 GMT
ENV REDMINE_VERSION=3.3.2
# Wed, 25 Jan 2017 19:13:21 GMT
ENV REDMINE_DOWNLOAD_MD5=8e403981dc3a19a42ee978f055be62ca
# Wed, 25 Jan 2017 19:13:25 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Wed, 25 Jan 2017 19:15:29 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Wed, 25 Jan 2017 19:15:30 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 25 Jan 2017 19:15:30 GMT
COPY file:5efb6ca648b54af01740423ca0fdde905eae0ce732d8f2683c79dcf93e0e86c5 in / 
# Wed, 25 Jan 2017 19:15:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 25 Jan 2017 19:15:31 GMT
EXPOSE 3000/tcp
# Wed, 25 Jan 2017 19:15:31 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Wed, 25 Jan 2017 19:15:32 GMT
ENV PASSENGER_VERSION=5.1.2
# Wed, 25 Jan 2017 19:15:44 GMT
RUN buildDeps=' 		make 	' 	&& set -x 	&& apt-get update && apt-get install -y --no-install-recommends $buildDeps && rm -rf /var/lib/apt/lists/* 	&& gem install passenger --version "$PASSENGER_VERSION" 	&& apt-get purge -y --auto-remove $buildDeps
# Wed, 08 Feb 2017 21:47:16 GMT
RUN set -x 	&& passenger-config install-agent 	&& passenger-config download-nginx-engine
# Wed, 08 Feb 2017 21:47:16 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:5040bd2983909aa8896b9932438c3f1479d25ae837a5f6220242a264d0221f2d`  
		Last Modified: Mon, 16 Jan 2017 20:43:26 GMT  
		Size: 51.4 MB (51361210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596ec0bfbfe79e6bf8ba516cc80f14487c52f661c1c8f1dfdef2535f165beb56`  
		Last Modified: Wed, 18 Jan 2017 07:25:44 GMT  
		Size: 10.0 MB (9994242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330c0f0b9895c0a3df4249a9e2fe344e00dc43a4d9aac66506818ee0a8408043`  
		Last Modified: Wed, 18 Jan 2017 07:25:33 GMT  
		Size: 204.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759aaf3bf184b4692bcec722e430b1de0efcc5ebde1900ed83ef473c51d13d25`  
		Last Modified: Wed, 25 Jan 2017 18:33:14 GMT  
		Size: 33.3 MB (33326682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d391bd471e9bc64130a292130fcc4209eda0d1104ace90657ee4a56936cce2`  
		Last Modified: Wed, 25 Jan 2017 18:33:04 GMT  
		Size: 631.7 KB (631727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d548a23aa17d0f8419147686fdfa8b4f1637c6d592d2e13747c673f78a94b3c`  
		Last Modified: Wed, 25 Jan 2017 18:33:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548bf7ed54c4db146a49c6c74fd814210ff67320823ebf8dd5a5bae27bb62bb0`  
		Last Modified: Wed, 25 Jan 2017 19:16:08 GMT  
		Size: 2.0 KB (2043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42efbdc1be57cd208a79d1d7e3d07d83ecb18ae788b4f4b2ef0d6e4fdc86e4c0`  
		Last Modified: Wed, 25 Jan 2017 19:16:11 GMT  
		Size: 13.9 MB (13863641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c31ff7009497607f6e6e568d32553e37836e372cde3c5e53014f911ad6d69e`  
		Last Modified: Wed, 25 Jan 2017 19:16:06 GMT  
		Size: 807.9 KB (807934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdc0aa7eb6c6b4772890ecd81a8544f69d86e7aecf56b6be1c25088e4a4208e`  
		Last Modified: Wed, 25 Jan 2017 19:16:05 GMT  
		Size: 7.1 KB (7122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2bb7220f9b536cc758b25d7b5a65d33622e72ea714030de7cfcdb4e5ab9ae3`  
		Last Modified: Wed, 25 Jan 2017 19:16:22 GMT  
		Size: 58.2 MB (58213014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bd5e9fe51eb83c0111790e7dda6c778aa07e6d7699168b08dbc2c50680d231`  
		Last Modified: Wed, 25 Jan 2017 19:16:03 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc502bf8c5ab1e8a7c2277b45dff3cb372c79eea75c1ee27de940d8c0ad49159`  
		Last Modified: Wed, 25 Jan 2017 19:19:04 GMT  
		Size: 2.4 MB (2376996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c88d95529382256ccc7d960f0581829e24584a7722aca63ee4cc10e38ab0f4f0`  
		Last Modified: Wed, 25 Jan 2017 19:19:16 GMT  
		Size: 75.8 MB (75788340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3560bd24100c45be977767a24def1c6c3d241299c530a8d890ca8002a10cd52b`  
		Last Modified: Wed, 25 Jan 2017 19:19:02 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a504b1ab29b87afe3b50301a15e91deac52d6d24518dc169f2e34684583c744`  
		Last Modified: Wed, 25 Jan 2017 19:20:27 GMT  
		Size: 15.5 MB (15505038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6710dbee80e095f670b73b200725457f1524b95ee61fe60882888433cb29cc43`  
		Last Modified: Wed, 08 Feb 2017 21:51:00 GMT  
		Size: 4.1 MB (4066210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:passenger`

```console
$ docker pull redmine@sha256:959f658676033254221d5db8fd4970fc7037eeec4b87a1c4266f71db94d8f685
```

-	Platforms:
	-	linux; amd64

### `redmine:passenger` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.9 MB (265946222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64c6305b6d97f2bc923df2ef9e671a81602af45f07392a67ed3a466b8a9d16d0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Mon, 16 Jan 2017 20:35:09 GMT
ADD file:89ecb642d662ee7edbb868340551106d51336c7e589fdaca4111725ec64da957 in / 
# Mon, 16 Jan 2017 20:35:16 GMT
CMD ["/bin/bash"]
# Tue, 17 Jan 2017 20:12:19 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Jan 2017 20:12:20 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 17 Jan 2017 20:17:55 GMT
ENV RUBY_MAJOR=2.2
# Tue, 17 Jan 2017 20:17:55 GMT
ENV RUBY_VERSION=2.2.6
# Tue, 17 Jan 2017 20:17:55 GMT
ENV RUBY_DOWNLOAD_SHA256=9414ecc0d09cf71c9a24e8dc82fcc87919ac7359fb08db2791d6c32bfd157339
# Wed, 25 Jan 2017 18:08:18 GMT
ENV RUBYGEMS_VERSION=2.6.10
# Wed, 25 Jan 2017 18:10:49 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& ./configure --disable-install-doc --enable-shared 	&& make -j"$(nproc)" 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION"
# Wed, 25 Jan 2017 18:10:49 GMT
ENV BUNDLER_VERSION=1.14.3
# Wed, 25 Jan 2017 18:10:50 GMT
RUN gem install bundler --version "$BUNDLER_VERSION"
# Wed, 25 Jan 2017 18:10:51 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 25 Jan 2017 18:10:51 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 25 Jan 2017 18:10:51 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Jan 2017 18:10:52 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Wed, 25 Jan 2017 18:10:52 GMT
CMD ["irb"]
# Wed, 25 Jan 2017 19:07:25 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Wed, 25 Jan 2017 19:07:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2017 19:07:34 GMT
ENV GOSU_VERSION=1.7
# Wed, 25 Jan 2017 19:07:39 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Wed, 25 Jan 2017 19:07:39 GMT
ENV TINI_VERSION=v0.9.0
# Wed, 25 Jan 2017 19:07:42 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Wed, 25 Jan 2017 19:08:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2017 19:08:14 GMT
ENV RAILS_ENV=production
# Wed, 25 Jan 2017 19:08:14 GMT
WORKDIR /usr/src/redmine
# Wed, 25 Jan 2017 19:13:21 GMT
ENV REDMINE_VERSION=3.3.2
# Wed, 25 Jan 2017 19:13:21 GMT
ENV REDMINE_DOWNLOAD_MD5=8e403981dc3a19a42ee978f055be62ca
# Wed, 25 Jan 2017 19:13:25 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Wed, 25 Jan 2017 19:15:29 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Wed, 25 Jan 2017 19:15:30 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 25 Jan 2017 19:15:30 GMT
COPY file:5efb6ca648b54af01740423ca0fdde905eae0ce732d8f2683c79dcf93e0e86c5 in / 
# Wed, 25 Jan 2017 19:15:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 25 Jan 2017 19:15:31 GMT
EXPOSE 3000/tcp
# Wed, 25 Jan 2017 19:15:31 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Wed, 25 Jan 2017 19:15:32 GMT
ENV PASSENGER_VERSION=5.1.2
# Wed, 25 Jan 2017 19:15:44 GMT
RUN buildDeps=' 		make 	' 	&& set -x 	&& apt-get update && apt-get install -y --no-install-recommends $buildDeps && rm -rf /var/lib/apt/lists/* 	&& gem install passenger --version "$PASSENGER_VERSION" 	&& apt-get purge -y --auto-remove $buildDeps
# Wed, 08 Feb 2017 21:47:16 GMT
RUN set -x 	&& passenger-config install-agent 	&& passenger-config download-nginx-engine
# Wed, 08 Feb 2017 21:47:16 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:5040bd2983909aa8896b9932438c3f1479d25ae837a5f6220242a264d0221f2d`  
		Last Modified: Mon, 16 Jan 2017 20:43:26 GMT  
		Size: 51.4 MB (51361210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596ec0bfbfe79e6bf8ba516cc80f14487c52f661c1c8f1dfdef2535f165beb56`  
		Last Modified: Wed, 18 Jan 2017 07:25:44 GMT  
		Size: 10.0 MB (9994242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330c0f0b9895c0a3df4249a9e2fe344e00dc43a4d9aac66506818ee0a8408043`  
		Last Modified: Wed, 18 Jan 2017 07:25:33 GMT  
		Size: 204.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759aaf3bf184b4692bcec722e430b1de0efcc5ebde1900ed83ef473c51d13d25`  
		Last Modified: Wed, 25 Jan 2017 18:33:14 GMT  
		Size: 33.3 MB (33326682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d391bd471e9bc64130a292130fcc4209eda0d1104ace90657ee4a56936cce2`  
		Last Modified: Wed, 25 Jan 2017 18:33:04 GMT  
		Size: 631.7 KB (631727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d548a23aa17d0f8419147686fdfa8b4f1637c6d592d2e13747c673f78a94b3c`  
		Last Modified: Wed, 25 Jan 2017 18:33:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548bf7ed54c4db146a49c6c74fd814210ff67320823ebf8dd5a5bae27bb62bb0`  
		Last Modified: Wed, 25 Jan 2017 19:16:08 GMT  
		Size: 2.0 KB (2043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42efbdc1be57cd208a79d1d7e3d07d83ecb18ae788b4f4b2ef0d6e4fdc86e4c0`  
		Last Modified: Wed, 25 Jan 2017 19:16:11 GMT  
		Size: 13.9 MB (13863641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c31ff7009497607f6e6e568d32553e37836e372cde3c5e53014f911ad6d69e`  
		Last Modified: Wed, 25 Jan 2017 19:16:06 GMT  
		Size: 807.9 KB (807934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdc0aa7eb6c6b4772890ecd81a8544f69d86e7aecf56b6be1c25088e4a4208e`  
		Last Modified: Wed, 25 Jan 2017 19:16:05 GMT  
		Size: 7.1 KB (7122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2bb7220f9b536cc758b25d7b5a65d33622e72ea714030de7cfcdb4e5ab9ae3`  
		Last Modified: Wed, 25 Jan 2017 19:16:22 GMT  
		Size: 58.2 MB (58213014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bd5e9fe51eb83c0111790e7dda6c778aa07e6d7699168b08dbc2c50680d231`  
		Last Modified: Wed, 25 Jan 2017 19:16:03 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc502bf8c5ab1e8a7c2277b45dff3cb372c79eea75c1ee27de940d8c0ad49159`  
		Last Modified: Wed, 25 Jan 2017 19:19:04 GMT  
		Size: 2.4 MB (2376996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c88d95529382256ccc7d960f0581829e24584a7722aca63ee4cc10e38ab0f4f0`  
		Last Modified: Wed, 25 Jan 2017 19:19:16 GMT  
		Size: 75.8 MB (75788340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3560bd24100c45be977767a24def1c6c3d241299c530a8d890ca8002a10cd52b`  
		Last Modified: Wed, 25 Jan 2017 19:19:02 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a504b1ab29b87afe3b50301a15e91deac52d6d24518dc169f2e34684583c744`  
		Last Modified: Wed, 25 Jan 2017 19:20:27 GMT  
		Size: 15.5 MB (15505038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6710dbee80e095f670b73b200725457f1524b95ee61fe60882888433cb29cc43`  
		Last Modified: Wed, 08 Feb 2017 21:51:00 GMT  
		Size: 4.1 MB (4066210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
