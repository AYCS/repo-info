## `golang:1-windowsservercore`

```console
$ docker pull golang@sha256:fbfc1be131b53fc8bfb3d082fadca72b4da75bcd484062b0de8cf1c0ab95d685
```

-	Platforms:
	-	windows; amd64

### `golang:1-windowsservercore` - windows; amd64

-	Docker Version: 1.12.2-cs2-ws-beta
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 GB (5317093563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f54347770e63ccb51e801455ddffc0e6289a477cc295b950835281ba01139f49`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Wed, 18 Jan 2017 00:22:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 18 Jan 2017 00:22:39 GMT
ENV GIT_VERSION=2.11.0
# Wed, 18 Jan 2017 00:22:41 GMT
ENV GIT_TAG=v2.11.0.windows.1
# Wed, 18 Jan 2017 00:22:44 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.11.0.windows.1/Git-2.11.0-64-bit.exe
# Wed, 18 Jan 2017 00:22:47 GMT
ENV GIT_DOWNLOAD_SHA256=fd1937ea8468461d35d9cabfcdd2daa3a74509dc9213c43c2b9615e8f0b85086
# Wed, 18 Jan 2017 00:26:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.exe -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-Wait 		-FilePath ./git.exe 		-ArgumentList @( 			'/VERYSILENT', 			'/NORESTART', 			'/NOCANCEL', 			'/SP-', 			'/SUPPRESSMSGBOXES', 						'/COMPONENTS=assoc_sh', 						'/DIR=C:\git' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\bin;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  git --version'; git --version; 	Write-Host '  bash --version'; bash --version; 	Write-Host '  curl --version'; curl.exe --version; 		Write-Host 'Removing installer ...'; 	Remove-Item git.exe -Force; 		Write-Host 'Complete.';
# Wed, 18 Jan 2017 00:26:23 GMT
ENV GOPATH=C:\gopath
# Wed, 18 Jan 2017 00:26:44 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 20 Jan 2017 21:41:40 GMT
ENV GOLANG_VERSION=1.7.4
# Fri, 20 Jan 2017 21:41:47 GMT
ENV GOLANG_DOWNLOAD_URL=https://golang.org/dl/go1.7.4.windows-amd64.zip
# Fri, 20 Jan 2017 21:41:51 GMT
ENV GOLANG_DOWNLOAD_SHA256=36739164fed38a6da908813aba48d72fb22fea923de5611a85a81135b7cfceb9
# Fri, 20 Jan 2017 21:48:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GOLANG_DOWNLOAD_URL); 	Invoke-WebRequest -Uri $env:GOLANG_DOWNLOAD_URL -OutFile 'go.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GOLANG_DOWNLOAD_SHA256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $env:GOLANG_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Complete.';
# Fri, 20 Jan 2017 21:48:14 GMT
WORKDIR C:\gopath
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3430754e4d171ead00cf6766797a28abf3caf236f6c92c5c346ea2ad3955a129`  
		Size: 913.1 MB (913145061 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2090e83c9aacacb2da7d0836cf297e9927a3137c208e2f631e39e181e31ceb90`  
		Last Modified: Wed, 18 Jan 2017 22:56:55 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:897c7807798acd4116c377b5307f0b5d3c4bbc03c235a727c4789e6b35974cba`  
		Last Modified: Fri, 20 Jan 2017 22:01:25 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cc7c7c5b42aa2cf38693b33954d51e48e763705017cd1f4d16b0a311c539863`  
		Last Modified: Fri, 20 Jan 2017 22:01:20 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf30c0d5a2dbb915e9b83bb1865163fe73ff9274f10b59e2901c1e0e045ae17b`  
		Last Modified: Fri, 20 Jan 2017 22:01:20 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7d51259173ad3b6238e2d8d0a5bc8a0a00632206dc98ed8e9760cde0769ac0`  
		Last Modified: Fri, 20 Jan 2017 22:01:15 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad25170cb36a913293bf6047d0997a2f062f2fe4c8505cda896351ab08dc24e6`  
		Last Modified: Fri, 20 Jan 2017 22:08:24 GMT  
		Size: 228.9 MB (228880826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c96a3c292bede7d32494f1d419d749d331e33f84507a8fe4fcc2387ec91c669`  
		Last Modified: Fri, 20 Jan 2017 22:01:15 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1775be9ff04c6b10f539f7c2720bc9f5d0396356cf38f8e95b5017590bcf191e`  
		Last Modified: Fri, 20 Jan 2017 22:01:36 GMT  
		Size: 9.0 MB (8974533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cef27ca5db82072f22d30caa8cf4ddf5355b228be1402d1bf019f3081c5aab3`  
		Last Modified: Fri, 20 Jan 2017 22:09:48 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d26471d4a342228937ffb7e2ed324d30e815d42b1d5920f8d5696956ee8be7a`  
		Last Modified: Fri, 20 Jan 2017 22:09:48 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89b4413cdb3db254bd9d08c195a80dc4815d569a9d8b8342132cb63dd9118af9`  
		Last Modified: Fri, 20 Jan 2017 22:09:48 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:294342d935462e5f63b0de47d38cc867b6eacca5f7d9b2e91db15fe92cb6c3e9`  
		Last Modified: Fri, 20 Jan 2017 22:10:22 GMT  
		Size: 96.1 MB (96095037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d45e5a5f5f115df518164a797b3abee13adb4608dbb005643154b345200d444c`  
		Last Modified: Fri, 20 Jan 2017 22:09:49 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
