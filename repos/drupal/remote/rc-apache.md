## `drupal:rc-apache`

```console
$ docker pull drupal@sha256:19bc4dd9d80c0bb326d3dc810afa46cf134ccdc472f6d4375e6e7ccfee0ce135
```

-	Platforms:
	-	linux; amd64

### `drupal:rc-apache` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.4 MB (179379025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d71c5bf92ed15de4c528d596ef883e9a3bb7caba255a08739daf8788eead8a02`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 16 Jan 2017 20:35:09 GMT
ADD file:89ecb642d662ee7edbb868340551106d51336c7e589fdaca4111725ec64da957 in / 
# Mon, 16 Jan 2017 20:35:16 GMT
CMD ["/bin/bash"]
# Tue, 17 Jan 2017 18:54:13 GMT
ENV PHPIZE_DEPS=autoconf 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 17 Jan 2017 18:54:39 GMT
RUN apt-get update && apt-get install -y 		$PHPIZE_DEPS 		ca-certificates 		curl 		libedit2 		libsqlite3-0 		libxml2 		xz-utils 	--no-install-recommends && rm -r /var/lib/apt/lists/*
# Tue, 17 Jan 2017 18:54:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 17 Jan 2017 18:54:40 GMT
RUN mkdir -p $PHP_INI_DIR/conf.d
# Tue, 17 Jan 2017 18:58:08 GMT
RUN apt-get update && apt-get install -y apache2-bin apache2.2-common --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 17 Jan 2017 18:58:08 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 17 Jan 2017 18:58:08 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 17 Jan 2017 18:58:09 GMT
RUN set -ex 		&& sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS" 		&& . "$APACHE_ENVVARS" 	&& for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		/var/www/html 	; do 		rm -rvf "$dir" 		&& mkdir -p "$dir" 		&& chown -R "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 	done
# Tue, 17 Jan 2017 18:58:10 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 17 Jan 2017 18:58:11 GMT
RUN set -ex 	&& . "$APACHE_ENVVARS" 	&& ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log" 	&& ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log" 	&& ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"
# Tue, 17 Jan 2017 18:58:12 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 17 Jan 2017 18:58:12 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Tue, 17 Jan 2017 18:58:13 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2
# Tue, 17 Jan 2017 18:58:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Tue, 17 Jan 2017 18:58:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Tue, 17 Jan 2017 18:58:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Tue, 24 Jan 2017 18:31:37 GMT
ENV GPG_KEYS=A917B1ECDA84AEC2B568FED6F50ABC807BD5DCD0 528995BFEDFBA7191D46839EF9BA0ADA31CBD89E
# Tue, 24 Jan 2017 18:31:37 GMT
ENV PHP_VERSION=7.1.1
# Tue, 24 Jan 2017 18:31:38 GMT
ENV PHP_URL=https://secure.php.net/get/php-7.1.1.tar.xz/from/this/mirror PHP_ASC_URL=https://secure.php.net/get/php-7.1.1.tar.xz.asc/from/this/mirror
# Tue, 24 Jan 2017 18:31:38 GMT
ENV PHP_SHA256=b3565b0c1441064eba204821608df1ec7367abff881286898d900c2c2a5ffe70 PHP_MD5=65eef256f6e7104a05361939f5e23ada
# Tue, 24 Jan 2017 18:31:47 GMT
RUN set -xe; 		fetchDeps=' 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		wget -O php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		wget -O php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		rm -r "$GNUPGHOME"; 	fi; 		apt-get purge -y --auto-remove $fetchDeps
# Tue, 24 Jan 2017 18:31:48 GMT
COPY file:207c686e3fed4f71f8a7b245d8dcae9c9048d276a326d82b553c12a90af0c0ca in /usr/local/bin/ 
# Tue, 24 Jan 2017 18:34:09 GMT
RUN set -xe 	&& buildDeps=" 		$PHP_EXTRA_BUILD_DEPS 		libcurl4-openssl-dev 		libedit-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 	" 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	&& docker-php-source extract 	&& cd /usr/src/php 	&& ./configure 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--disable-cgi 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$PHP_EXTRA_CONFIGURE_ARGS 	&& make -j "$(nproc)" 	&& make install 	&& { find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; } 	&& make clean 	&& docker-php-source delete 		&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $buildDeps
# Tue, 24 Jan 2017 18:34:10 GMT
COPY multi:2b7e23dbf0e975ef1ec1f186511e2789ab94e8c8734ca9fa8419c893f7357d6c in /usr/local/bin/ 
# Tue, 24 Jan 2017 18:34:10 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 27 Jan 2017 23:15:10 GMT
COPY file:24613ecbb1ce6a09f683b0753da9c26a1af07547326e8a02f6eec80ad6f2774a in /usr/local/bin/ 
# Fri, 27 Jan 2017 23:15:11 GMT
WORKDIR /var/www/html
# Fri, 27 Jan 2017 23:15:11 GMT
EXPOSE 80/tcp
# Fri, 27 Jan 2017 23:15:12 GMT
CMD ["apache2-foreground"]
# Tue, 07 Feb 2017 19:45:17 GMT
RUN a2enmod rewrite
# Tue, 07 Feb 2017 19:46:48 GMT
RUN apt-get update && apt-get install -y libpng12-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr 	&& docker-php-ext-install gd mbstring opcache pdo pdo_mysql pdo_pgsql zip
# Tue, 07 Feb 2017 19:46:49 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 		echo 'opcache.enable_cli=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 07 Feb 2017 19:46:49 GMT
WORKDIR /var/www/html
# Tue, 07 Feb 2017 19:46:49 GMT
ENV DRUPAL_VERSION=8.3.0-alpha1
# Tue, 07 Feb 2017 19:46:50 GMT
ENV DRUPAL_MD5=601f931d5a3281214917e3eabfd86408
# Tue, 07 Feb 2017 19:46:56 GMT
RUN curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz 	&& echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f drupal.tar.gz 	&& rm drupal.tar.gz 	&& chown -R www-data:www-data sites modules themes
```

-	Layers:
	-	`sha256:5040bd2983909aa8896b9932438c3f1479d25ae837a5f6220242a264d0221f2d`  
		Last Modified: Mon, 16 Jan 2017 20:43:26 GMT  
		Size: 51.4 MB (51361210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:568dce68541a55fd0fb33021383e3921145275a1f87d925f37f1246b682baf0b`  
		Last Modified: Wed, 18 Jan 2017 03:05:48 GMT  
		Size: 77.6 MB (77606810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a832068e64c0a907e1585adac98802eb69cf9fc878ba00941d59e7be57c4b93`  
		Last Modified: Wed, 18 Jan 2017 03:05:21 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0f3d176a5bf080e41340e04575cdeece539b71cd0405812474a03151cdf73f`  
		Last Modified: Wed, 18 Jan 2017 03:05:22 GMT  
		Size: 2.8 MB (2849173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20cc248a5690169dac19b598857e4ecd4a6421a5c21eb699066d5006cf27834b`  
		Last Modified: Wed, 18 Jan 2017 03:05:20 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff565538ee684ae5f9d8e1c0c152bfabefa1f94202054df27edc82410555c74`  
		Last Modified: Wed, 18 Jan 2017 03:05:19 GMT  
		Size: 431.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1077228581cd19b5dc570b5831269295dd388feba6e783bd93396b0a825caa`  
		Last Modified: Wed, 18 Jan 2017 03:05:18 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57359f144a1928936e5079e40f75cf1e00f8eb81b3bf2045fbdbc02e9f1b78e5`  
		Last Modified: Wed, 18 Jan 2017 03:05:17 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02192cdb2b85b8e791facf01c6d856479e4f17deed3f1496b26f5ad80ab9b254`  
		Last Modified: Tue, 24 Jan 2017 19:45:54 GMT  
		Size: 12.9 MB (12896249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438a4f02ffc78eb4a0841f27eb20b201db9d775e2e5f87d9892ea822534246d7`  
		Last Modified: Tue, 24 Jan 2017 19:45:52 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf3c50aa40727b1bf4c8645dd6976963e6f3a0cd4870695613574604a1f5c17`  
		Last Modified: Tue, 24 Jan 2017 19:45:57 GMT  
		Size: 13.6 MB (13601582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7291edaaf617548d594d8855e35a9fb3c657f79ebe997aa34b2879c87502bdf4`  
		Last Modified: Tue, 24 Jan 2017 19:45:52 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ac60b9af575c65836748f9ed03ccb909db120bb9b848ff3bbf217eb6151c817`  
		Last Modified: Fri, 27 Jan 2017 23:18:38 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8858fea14c13f607642773618ce4dd91194b2fd027784d7bc1a0c6fe657db90`  
		Last Modified: Tue, 07 Feb 2017 19:48:53 GMT  
		Size: 295.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1055670e79cffaaef4e2b2ad993904074265fd4bb2be51036cd035d6374ed61d`  
		Last Modified: Tue, 07 Feb 2017 19:48:55 GMT  
		Size: 8.7 MB (8744236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08f6aece3020993b0ccbf54b11a3a6e1423471be1534ca1f19d983f475856424`  
		Last Modified: Tue, 07 Feb 2017 19:48:53 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07cc9d347ba07bcfcee4a6fc31773ebc29001a55f16b690760b012c75844566a`  
		Last Modified: Tue, 07 Feb 2017 19:48:57 GMT  
		Size: 12.3 MB (12313190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
