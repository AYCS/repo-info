## `vault:latest`

```console
$ docker pull vault@sha256:43720b6db6ca01bce18fb60a7aadea8e4b5cc70ae6451152703db47451b6c756
```

-	Platforms:
	-	linux; amd64

### `vault:latest` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16992723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eb63fad30d88a62ce4ef83ce4d16eaf71dd5381986fdb40e44ea2246ee64025`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 27 Dec 2016 18:17:13 GMT
ADD file:eeed5f514a35d18fcd9cbfe6c40c582211020bffdd53e4799018d33826fe5067 in / 
# Tue, 27 Dec 2016 22:08:25 GMT
MAINTAINER Jeff Mitchell <jeff@hashicorp.com> (@jefferai)
# Wed, 08 Feb 2017 18:51:05 GMT
ENV VAULT_VERSION=0.6.5
# Wed, 08 Feb 2017 18:51:05 GMT
ENV DOCKER_BASE_VERSION=0.0.4
# Wed, 08 Feb 2017 18:51:06 GMT
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 08 Feb 2017 18:51:20 GMT
RUN apk add --no-cache ca-certificates gnupg openssl libcap &&     gpg --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/docker-base/${DOCKER_BASE_VERSION}/docker-base_${DOCKER_BASE_VERSION}_linux_amd64.zip &&     wget https://releases.hashicorp.com/docker-base/${DOCKER_BASE_VERSION}/docker-base_${DOCKER_BASE_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/docker-base/${DOCKER_BASE_VERSION}/docker-base_${DOCKER_BASE_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify docker-base_${DOCKER_BASE_VERSION}_SHA256SUMS.sig docker-base_${DOCKER_BASE_VERSION}_SHA256SUMS &&     grep ${DOCKER_BASE_VERSION}_linux_amd64.zip docker-base_${DOCKER_BASE_VERSION}_SHA256SUMS | sha256sum -c &&     unzip docker-base_${DOCKER_BASE_VERSION}_linux_amd64.zip &&     cp bin/gosu bin/dumb-init /bin &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_amd64.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_amd64.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_amd64.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 08 Feb 2017 18:51:21 GMT
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 08 Feb 2017 18:51:22 GMT
VOLUME [/vault/logs]
# Wed, 08 Feb 2017 18:51:22 GMT
VOLUME [/vault/file]
# Wed, 08 Feb 2017 18:51:22 GMT
EXPOSE 8200/tcp
# Wed, 08 Feb 2017 18:51:23 GMT
COPY file:ba639bce844e294b4d0251427ff66d5b257eca29d400982328a19a258fb09db9 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 08 Feb 2017 18:51:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Feb 2017 18:51:23 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:b7f33cc0b48ea4fb2f0745def58c25483a5f6b7aed5b41ce8f1cb6e17f5723cf`  
		Last Modified: Tue, 27 Dec 2016 18:18:49 GMT  
		Size: 2.3 MB (2313090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25efcb05dbe6e6932b855c3447e606f48f522050c2f3f3b5b9daec99d0f9e00b`  
		Last Modified: Wed, 08 Feb 2017 18:51:45 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ece7ce0a313286ae27b1cf07ee0f3fd89b414504a3e2591869404b7730576d4`  
		Last Modified: Wed, 08 Feb 2017 18:51:50 GMT  
		Size: 14.7 MB (14676454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a005893bf7d7eb621b5b7f7c6b62a68d05af0cb94c8380a6abb1625011a9da49`  
		Last Modified: Wed, 08 Feb 2017 18:51:45 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3bbcaacffcf3167fbdc199d825fd89d476af454fc6fb8d8b3fb07d67f176444`  
		Last Modified: Wed, 08 Feb 2017 18:51:45 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
