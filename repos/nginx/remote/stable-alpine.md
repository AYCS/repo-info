## `nginx:stable-alpine`

```console
$ docker pull nginx@sha256:f5903273584555a30ebcfbe063ab7773b0b3667b6753df0d9680505cdfbaaa49
```

-	Platforms:
	-	linux; amd64

### `nginx:stable-alpine` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17953500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f481234b230c3edfda8b56993857daa5b37c0ba229b2090e496cbd0a888c8b0`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 27 Dec 2016 18:17:13 GMT
ADD file:eeed5f514a35d18fcd9cbfe6c40c582211020bffdd53e4799018d33826fe5067 in / 
# Tue, 27 Dec 2016 19:17:38 GMT
MAINTAINER NGINX Docker Maintainers "docker-maint@nginx.com"
# Tue, 31 Jan 2017 17:39:20 GMT
ENV NGINX_VERSION=1.10.3
# Tue, 31 Jan 2017 17:40:09 GMT
RUN GPG_KEYS=B0F4253373F8F6F510D42178520A9993A1C052F8 	&& CONFIG="		--prefix=/etc/nginx 		--sbin-path=/usr/sbin/nginx 		--modules-path=/usr/lib/nginx/modules 		--conf-path=/etc/nginx/nginx.conf 		--error-log-path=/var/log/nginx/error.log 		--http-log-path=/var/log/nginx/access.log 		--pid-path=/var/run/nginx.pid 		--lock-path=/var/run/nginx.lock 		--http-client-body-temp-path=/var/cache/nginx/client_temp 		--http-proxy-temp-path=/var/cache/nginx/proxy_temp 		--http-fastcgi-temp-path=/var/cache/nginx/fastcgi_temp 		--http-uwsgi-temp-path=/var/cache/nginx/uwsgi_temp 		--http-scgi-temp-path=/var/cache/nginx/scgi_temp 		--user=nginx 		--group=nginx 		--with-http_ssl_module 		--with-http_realip_module 		--with-http_addition_module 		--with-http_sub_module 		--with-http_dav_module 		--with-http_flv_module 		--with-http_mp4_module 		--with-http_gunzip_module 		--with-http_gzip_static_module 		--with-http_random_index_module 		--with-http_secure_link_module 		--with-http_stub_status_module 		--with-http_auth_request_module 		--with-http_xslt_module=dynamic 		--with-http_image_filter_module=dynamic 		--with-http_geoip_module=dynamic 		--with-http_perl_module=dynamic 		--with-threads 		--with-stream 		--with-stream_ssl_module 		--with-http_slice_module 		--with-mail 		--with-mail_ssl_module 		--with-file-aio 		--with-http_v2_module 		--with-ipv6 	" 	&& addgroup -S nginx 	&& adduser -D -S -h /var/cache/nginx -s /sbin/nologin -G nginx nginx 	&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		make 		openssl-dev 		pcre-dev 		zlib-dev 		linux-headers 		curl 		gnupg 		libxslt-dev 		gd-dev 		geoip-dev 		perl-dev 	&& curl -fSL http://nginx.org/download/nginx-$NGINX_VERSION.tar.gz -o nginx.tar.gz 	&& curl -fSL http://nginx.org/download/nginx-$NGINX_VERSION.tar.gz.asc  -o nginx.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEYS" 	&& gpg --batch --verify nginx.tar.gz.asc nginx.tar.gz 	&& rm -r "$GNUPGHOME" nginx.tar.gz.asc 	&& mkdir -p /usr/src 	&& tar -zxC /usr/src -f nginx.tar.gz 	&& rm nginx.tar.gz 	&& cd /usr/src/nginx-$NGINX_VERSION 	&& ./configure $CONFIG --with-debug 	&& make -j$(getconf _NPROCESSORS_ONLN) 	&& mv objs/nginx objs/nginx-debug 	&& mv objs/ngx_http_xslt_filter_module.so objs/ngx_http_xslt_filter_module-debug.so 	&& mv objs/ngx_http_image_filter_module.so objs/ngx_http_image_filter_module-debug.so 	&& mv objs/ngx_http_geoip_module.so objs/ngx_http_geoip_module-debug.so 	&& mv objs/ngx_http_perl_module.so objs/ngx_http_perl_module-debug.so 	&& ./configure $CONFIG 	&& make -j$(getconf _NPROCESSORS_ONLN) 	&& make install 	&& rm -rf /etc/nginx/html/ 	&& mkdir /etc/nginx/conf.d/ 	&& mkdir -p /usr/share/nginx/html/ 	&& install -m644 html/index.html /usr/share/nginx/html/ 	&& install -m644 html/50x.html /usr/share/nginx/html/ 	&& install -m755 objs/nginx-debug /usr/sbin/nginx-debug 	&& install -m755 objs/ngx_http_xslt_filter_module-debug.so /usr/lib/nginx/modules/ngx_http_xslt_filter_module-debug.so 	&& install -m755 objs/ngx_http_image_filter_module-debug.so /usr/lib/nginx/modules/ngx_http_image_filter_module-debug.so 	&& install -m755 objs/ngx_http_geoip_module-debug.so /usr/lib/nginx/modules/ngx_http_geoip_module-debug.so 	&& install -m755 objs/ngx_http_perl_module-debug.so /usr/lib/nginx/modules/ngx_http_perl_module-debug.so 	&& ln -s ../../usr/lib/nginx/modules /etc/nginx/modules 	&& strip /usr/sbin/nginx* 	&& strip /usr/lib/nginx/modules/*.so 	&& rm -rf /usr/src/nginx-$NGINX_VERSION 		&& apk add --no-cache --virtual .gettext gettext 	&& mv /usr/bin/envsubst /tmp/ 		&& runDeps="$( 		scanelf --needed --nobanner /usr/sbin/nginx /usr/lib/nginx/modules/*.so /tmp/envsubst 			| awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }' 			| sort -u 			| xargs -r apk info --installed 			| sort -u 	)" 	&& apk add --no-cache --virtual .nginx-rundeps $runDeps 	&& apk del .build-deps 	&& apk del .gettext 	&& mv /tmp/envsubst /usr/local/bin/ 		&& ln -sf /dev/stdout /var/log/nginx/access.log 	&& ln -sf /dev/stderr /var/log/nginx/error.log
# Tue, 31 Jan 2017 17:40:10 GMT
COPY file:af94db45bb7e4b8ff4e699f1ff6f41c348f9876073ad91d6e803070415f8d9ce in /etc/nginx/nginx.conf 
# Tue, 31 Jan 2017 17:40:10 GMT
COPY file:d15ceb73c6ea776c299822265ed38cd2fd8a78804f4f4889094d1dd1e292984b in /etc/nginx/conf.d/default.conf 
# Tue, 31 Jan 2017 17:40:11 GMT
EXPOSE 443/tcp 80/tcp
# Tue, 31 Jan 2017 17:40:11 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:b7f33cc0b48ea4fb2f0745def58c25483a5f6b7aed5b41ce8f1cb6e17f5723cf`  
		Last Modified: Tue, 27 Dec 2016 18:18:49 GMT  
		Size: 2.3 MB (2313090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35b5d4ba733e908c71bed7a1d96ec3f44037f5867bb325e5d2da54a4a2c52789`  
		Last Modified: Tue, 31 Jan 2017 17:45:17 GMT  
		Size: 15.6 MB (15639296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a68a7c476e0d1ce302db758f83e2d783c025821ec5f691a050903bda7e3155b`  
		Last Modified: Tue, 31 Jan 2017 17:45:13 GMT  
		Size: 488.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4049f7dc70f68b4c52eb4d7a206a82925665b124aa7f4838ce8d1524d1370e9b`  
		Last Modified: Tue, 31 Jan 2017 17:45:11 GMT  
		Size: 626.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
