## `tomcat:7-jre7`

```console
$ docker pull tomcat@sha256:e137a79f86f9f3c79c868213b58867aaae27d385a1b5014dc5b5861cd5d170a0
```

-	Platforms:
	-	linux; amd64

### `tomcat:7-jre7` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.1 MB (161058166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28f88d683c4c13d218fb9d351df0d1945c322fe8ab8e975b3fd532854fa5887e`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 16 Jan 2017 20:35:09 GMT
ADD file:89ecb642d662ee7edbb868340551106d51336c7e589fdaca4111725ec64da957 in / 
# Mon, 16 Jan 2017 20:35:16 GMT
CMD ["/bin/bash"]
# Tue, 17 Jan 2017 00:00:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Jan 2017 00:51:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Jan 2017 00:51:05 GMT
ENV LANG=C.UTF-8
# Tue, 17 Jan 2017 00:51:06 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 17 Jan 2017 00:51:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-7-openjdk-amd64/jre
# Wed, 08 Feb 2017 22:16:54 GMT
ENV JAVA_VERSION=7u121
# Wed, 08 Feb 2017 22:16:55 GMT
ENV JAVA_DEBIAN_VERSION=7u121-2.6.8-2~deb8u1
# Wed, 08 Feb 2017 22:17:27 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		openjdk-7-jre-headless="$JAVA_DEBIAN_VERSION" 	&& rm -rf /var/lib/apt/lists/* 	&& [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 09 Feb 2017 00:02:55 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 09 Feb 2017 00:02:56 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Feb 2017 00:02:57 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 09 Feb 2017 00:02:57 GMT
WORKDIR /usr/local/tomcat
# Thu, 09 Feb 2017 00:02:58 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 09 Feb 2017 00:02:59 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 09 Feb 2017 00:02:59 GMT
ENV OPENSSL_VERSION=1.1.0c-2
# Thu, 09 Feb 2017 00:03:00 GMT
RUN { 		echo 'deb http://deb.debian.org/debian stretch main'; 	} > /etc/apt/sources.list.d/stretch.list 	&& { 		echo 'Package: *'; 		echo 'Pin: release n=stretch'; 		echo 'Pin-Priority: -10'; 		echo; 		echo 'Package: openssl libssl*'; 		echo "Pin: version $OPENSSL_VERSION"; 		echo 'Pin-Priority: 990'; 	} > /etc/apt/preferences.d/stretch-openssl
# Thu, 09 Feb 2017 00:03:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libapr1 		openssl="$OPENSSL_VERSION" 	&& rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2017 00:04:04 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 09 Feb 2017 00:04:09 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Thu, 09 Feb 2017 00:04:09 GMT
ENV TOMCAT_MAJOR=7
# Thu, 09 Feb 2017 00:04:10 GMT
ENV TOMCAT_VERSION=7.0.75
# Thu, 09 Feb 2017 00:04:11 GMT
ENV TOMCAT_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=tomcat/tomcat-7/v7.0.75/bin/apache-tomcat-7.0.75.tar.gz
# Thu, 09 Feb 2017 00:04:11 GMT
ENV TOMCAT_ASC_URL=https://www.apache.org/dist/tomcat/tomcat-7/v7.0.75/bin/apache-tomcat-7.0.75.tar.gz.asc
# Thu, 09 Feb 2017 00:04:45 GMT
RUN set -x 		&& wget -O tomcat.tar.gz "$TOMCAT_TGZ_URL" 	&& wget -O tomcat.tar.gz.asc "$TOMCAT_ASC_URL" 	&& gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz 	&& tar -xvf tomcat.tar.gz --strip-components=1 	&& rm bin/*.bat 	&& rm tomcat.tar.gz* 		&& nativeBuildDir="$(mktemp -d)" 	&& tar -xvf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1 	&& nativeBuildDeps=" 		gcc 		libapr1-dev 		libssl-dev 		make 		openjdk-${JAVA_VERSION%%[-~bu]*}-jdk=$JAVA_DEBIAN_VERSION 	" 	&& apt-get update && apt-get install -y --no-install-recommends $nativeBuildDeps && rm -rf /var/lib/apt/lists/* 	&& ( 		export CATALINA_HOME="$PWD" 		&& cd "$nativeBuildDir/native" 		&& ./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$(which apr-1-config)" 			--with-java-home="$(docker-java-home)" 			--with-ssl=yes 		&& make -j$(nproc) 		&& make install 	) 	&& apt-get purge -y --auto-remove $nativeBuildDeps 	&& rm -rf "$nativeBuildDir" 	&& rm bin/tomcat-native.tar.gz
# Thu, 09 Feb 2017 00:04:47 GMT
RUN set -e 	&& nativeLines="$(catalina.sh configtest 2>&1)" 	&& nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')" 	&& nativeLines="$(echo "$nativeLines" | sort -u)" 	&& if ! echo "$nativeLines" | grep 'INFO: Loaded APR based Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 09 Feb 2017 00:04:47 GMT
EXPOSE 8080/tcp
# Thu, 09 Feb 2017 00:04:48 GMT
CMD ["catalina.sh" "run"]
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
	-	`sha256:c42794440453cbec048425a8d20efae4d6f57b629bbbf4f1793131e91088eb46`  
		Last Modified: Tue, 17 Jan 2017 21:37:12 GMT  
		Size: 566.7 KB (566657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9789263043d1903b4bfb12d55378dce8182df44901ba747f53b662dfbddd0f10`  
		Last Modified: Wed, 18 Jan 2017 05:27:33 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c6ea13aad1573ad87eb6d2f38f7c42ea634532edc51d19039f4e57e82d3c549`  
		Last Modified: Wed, 08 Feb 2017 22:22:10 GMT  
		Size: 77.8 MB (77813197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55336e5423a8b81f4d87d0ed70472ac62e395804ce51e7bd80ccfda4d0eaf468`  
		Last Modified: Thu, 09 Feb 2017 00:06:02 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d8becd1725ee34e153af026043ff67e6e6b8919956aae9e7569b4d97cbfbe4`  
		Last Modified: Thu, 09 Feb 2017 00:06:02 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb7733eca8c6b18ee0a92466d7fbbad2066f24c69be767aaed166bb79dc72a4`  
		Last Modified: Thu, 09 Feb 2017 00:06:03 GMT  
		Size: 3.1 MB (3108484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52ab100cab32299ec69ff6928df6fe19c5d75b76474e1c821d1ccf304e2ea7e`  
		Last Modified: Thu, 09 Feb 2017 00:08:28 GMT  
		Size: 112.7 KB (112656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a041b1791a19f7a6dd6cd4989b37957054da36d66155d1a1453d3eeb6daf3a66`  
		Last Modified: Thu, 09 Feb 2017 00:08:29 GMT  
		Size: 9.6 MB (9559675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d6c900d71247d3c023ff888a3aa08b9fb72e3fa505c1f27019909d1a5078f3`  
		Last Modified: Thu, 09 Feb 2017 00:08:27 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
