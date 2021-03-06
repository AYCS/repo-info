## `eclipse-mosquitto:latest`

```console
$ docker pull eclipse-mosquitto@sha256:9fa2640d6c9c4750a3458307d1ec87651d2018511a5daf4810294e5e7d5dceff
```

-	Platforms:
	-	linux; amd64

### `eclipse-mosquitto:latest` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2071982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b7fc98f4b331701d9b50de0e8c866e48d81863a53f63d8c26d4f1948b577a82`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Tue, 27 Dec 2016 18:17:25 GMT
ADD file:92ab746eb22dd3ed2b87469c719adf3c1bed7302653bbd76baafd7cfd95e911e in / 
# Thu, 05 Jan 2017 23:56:30 GMT
MAINTAINER David Audet <david.audet@ca.com>
# Thu, 05 Jan 2017 23:56:30 GMT
LABEL Description=Eclipse Mosquitto MQTT Broker
# Thu, 05 Jan 2017 23:56:33 GMT
RUN apk --no-cache add mosquitto=1.4.10-r2 &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     cp /etc/mosquitto/mosquitto.conf /mosquitto/config &&     chown -R mosquitto:mosquitto /mosquitto
# Thu, 05 Jan 2017 23:56:44 GMT
COPY file:837d39cfa86d29b54b50c161745633f730844caea976da0ece1641e4e4b122aa in / 
# Thu, 05 Jan 2017 23:56:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Jan 2017 23:56:45 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:0a8490d0dfd399b3a50e9aaa81dba0d425c3868762d46526b41be00886bcc28b`  
		Last Modified: Tue, 27 Dec 2016 18:19:22 GMT  
		Size: 1.9 MB (1902063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e75f87f0f26d8b12edbe044a0529e1536d2ab3d83c9e24eea1a235b31f738afd`  
		Last Modified: Thu, 05 Jan 2017 23:57:28 GMT  
		Size: 169.8 KB (169773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e1df5087349fdf5c1080fadead75d430821c8812860885dc6db1109268a41f`  
		Last Modified: Thu, 05 Jan 2017 23:57:28 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
