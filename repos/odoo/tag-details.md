<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:8.0`](#odoo80)
-	[`odoo:8`](#odoo8)
-	[`odoo:9.0`](#odoo90)
-	[`odoo:9`](#odoo9)
-	[`odoo:10.0`](#odoo100)
-	[`odoo:10`](#odoo10)
-	[`odoo:latest`](#odoolatest)

## `odoo:8.0`

```console
$ docker pull odoo@sha256:b2e2bbaab4b5868ff1ed48ed4ae7dc5fde662e4bf0de5f1017c05bf7906e3593
```

-	Platforms:
	-	linux; amd64

### `odoo:8.0` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268892458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebc8a1d2334bf555041f46886e953adfb571cb07414cfe42901dcd1c2261927`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["openerp-server"]`

```dockerfile
# Mon, 16 Jan 2017 20:35:09 GMT
ADD file:89ecb642d662ee7edbb868340551106d51336c7e589fdaca4111725ec64da957 in / 
# Mon, 16 Jan 2017 20:35:16 GMT
CMD ["/bin/bash"]
# Tue, 17 Jan 2017 18:45:20 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 17 Jan 2017 18:48:14 GMT
RUN set -x;         apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             node-less             node-clean-css             python-gevent             python-pip             python-pyinotify             python-renderpm             python-support         && curl -o wkhtmltox.deb -SL http://nightly.odoo.com/extra/wkhtmltox-0.12.1.2_linux-jessie-amd64.deb         && echo '40e8b906de658a2221b15e4e8cd82565a47d7ee8 wkhtmltox.deb' | sha1sum -c -         && dpkg --force-depends -i wkhtmltox.deb         && apt-get -y install -f --no-install-recommends         && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false -o APT::AutoRemove::SuggestsImportant=false npm         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb         && pip install psycogreen==1.0
# Tue, 17 Jan 2017 18:48:14 GMT
ENV ODOO_VERSION=8.0
# Tue, 07 Feb 2017 21:42:35 GMT
ENV ODOO_RELEASE=20170207
# Tue, 07 Feb 2017 21:43:59 GMT
RUN set -x;         curl -o odoo.deb -SL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo 'cd8c1dc9d2ddf5a538381eed85871a2e343ec8ae odoo.deb' | sha1sum -c -         && dpkg --force-depends -i odoo.deb         && apt-get update         && apt-get -y install -f --no-install-recommends         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 07 Feb 2017 21:44:13 GMT
COPY file:b514c2e8f66799bc707e194d35e0ef442ee72b46668e42cdfee105b6445d7eb0 in / 
# Tue, 07 Feb 2017 21:44:14 GMT
COPY file:1172e26dac1f2b6dd4d3b3ae484c69b33109695606154cdb13dcfa032d798e88 in /etc/odoo/ 
# Tue, 07 Feb 2017 21:44:15 GMT
RUN chown odoo /etc/odoo/openerp-server.conf
# Tue, 07 Feb 2017 21:44:16 GMT
RUN mkdir -p /mnt/extra-addons         && chown -R odoo /mnt/extra-addons
# Tue, 07 Feb 2017 21:44:17 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 07 Feb 2017 21:44:17 GMT
EXPOSE 8069/tcp 8071/tcp
# Tue, 07 Feb 2017 21:44:18 GMT
ENV OPENERP_SERVER=/etc/odoo/openerp-server.conf
# Tue, 07 Feb 2017 21:44:18 GMT
USER [odoo]
# Tue, 07 Feb 2017 21:44:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Feb 2017 21:44:19 GMT
CMD ["openerp-server"]
```

-	Layers:
	-	`sha256:5040bd2983909aa8896b9932438c3f1479d25ae837a5f6220242a264d0221f2d`  
		Last Modified: Mon, 16 Jan 2017 20:43:26 GMT  
		Size: 51.4 MB (51361210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e03bdb4ff8c51a4a8b6bdaf0f002397a53bb36c596e070a6d8837ba4b1fa078b`  
		Last Modified: Wed, 18 Jan 2017 06:10:51 GMT  
		Size: 86.3 MB (86289690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8100ac0f660af5620f95656d6eab20835b9d28ba54669dd0c774d2e62442c199`  
		Last Modified: Tue, 07 Feb 2017 21:52:20 GMT  
		Size: 131.2 MB (131239646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8e3ee5ac6b8e8f72176e5f93177b7558671d694878fe4a5e742f5cced750e3`  
		Last Modified: Tue, 07 Feb 2017 21:51:23 GMT  
		Size: 610.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3971985f493de0bffbee24eeb9694fd61486e966bfeb229710563ce0ceccac4d`  
		Last Modified: Tue, 07 Feb 2017 21:51:23 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942ead8e24e7e822ca60123279285c0b5cb37023c94eb88f7aab1084d87007fa`  
		Last Modified: Tue, 07 Feb 2017 21:51:23 GMT  
		Size: 591.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:421585eb0a83c211d04355464ca2452c7a9bab2fc754a58de85f8d22d0666966`  
		Last Modified: Tue, 07 Feb 2017 21:51:22 GMT  
		Size: 123.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:8`

```console
$ docker pull odoo@sha256:b2e2bbaab4b5868ff1ed48ed4ae7dc5fde662e4bf0de5f1017c05bf7906e3593
```

-	Platforms:
	-	linux; amd64

### `odoo:8` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268892458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebc8a1d2334bf555041f46886e953adfb571cb07414cfe42901dcd1c2261927`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["openerp-server"]`

```dockerfile
# Mon, 16 Jan 2017 20:35:09 GMT
ADD file:89ecb642d662ee7edbb868340551106d51336c7e589fdaca4111725ec64da957 in / 
# Mon, 16 Jan 2017 20:35:16 GMT
CMD ["/bin/bash"]
# Tue, 17 Jan 2017 18:45:20 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 17 Jan 2017 18:48:14 GMT
RUN set -x;         apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             node-less             node-clean-css             python-gevent             python-pip             python-pyinotify             python-renderpm             python-support         && curl -o wkhtmltox.deb -SL http://nightly.odoo.com/extra/wkhtmltox-0.12.1.2_linux-jessie-amd64.deb         && echo '40e8b906de658a2221b15e4e8cd82565a47d7ee8 wkhtmltox.deb' | sha1sum -c -         && dpkg --force-depends -i wkhtmltox.deb         && apt-get -y install -f --no-install-recommends         && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false -o APT::AutoRemove::SuggestsImportant=false npm         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb         && pip install psycogreen==1.0
# Tue, 17 Jan 2017 18:48:14 GMT
ENV ODOO_VERSION=8.0
# Tue, 07 Feb 2017 21:42:35 GMT
ENV ODOO_RELEASE=20170207
# Tue, 07 Feb 2017 21:43:59 GMT
RUN set -x;         curl -o odoo.deb -SL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo 'cd8c1dc9d2ddf5a538381eed85871a2e343ec8ae odoo.deb' | sha1sum -c -         && dpkg --force-depends -i odoo.deb         && apt-get update         && apt-get -y install -f --no-install-recommends         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 07 Feb 2017 21:44:13 GMT
COPY file:b514c2e8f66799bc707e194d35e0ef442ee72b46668e42cdfee105b6445d7eb0 in / 
# Tue, 07 Feb 2017 21:44:14 GMT
COPY file:1172e26dac1f2b6dd4d3b3ae484c69b33109695606154cdb13dcfa032d798e88 in /etc/odoo/ 
# Tue, 07 Feb 2017 21:44:15 GMT
RUN chown odoo /etc/odoo/openerp-server.conf
# Tue, 07 Feb 2017 21:44:16 GMT
RUN mkdir -p /mnt/extra-addons         && chown -R odoo /mnt/extra-addons
# Tue, 07 Feb 2017 21:44:17 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 07 Feb 2017 21:44:17 GMT
EXPOSE 8069/tcp 8071/tcp
# Tue, 07 Feb 2017 21:44:18 GMT
ENV OPENERP_SERVER=/etc/odoo/openerp-server.conf
# Tue, 07 Feb 2017 21:44:18 GMT
USER [odoo]
# Tue, 07 Feb 2017 21:44:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Feb 2017 21:44:19 GMT
CMD ["openerp-server"]
```

-	Layers:
	-	`sha256:5040bd2983909aa8896b9932438c3f1479d25ae837a5f6220242a264d0221f2d`  
		Last Modified: Mon, 16 Jan 2017 20:43:26 GMT  
		Size: 51.4 MB (51361210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e03bdb4ff8c51a4a8b6bdaf0f002397a53bb36c596e070a6d8837ba4b1fa078b`  
		Last Modified: Wed, 18 Jan 2017 06:10:51 GMT  
		Size: 86.3 MB (86289690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8100ac0f660af5620f95656d6eab20835b9d28ba54669dd0c774d2e62442c199`  
		Last Modified: Tue, 07 Feb 2017 21:52:20 GMT  
		Size: 131.2 MB (131239646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8e3ee5ac6b8e8f72176e5f93177b7558671d694878fe4a5e742f5cced750e3`  
		Last Modified: Tue, 07 Feb 2017 21:51:23 GMT  
		Size: 610.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3971985f493de0bffbee24eeb9694fd61486e966bfeb229710563ce0ceccac4d`  
		Last Modified: Tue, 07 Feb 2017 21:51:23 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942ead8e24e7e822ca60123279285c0b5cb37023c94eb88f7aab1084d87007fa`  
		Last Modified: Tue, 07 Feb 2017 21:51:23 GMT  
		Size: 591.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:421585eb0a83c211d04355464ca2452c7a9bab2fc754a58de85f8d22d0666966`  
		Last Modified: Tue, 07 Feb 2017 21:51:22 GMT  
		Size: 123.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:9.0`

```console
$ docker pull odoo@sha256:ef621794806be5af316a5ee39ee8c87ffbdcdc91216243858ade8d7ac1618b74
```

-	Platforms:
	-	linux; amd64

### `odoo:9.0` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.6 MB (284636380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c51e6c88f2d2e9cd1cfe239ec467c5e47c7bd7a9b1398554c27c2c7439678af`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["openerp-server"]`

```dockerfile
# Mon, 16 Jan 2017 20:35:09 GMT
ADD file:89ecb642d662ee7edbb868340551106d51336c7e589fdaca4111725ec64da957 in / 
# Mon, 16 Jan 2017 20:35:16 GMT
CMD ["/bin/bash"]
# Tue, 17 Jan 2017 18:45:20 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 07 Feb 2017 21:45:00 GMT
RUN set -x;         apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             node-less             python-gevent             python-pip             python-renderpm             python-support             python-watchdog         && curl -o wkhtmltox.deb -SL http://nightly.odoo.com/extra/wkhtmltox-0.12.1.2_linux-jessie-amd64.deb         && echo '40e8b906de658a2221b15e4e8cd82565a47d7ee8 wkhtmltox.deb' | sha1sum -c -         && dpkg --force-depends -i wkhtmltox.deb         && apt-get -y install -f --no-install-recommends         && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false -o APT::AutoRemove::SuggestsImportant=false npm         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb         && pip install psycogreen==1.0
# Tue, 07 Feb 2017 21:45:07 GMT
ENV ODOO_VERSION=9.0
# Tue, 07 Feb 2017 21:45:08 GMT
ENV ODOO_RELEASE=20170207
# Tue, 07 Feb 2017 21:46:39 GMT
RUN set -x;         curl -o odoo.deb -SL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}c.${ODOO_RELEASE}_all.deb         && echo '4ff504f4b2a49667a0bc8bbca95079305d8108c8 odoo.deb' | sha1sum -c -         && dpkg --force-depends -i odoo.deb         && apt-get update         && apt-get -y install -f --no-install-recommends         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 07 Feb 2017 21:46:41 GMT
COPY file:b514c2e8f66799bc707e194d35e0ef442ee72b46668e42cdfee105b6445d7eb0 in / 
# Tue, 07 Feb 2017 21:46:42 GMT
COPY file:5bf1f863cb98f8aeeac8f1a8430f1af56358cee4a6e5ade3b2c00fb3fc8d4162 in /etc/odoo/ 
# Tue, 07 Feb 2017 21:46:44 GMT
RUN chown odoo /etc/odoo/openerp-server.conf
# Tue, 07 Feb 2017 21:46:45 GMT
RUN mkdir -p /mnt/extra-addons         && chown -R odoo /mnt/extra-addons
# Tue, 07 Feb 2017 21:46:46 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 07 Feb 2017 21:46:46 GMT
EXPOSE 8069/tcp 8071/tcp
# Tue, 07 Feb 2017 21:46:47 GMT
ENV OPENERP_SERVER=/etc/odoo/openerp-server.conf
# Tue, 07 Feb 2017 21:46:47 GMT
USER [odoo]
# Tue, 07 Feb 2017 21:46:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Feb 2017 21:46:48 GMT
CMD ["openerp-server"]
```

-	Layers:
	-	`sha256:5040bd2983909aa8896b9932438c3f1479d25ae837a5f6220242a264d0221f2d`  
		Last Modified: Mon, 16 Jan 2017 20:43:26 GMT  
		Size: 51.4 MB (51361210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b964bb84dc923fb155278c755e5db0292ccfd322dbb3e10e942ee2195bc0d59b`  
		Last Modified: Tue, 07 Feb 2017 21:53:32 GMT  
		Size: 86.7 MB (86671184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32471c9460ff7c8a59a7993dc2b21622b3c467d7f32ca0d115fc730acea0c28b`  
		Last Modified: Tue, 07 Feb 2017 21:54:02 GMT  
		Size: 146.6 MB (146602091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80fec2cde9459a489bf4b9b53c42685d32d98d64f6811f1a1571ed000953a91c`  
		Last Modified: Tue, 07 Feb 2017 21:52:59 GMT  
		Size: 610.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d27cf1e56ae13939e7cd49683c3305261085552b02c0f9c3939443fe6892319`  
		Last Modified: Tue, 07 Feb 2017 21:52:59 GMT  
		Size: 580.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98840f0ccecc25e7e031ac02a02890ec47c0ffc145fc145d03c6970378c5281e`  
		Last Modified: Tue, 07 Feb 2017 21:52:59 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250ac63c34f0303f2bb6e75f213efecd4a2458704a53d902ad10d0a3b5e5c50d`  
		Last Modified: Tue, 07 Feb 2017 21:52:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:9`

```console
$ docker pull odoo@sha256:ef621794806be5af316a5ee39ee8c87ffbdcdc91216243858ade8d7ac1618b74
```

-	Platforms:
	-	linux; amd64

### `odoo:9` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.6 MB (284636380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c51e6c88f2d2e9cd1cfe239ec467c5e47c7bd7a9b1398554c27c2c7439678af`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["openerp-server"]`

```dockerfile
# Mon, 16 Jan 2017 20:35:09 GMT
ADD file:89ecb642d662ee7edbb868340551106d51336c7e589fdaca4111725ec64da957 in / 
# Mon, 16 Jan 2017 20:35:16 GMT
CMD ["/bin/bash"]
# Tue, 17 Jan 2017 18:45:20 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 07 Feb 2017 21:45:00 GMT
RUN set -x;         apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             node-less             python-gevent             python-pip             python-renderpm             python-support             python-watchdog         && curl -o wkhtmltox.deb -SL http://nightly.odoo.com/extra/wkhtmltox-0.12.1.2_linux-jessie-amd64.deb         && echo '40e8b906de658a2221b15e4e8cd82565a47d7ee8 wkhtmltox.deb' | sha1sum -c -         && dpkg --force-depends -i wkhtmltox.deb         && apt-get -y install -f --no-install-recommends         && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false -o APT::AutoRemove::SuggestsImportant=false npm         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb         && pip install psycogreen==1.0
# Tue, 07 Feb 2017 21:45:07 GMT
ENV ODOO_VERSION=9.0
# Tue, 07 Feb 2017 21:45:08 GMT
ENV ODOO_RELEASE=20170207
# Tue, 07 Feb 2017 21:46:39 GMT
RUN set -x;         curl -o odoo.deb -SL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}c.${ODOO_RELEASE}_all.deb         && echo '4ff504f4b2a49667a0bc8bbca95079305d8108c8 odoo.deb' | sha1sum -c -         && dpkg --force-depends -i odoo.deb         && apt-get update         && apt-get -y install -f --no-install-recommends         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 07 Feb 2017 21:46:41 GMT
COPY file:b514c2e8f66799bc707e194d35e0ef442ee72b46668e42cdfee105b6445d7eb0 in / 
# Tue, 07 Feb 2017 21:46:42 GMT
COPY file:5bf1f863cb98f8aeeac8f1a8430f1af56358cee4a6e5ade3b2c00fb3fc8d4162 in /etc/odoo/ 
# Tue, 07 Feb 2017 21:46:44 GMT
RUN chown odoo /etc/odoo/openerp-server.conf
# Tue, 07 Feb 2017 21:46:45 GMT
RUN mkdir -p /mnt/extra-addons         && chown -R odoo /mnt/extra-addons
# Tue, 07 Feb 2017 21:46:46 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 07 Feb 2017 21:46:46 GMT
EXPOSE 8069/tcp 8071/tcp
# Tue, 07 Feb 2017 21:46:47 GMT
ENV OPENERP_SERVER=/etc/odoo/openerp-server.conf
# Tue, 07 Feb 2017 21:46:47 GMT
USER [odoo]
# Tue, 07 Feb 2017 21:46:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Feb 2017 21:46:48 GMT
CMD ["openerp-server"]
```

-	Layers:
	-	`sha256:5040bd2983909aa8896b9932438c3f1479d25ae837a5f6220242a264d0221f2d`  
		Last Modified: Mon, 16 Jan 2017 20:43:26 GMT  
		Size: 51.4 MB (51361210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b964bb84dc923fb155278c755e5db0292ccfd322dbb3e10e942ee2195bc0d59b`  
		Last Modified: Tue, 07 Feb 2017 21:53:32 GMT  
		Size: 86.7 MB (86671184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32471c9460ff7c8a59a7993dc2b21622b3c467d7f32ca0d115fc730acea0c28b`  
		Last Modified: Tue, 07 Feb 2017 21:54:02 GMT  
		Size: 146.6 MB (146602091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80fec2cde9459a489bf4b9b53c42685d32d98d64f6811f1a1571ed000953a91c`  
		Last Modified: Tue, 07 Feb 2017 21:52:59 GMT  
		Size: 610.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d27cf1e56ae13939e7cd49683c3305261085552b02c0f9c3939443fe6892319`  
		Last Modified: Tue, 07 Feb 2017 21:52:59 GMT  
		Size: 580.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98840f0ccecc25e7e031ac02a02890ec47c0ffc145fc145d03c6970378c5281e`  
		Last Modified: Tue, 07 Feb 2017 21:52:59 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250ac63c34f0303f2bb6e75f213efecd4a2458704a53d902ad10d0a3b5e5c50d`  
		Last Modified: Tue, 07 Feb 2017 21:52:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:10.0`

```console
$ docker pull odoo@sha256:1d4119b195a0520b7b568c0cb800a4a21097d6e65f4a3612f082c66510a48d07
```

-	Platforms:
	-	linux; amd64

### `odoo:10.0` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.3 MB (269280023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:521d6cf51841533c0fd52783035578458701a3e54332dd149ce070a40eb9cd64`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`

```dockerfile
# Mon, 16 Jan 2017 20:35:09 GMT
ADD file:89ecb642d662ee7edbb868340551106d51336c7e589fdaca4111725ec64da957 in / 
# Mon, 16 Jan 2017 20:35:16 GMT
CMD ["/bin/bash"]
# Tue, 17 Jan 2017 18:45:20 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 07 Feb 2017 21:45:00 GMT
RUN set -x;         apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             node-less             python-gevent             python-pip             python-renderpm             python-support             python-watchdog         && curl -o wkhtmltox.deb -SL http://nightly.odoo.com/extra/wkhtmltox-0.12.1.2_linux-jessie-amd64.deb         && echo '40e8b906de658a2221b15e4e8cd82565a47d7ee8 wkhtmltox.deb' | sha1sum -c -         && dpkg --force-depends -i wkhtmltox.deb         && apt-get -y install -f --no-install-recommends         && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false -o APT::AutoRemove::SuggestsImportant=false npm         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb         && pip install psycogreen==1.0
# Tue, 07 Feb 2017 21:46:49 GMT
ENV ODOO_VERSION=10.0
# Tue, 07 Feb 2017 21:46:50 GMT
ENV ODOO_RELEASE=20170207
# Tue, 07 Feb 2017 21:48:05 GMT
RUN set -x;         curl -o odoo.deb -SL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo '5d2fb0cc03fa0795a7b2186bb341caa74d372e82 odoo.deb' | sha1sum -c -         && dpkg --force-depends -i odoo.deb         && apt-get update         && apt-get -y install -f --no-install-recommends         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 07 Feb 2017 21:48:07 GMT
COPY file:33fddeba88e5214ff2c7cd05a02348dc417a5de70b767d6ff559e871ee6d046a in / 
# Tue, 07 Feb 2017 21:48:07 GMT
COPY file:18e3dbead2bc096fe44ef1cfaa2a6e8dc1b27daeeb1d281cfdd552b805f2e767 in /etc/odoo/ 
# Tue, 07 Feb 2017 21:48:09 GMT
RUN chown odoo /etc/odoo/odoo.conf
# Tue, 07 Feb 2017 21:48:10 GMT
RUN mkdir -p /mnt/extra-addons         && chown -R odoo /mnt/extra-addons
# Tue, 07 Feb 2017 21:48:10 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 07 Feb 2017 21:48:11 GMT
EXPOSE 8069/tcp 8071/tcp
# Tue, 07 Feb 2017 21:48:11 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 07 Feb 2017 21:48:12 GMT
USER [odoo]
# Tue, 07 Feb 2017 21:48:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Feb 2017 21:48:13 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5040bd2983909aa8896b9932438c3f1479d25ae837a5f6220242a264d0221f2d`  
		Last Modified: Mon, 16 Jan 2017 20:43:26 GMT  
		Size: 51.4 MB (51361210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b964bb84dc923fb155278c755e5db0292ccfd322dbb3e10e942ee2195bc0d59b`  
		Last Modified: Tue, 07 Feb 2017 21:53:32 GMT  
		Size: 86.7 MB (86671184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57cffaa3a36f16e17f29be455d25f6f2f20138c20c47fe032cab88fd98c7ff70`  
		Last Modified: Tue, 07 Feb 2017 21:55:33 GMT  
		Size: 131.2 MB (131245766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb5f8ef650c7de5706bf7bf44e3a7a55eed1029609de61c026b05a3597913896`  
		Last Modified: Tue, 07 Feb 2017 21:54:40 GMT  
		Size: 594.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b2872261b9bc7e1cb01b814f9cbfe753430687ae21be8c805c4ab07df0cf0c`  
		Last Modified: Tue, 07 Feb 2017 21:54:41 GMT  
		Size: 572.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dc4b6b5d259ecd7eb3eb15527296273c8ce621073ebe423d4f3b858772efded`  
		Last Modified: Tue, 07 Feb 2017 21:54:40 GMT  
		Size: 574.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf13d0120c417b1ac140ea4a7bedb9383d14c817b220f7283c4a4710d7a4f5fe`  
		Last Modified: Tue, 07 Feb 2017 21:54:40 GMT  
		Size: 123.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:10`

```console
$ docker pull odoo@sha256:1d4119b195a0520b7b568c0cb800a4a21097d6e65f4a3612f082c66510a48d07
```

-	Platforms:
	-	linux; amd64

### `odoo:10` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.3 MB (269280023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:521d6cf51841533c0fd52783035578458701a3e54332dd149ce070a40eb9cd64`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`

```dockerfile
# Mon, 16 Jan 2017 20:35:09 GMT
ADD file:89ecb642d662ee7edbb868340551106d51336c7e589fdaca4111725ec64da957 in / 
# Mon, 16 Jan 2017 20:35:16 GMT
CMD ["/bin/bash"]
# Tue, 17 Jan 2017 18:45:20 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 07 Feb 2017 21:45:00 GMT
RUN set -x;         apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             node-less             python-gevent             python-pip             python-renderpm             python-support             python-watchdog         && curl -o wkhtmltox.deb -SL http://nightly.odoo.com/extra/wkhtmltox-0.12.1.2_linux-jessie-amd64.deb         && echo '40e8b906de658a2221b15e4e8cd82565a47d7ee8 wkhtmltox.deb' | sha1sum -c -         && dpkg --force-depends -i wkhtmltox.deb         && apt-get -y install -f --no-install-recommends         && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false -o APT::AutoRemove::SuggestsImportant=false npm         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb         && pip install psycogreen==1.0
# Tue, 07 Feb 2017 21:46:49 GMT
ENV ODOO_VERSION=10.0
# Tue, 07 Feb 2017 21:46:50 GMT
ENV ODOO_RELEASE=20170207
# Tue, 07 Feb 2017 21:48:05 GMT
RUN set -x;         curl -o odoo.deb -SL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo '5d2fb0cc03fa0795a7b2186bb341caa74d372e82 odoo.deb' | sha1sum -c -         && dpkg --force-depends -i odoo.deb         && apt-get update         && apt-get -y install -f --no-install-recommends         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 07 Feb 2017 21:48:07 GMT
COPY file:33fddeba88e5214ff2c7cd05a02348dc417a5de70b767d6ff559e871ee6d046a in / 
# Tue, 07 Feb 2017 21:48:07 GMT
COPY file:18e3dbead2bc096fe44ef1cfaa2a6e8dc1b27daeeb1d281cfdd552b805f2e767 in /etc/odoo/ 
# Tue, 07 Feb 2017 21:48:09 GMT
RUN chown odoo /etc/odoo/odoo.conf
# Tue, 07 Feb 2017 21:48:10 GMT
RUN mkdir -p /mnt/extra-addons         && chown -R odoo /mnt/extra-addons
# Tue, 07 Feb 2017 21:48:10 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 07 Feb 2017 21:48:11 GMT
EXPOSE 8069/tcp 8071/tcp
# Tue, 07 Feb 2017 21:48:11 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 07 Feb 2017 21:48:12 GMT
USER [odoo]
# Tue, 07 Feb 2017 21:48:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Feb 2017 21:48:13 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5040bd2983909aa8896b9932438c3f1479d25ae837a5f6220242a264d0221f2d`  
		Last Modified: Mon, 16 Jan 2017 20:43:26 GMT  
		Size: 51.4 MB (51361210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b964bb84dc923fb155278c755e5db0292ccfd322dbb3e10e942ee2195bc0d59b`  
		Last Modified: Tue, 07 Feb 2017 21:53:32 GMT  
		Size: 86.7 MB (86671184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57cffaa3a36f16e17f29be455d25f6f2f20138c20c47fe032cab88fd98c7ff70`  
		Last Modified: Tue, 07 Feb 2017 21:55:33 GMT  
		Size: 131.2 MB (131245766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb5f8ef650c7de5706bf7bf44e3a7a55eed1029609de61c026b05a3597913896`  
		Last Modified: Tue, 07 Feb 2017 21:54:40 GMT  
		Size: 594.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b2872261b9bc7e1cb01b814f9cbfe753430687ae21be8c805c4ab07df0cf0c`  
		Last Modified: Tue, 07 Feb 2017 21:54:41 GMT  
		Size: 572.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dc4b6b5d259ecd7eb3eb15527296273c8ce621073ebe423d4f3b858772efded`  
		Last Modified: Tue, 07 Feb 2017 21:54:40 GMT  
		Size: 574.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf13d0120c417b1ac140ea4a7bedb9383d14c817b220f7283c4a4710d7a4f5fe`  
		Last Modified: Tue, 07 Feb 2017 21:54:40 GMT  
		Size: 123.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:1d4119b195a0520b7b568c0cb800a4a21097d6e65f4a3612f082c66510a48d07
```

-	Platforms:
	-	linux; amd64

### `odoo:latest` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.3 MB (269280023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:521d6cf51841533c0fd52783035578458701a3e54332dd149ce070a40eb9cd64`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`

```dockerfile
# Mon, 16 Jan 2017 20:35:09 GMT
ADD file:89ecb642d662ee7edbb868340551106d51336c7e589fdaca4111725ec64da957 in / 
# Mon, 16 Jan 2017 20:35:16 GMT
CMD ["/bin/bash"]
# Tue, 17 Jan 2017 18:45:20 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 07 Feb 2017 21:45:00 GMT
RUN set -x;         apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             node-less             python-gevent             python-pip             python-renderpm             python-support             python-watchdog         && curl -o wkhtmltox.deb -SL http://nightly.odoo.com/extra/wkhtmltox-0.12.1.2_linux-jessie-amd64.deb         && echo '40e8b906de658a2221b15e4e8cd82565a47d7ee8 wkhtmltox.deb' | sha1sum -c -         && dpkg --force-depends -i wkhtmltox.deb         && apt-get -y install -f --no-install-recommends         && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false -o APT::AutoRemove::SuggestsImportant=false npm         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb         && pip install psycogreen==1.0
# Tue, 07 Feb 2017 21:46:49 GMT
ENV ODOO_VERSION=10.0
# Tue, 07 Feb 2017 21:46:50 GMT
ENV ODOO_RELEASE=20170207
# Tue, 07 Feb 2017 21:48:05 GMT
RUN set -x;         curl -o odoo.deb -SL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo '5d2fb0cc03fa0795a7b2186bb341caa74d372e82 odoo.deb' | sha1sum -c -         && dpkg --force-depends -i odoo.deb         && apt-get update         && apt-get -y install -f --no-install-recommends         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 07 Feb 2017 21:48:07 GMT
COPY file:33fddeba88e5214ff2c7cd05a02348dc417a5de70b767d6ff559e871ee6d046a in / 
# Tue, 07 Feb 2017 21:48:07 GMT
COPY file:18e3dbead2bc096fe44ef1cfaa2a6e8dc1b27daeeb1d281cfdd552b805f2e767 in /etc/odoo/ 
# Tue, 07 Feb 2017 21:48:09 GMT
RUN chown odoo /etc/odoo/odoo.conf
# Tue, 07 Feb 2017 21:48:10 GMT
RUN mkdir -p /mnt/extra-addons         && chown -R odoo /mnt/extra-addons
# Tue, 07 Feb 2017 21:48:10 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 07 Feb 2017 21:48:11 GMT
EXPOSE 8069/tcp 8071/tcp
# Tue, 07 Feb 2017 21:48:11 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 07 Feb 2017 21:48:12 GMT
USER [odoo]
# Tue, 07 Feb 2017 21:48:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Feb 2017 21:48:13 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5040bd2983909aa8896b9932438c3f1479d25ae837a5f6220242a264d0221f2d`  
		Last Modified: Mon, 16 Jan 2017 20:43:26 GMT  
		Size: 51.4 MB (51361210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b964bb84dc923fb155278c755e5db0292ccfd322dbb3e10e942ee2195bc0d59b`  
		Last Modified: Tue, 07 Feb 2017 21:53:32 GMT  
		Size: 86.7 MB (86671184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57cffaa3a36f16e17f29be455d25f6f2f20138c20c47fe032cab88fd98c7ff70`  
		Last Modified: Tue, 07 Feb 2017 21:55:33 GMT  
		Size: 131.2 MB (131245766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb5f8ef650c7de5706bf7bf44e3a7a55eed1029609de61c026b05a3597913896`  
		Last Modified: Tue, 07 Feb 2017 21:54:40 GMT  
		Size: 594.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b2872261b9bc7e1cb01b814f9cbfe753430687ae21be8c805c4ab07df0cf0c`  
		Last Modified: Tue, 07 Feb 2017 21:54:41 GMT  
		Size: 572.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dc4b6b5d259ecd7eb3eb15527296273c8ce621073ebe423d4f3b858772efded`  
		Last Modified: Tue, 07 Feb 2017 21:54:40 GMT  
		Size: 574.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf13d0120c417b1ac140ea4a7bedb9383d14c817b220f7283c4a4710d7a4f5fe`  
		Last Modified: Tue, 07 Feb 2017 21:54:40 GMT  
		Size: 123.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
