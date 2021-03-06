## `r-base:latest`

```console
$ docker pull r-base@sha256:bb8a9751cfaa2cbef3f26201e6adcc4a99d034c7dce841da963c033e7a14057c
```

-	Platforms:
	-	linux; amd64

### `r-base:latest` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.1 MB (283126288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c7b11f30258bb4c05ca84306935075bdd7c384a1a0c114d087e870246f840d4`
-	Default Command: `["R"]`

```dockerfile
# Mon, 16 Jan 2017 20:40:08 GMT
ADD file:639e1728ddd61dcdf4ff96298c1e817ce503c12226fae69dd8096bb75c8b743d in / 
# Mon, 16 Jan 2017 20:40:16 GMT
CMD ["/bin/bash"]
# Tue, 17 Jan 2017 19:51:58 GMT
MAINTAINER "Carl Boettiger and Dirk Eddelbuettel" rocker-maintainers@eddelbuettel.com
# Tue, 17 Jan 2017 19:52:00 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Tue, 17 Jan 2017 19:52:19 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Jan 2017 19:52:21 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 17 Jan 2017 19:52:21 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 17 Jan 2017 19:52:21 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Jan 2017 19:52:22 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list 	&& echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default
# Tue, 17 Jan 2017 19:52:23 GMT
ENV R_BASE_VERSION=3.3.2
# Tue, 17 Jan 2017 19:56:24 GMT
RUN apt-get update 	&& apt-get install -t unstable -y --no-install-recommends 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}* 		r-base-dev=${R_BASE_VERSION}* 		r-recommended=${R_BASE_VERSION}*         && echo 'options(repos = c(CRAN = "https://cran.rstudio.com/"), download.file.method = "libcurl")' >> /etc/R/Rprofile.site         && echo 'source("/etc/R/Rprofile.site")' >> /etc/littler.r 	&& ln -s /usr/share/doc/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/share/doc/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/share/doc/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/share/doc/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Jan 2017 19:56:25 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:7c680b6659da0add368c25d34d40dbe2c3deb6ddcea465183c8545f904d538cb`  
		Last Modified: Mon, 16 Jan 2017 20:51:13 GMT  
		Size: 43.9 MB (43871391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:829cfa2808f7ea3c3b0a76d10a2f7775ea780d23e96609a902ac10d4fec04f4d`  
		Last Modified: Wed, 18 Jan 2017 07:09:02 GMT  
		Size: 1.8 KB (1832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b79a2aa56cc0cc0deb37c2d79d2ff830109fdfcead94442be95a5efeac26a7`  
		Last Modified: Wed, 18 Jan 2017 07:09:15 GMT  
		Size: 37.3 MB (37298787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:303458286239a01febca0184c1a1cf4eb89bc3ac0ded8b5f4893e94f8b44e4a7`  
		Last Modified: Wed, 18 Jan 2017 07:09:05 GMT  
		Size: 341.0 KB (340955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0051f83b6fe6112928bf06939e9f172b1a2cc3c71d16aafa150539773c1575c`  
		Last Modified: Wed, 18 Jan 2017 07:09:02 GMT  
		Size: 290.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4098981d02705239c501ecdcf403863dc8b89d187027e7edf7680e2c573f368`  
		Last Modified: Wed, 18 Jan 2017 07:10:00 GMT  
		Size: 201.6 MB (201613033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
