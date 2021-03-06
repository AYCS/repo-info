## `consul:latest`

```console
$ docker pull consul@sha256:0533f24f0f279a3e202e398828d7f7fc175e11972ba8dc63f48474235b471923
```

-	Platforms:
	-	linux; amd64

### `consul:latest` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12906945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c75c0b979b8791c592ffecc49b575692ebb22a78d30dfec33edbf179619c6c29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 27 Dec 2016 18:17:13 GMT
ADD file:eeed5f514a35d18fcd9cbfe6c40c582211020bffdd53e4799018d33826fe5067 in / 
# Tue, 27 Dec 2016 18:32:29 GMT
MAINTAINER James Phillips <james@hashicorp.com> (@slackpad)
# Mon, 06 Feb 2017 20:24:25 GMT
ENV CONSUL_VERSION=0.7.4
# Mon, 06 Feb 2017 20:24:25 GMT
ENV DOCKER_BASE_VERSION=0.0.4
# Mon, 06 Feb 2017 20:24:26 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Mon, 06 Feb 2017 20:24:27 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Mon, 06 Feb 2017 20:24:34 GMT
RUN apk add --no-cache ca-certificates curl gnupg libcap openssl &&     gpg --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     wget ${HASHICORP_RELEASES}/docker-base/${DOCKER_BASE_VERSION}/docker-base_${DOCKER_BASE_VERSION}_linux_amd64.zip &&     wget ${HASHICORP_RELEASES}/docker-base/${DOCKER_BASE_VERSION}/docker-base_${DOCKER_BASE_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/docker-base/${DOCKER_BASE_VERSION}/docker-base_${DOCKER_BASE_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify docker-base_${DOCKER_BASE_VERSION}_SHA256SUMS.sig docker-base_${DOCKER_BASE_VERSION}_SHA256SUMS &&     grep ${DOCKER_BASE_VERSION}_linux_amd64.zip docker-base_${DOCKER_BASE_VERSION}_SHA256SUMS | sha256sum -c &&     unzip docker-base_${DOCKER_BASE_VERSION}_linux_amd64.zip &&     cp bin/gosu bin/dumb-init /bin &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_amd64.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_amd64.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_amd64.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Mon, 06 Feb 2017 20:24:34 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Mon, 06 Feb 2017 20:24:35 GMT
VOLUME [/consul/data]
# Mon, 06 Feb 2017 20:24:35 GMT
EXPOSE 8300/tcp
# Mon, 06 Feb 2017 20:24:35 GMT
EXPOSE 8301/tcp 8301/udp 8302/tcp 8302/udp
# Mon, 06 Feb 2017 20:24:36 GMT
EXPOSE 8400/tcp 8500/tcp 8600/tcp 8600/udp
# Mon, 06 Feb 2017 20:24:36 GMT
COPY file:de6c9a0e693ae46a375c565826f2071715281bba7f165975eb8537acd0d96ff4 in /usr/local/bin/docker-entrypoint.sh 
# Mon, 06 Feb 2017 20:24:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 Feb 2017 20:24:37 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b7f33cc0b48ea4fb2f0745def58c25483a5f6b7aed5b41ce8f1cb6e17f5723cf`  
		Last Modified: Tue, 27 Dec 2016 18:18:49 GMT  
		Size: 2.3 MB (2313090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ad9bbc276c9d3aa61b8b94c37002a4e3e2b38421079dc1fd4681f233315ed32`  
		Last Modified: Mon, 06 Feb 2017 20:24:54 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3fe64b51e9042c6205b60666484ff7265720343864d53f37f36fcc2bffe215`  
		Last Modified: Mon, 06 Feb 2017 20:24:57 GMT  
		Size: 10.6 MB (10590810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47c212aeb67201d3141a1856288ae9d3e0c6d35bf166c16e9a45d70df86e9c73`  
		Last Modified: Mon, 06 Feb 2017 20:24:53 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955a7f23689af634f6546916b3fd8f3dd5d817d18ab82c014d0c40da479cb48a`  
		Last Modified: Mon, 06 Feb 2017 20:24:53 GMT  
		Size: 1.6 KB (1629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
