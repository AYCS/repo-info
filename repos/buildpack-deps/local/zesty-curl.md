# `buildpack-deps:zesty-curl`

## Docker Metadata

- Image ID: `sha256:40d50d9c8bdc1318762cc46293db16fdab6f9a02a7ad1921ff56b33538faaaf4`
- Created: `2017-01-20T22:52:17.404925643Z`
- Arch: `linux`/`amd64`
- Command: `["/bin/bash"]`
- Environment:
  - `PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`

## `dpkg` (`.deb`-based packages)

### `dpkg` source package: `acl=2.2.52-3`

Binary Packages:

- `libacl1:amd64=2.2.52-3`

Licenses: (parsed from: `/usr/share/doc/libacl1/copyright`)

- `GPL`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris acl=2.2.52-3
'http://archive.ubuntu.com/ubuntu/pool/main/a/acl/acl_2.2.52-3.dsc' acl_2.2.52-3.dsc 2025 SHA256:82e344b9ab176559a85630b74ee5a68d678d7f24b6fe8139f2fd9fcf38a48095
'http://archive.ubuntu.com/ubuntu/pool/main/a/acl/acl_2.2.52.orig.tar.bz2' acl_2.2.52.orig.tar.bz2 312128 SHA256:59d05b38af76baf2eddccbf08c7968a17451cc785ffecc657fcb46ce32b2631d
'http://archive.ubuntu.com/ubuntu/pool/main/a/acl/acl_2.2.52-3.debian.tar.xz' acl_2.2.52-3.debian.tar.xz 8740 SHA256:fc3f1178d18288993fc4ce4853b7f9dcdf0bd1fd26e4f69349a4e4e5916d1fa8
```

### `dpkg` source package: `adduser=3.113+nmu3ubuntu5`

Binary Packages:

- `adduser=3.113+nmu3ubuntu5`

Licenses: (parsed from: `/usr/share/doc/adduser/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris adduser=3.113+nmu3ubuntu5
'http://archive.ubuntu.com/ubuntu/pool/main/a/adduser/adduser_3.113+nmu3ubuntu5.dsc' adduser_3.113+nmu3ubuntu5.dsc 1856 SHA256:8ee45bcc264fbeaf8bf0ac56c7f79d60f4aed922acd622c5497809e66961d6a5
'http://archive.ubuntu.com/ubuntu/pool/main/a/adduser/adduser_3.113+nmu3ubuntu5.tar.gz' adduser_3.113+nmu3ubuntu5.tar.gz 362722 SHA256:03221563714d853cda454deabbd6eb87c41fbc87509e929828f8b670560f129f
```

### `dpkg` source package: `apt=1.4~beta4`

Binary Packages:

- `apt=1.4~beta4`
- `libapt-pkg5.0:amd64=1.4~beta4`

Licenses: (parsed from: `/usr/share/doc/apt/copyright`, `/usr/share/doc/libapt-pkg5.0/copyright`)

- `GPL-2`
- `GPLv2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!


### `dpkg` source package: `attr=1:2.4.47-2`

Binary Packages:

- `libattr1:amd64=1:2.4.47-2`

Licenses: (parsed from: `/usr/share/doc/libattr1/copyright`)

- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris attr=1:2.4.47-2
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.4.47-2.dsc' attr_2.4.47-2.dsc 2027 SHA256:ee842d6d62d473acf02b494c432cf33128fa46455a09d3172c77c252449fa1a6
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.4.47.orig.tar.bz2' attr_2.4.47.orig.tar.bz2 281877 SHA256:6c1208035757f5ce9b516402dd45b8299a53ae4d69ad2c352116f9cb8d7bc274
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.4.47-2.debian.tar.xz' attr_2.4.47-2.debian.tar.xz 8096 SHA256:f65909562def601b1556393f5656032c058dc574ba622414ad3eb80c7b05a42a
```

### `dpkg` source package: `audit=1:2.6.6-1ubuntu1`

Binary Packages:

- `libaudit-common=1:2.6.6-1ubuntu1`
- `libaudit1:amd64=1:2.6.6-1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libaudit-common/copyright`, `/usr/share/doc/libaudit1/copyright`)

- `GPL-1`
- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris audit=1:2.6.6-1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/a/audit/audit_2.6.6-1ubuntu1.dsc' audit_2.6.6-1ubuntu1.dsc 2748 SHA256:9b080441478f3ec833d2d2650cbc52c94e9ee4d1b0ce8e3b193d6e8062bffd29
'http://archive.ubuntu.com/ubuntu/pool/main/a/audit/audit_2.6.6.orig.tar.gz' audit_2.6.6.orig.tar.gz 1080510 SHA256:61d8dc61e882fdbb75153a1316817a8f8c8fca25de588256edd81fbb03e7994b
'http://archive.ubuntu.com/ubuntu/pool/main/a/audit/audit_2.6.6-1ubuntu1.debian.tar.xz' audit_2.6.6-1ubuntu1.debian.tar.xz 19856 SHA256:242f5d01e042dbe0e178d0f0c6fd0ad07f008898962b0f28e8c9e74f91c11e27
```

### `dpkg` source package: `base-files=9.6ubuntu9`

Binary Packages:

- `base-files=9.6ubuntu9`

Licenses: (parsed from: `/usr/share/doc/base-files/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris base-files=9.6ubuntu9
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-files/base-files_9.6ubuntu9.dsc' base-files_9.6ubuntu9.dsc 1582 SHA256:5377ebcc00f47bffc3f863b3de97544f7e6fccc8bfa66e85a814b42cc01a5cbe
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-files/base-files_9.6ubuntu9.tar.xz' base-files_9.6ubuntu9.tar.xz 64000 SHA256:6e7003fd963bab9fc8c846772737ac7a5ea8ebb861c155a4cc2e8bfa3467c19a
```

### `dpkg` source package: `base-passwd=3.5.43`

Binary Packages:

- `base-passwd=3.5.43`

Licenses: (parsed from: `/usr/share/doc/base-passwd/copyright`)

- `GPL-2`
- `PD`

Source:

```console
$ apt-get source -qq --print-uris base-passwd=3.5.43
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-passwd/base-passwd_3.5.43.dsc' base-passwd_3.5.43.dsc 1749 SHA256:174a03d0df0d0f36cc186592e36472339632de094d60f9fcab370e1101a2430d
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-passwd/base-passwd_3.5.43.tar.xz' base-passwd_3.5.43.tar.xz 52596 SHA256:7768d10e2c08469cc81342e391e059f0426afdb6eb74a3102beef59ac45ab994
```

### `dpkg` source package: `bash=4.4-2ubuntu1`

Binary Packages:

- `bash=4.4-2ubuntu1`

Licenses: (parsed from: `/usr/share/doc/bash/copyright`)

- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris bash=4.4-2ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/b/bash/bash_4.4-2ubuntu1.dsc' bash_4.4-2ubuntu1.dsc 2303 SHA256:a71ca5e94876b17196625d77f567a5e41634ab4bc5a09ccb65c7a96e96db9bb7
'http://archive.ubuntu.com/ubuntu/pool/main/b/bash/bash_4.4.orig.tar.xz' bash_4.4.orig.tar.xz 4878580 SHA256:819ebb6a23799e9e4ca56ac579778c46902005bd5ade4f131ed293d9f77108e7
'http://archive.ubuntu.com/ubuntu/pool/main/b/bash/bash_4.4-2ubuntu1.debian.tar.xz' bash_4.4-2ubuntu1.debian.tar.xz 66768 SHA256:731a16116d88e010e4379908e0d95d07a8a80c55ae567f70c564c12e498efea8
```

### `dpkg` source package: `bzip2=1.0.6-8build1`

Binary Packages:

- `libbz2-1.0:amd64=1.0.6-8build1`

Licenses: (parsed from: `/usr/share/doc/libbz2-1.0/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris bzip2=1.0.6-8build1
'http://archive.ubuntu.com/ubuntu/pool/main/b/bzip2/bzip2_1.0.6-8build1.dsc' bzip2_1.0.6-8build1.dsc 2084 SHA256:f92a0b270232bc31b233b8208dc50f7ea9168f6c68ee147966131a1803a678f3
'http://archive.ubuntu.com/ubuntu/pool/main/b/bzip2/bzip2_1.0.6.orig.tar.bz2' bzip2_1.0.6.orig.tar.bz2 708737 SHA256:d70a9ccd8bdf47e302d96c69fecd54925f45d9c7b966bb4ef5f56b770960afa7
'http://archive.ubuntu.com/ubuntu/pool/main/b/bzip2/bzip2_1.0.6-8build1.debian.tar.bz2' bzip2_1.0.6-8build1.debian.tar.bz2 59601 SHA256:5644d650048c817bb50073bb5628d27d9c0ea424a07328967cd3f88b9103ec30
```

### `dpkg` source package: `ca-certificates=20160104ubuntu1`

Binary Packages:

- `ca-certificates=20160104ubuntu1`

Licenses: (parsed from: `/usr/share/doc/ca-certificates/copyright`)

- `GPL-2`
- `GPL-2+`
- `MPL-2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!


### `dpkg` source package: `cdebconf=0.213ubuntu1`

Binary Packages:

- `libdebconfclient0:amd64=0.213ubuntu1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)
  If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris cdebconf=0.213ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/c/cdebconf/cdebconf_0.213ubuntu1.dsc' cdebconf_0.213ubuntu1.dsc 2769 SHA256:76cb3f0b1685629220b0e4c3105757b95714f7350df4e7863d5310f1f581fee0
'http://archive.ubuntu.com/ubuntu/pool/main/c/cdebconf/cdebconf_0.213ubuntu1.tar.xz' cdebconf_0.213ubuntu1.tar.xz 272596 SHA256:624feaf9e7e5f407271f99e06e54d5002fcce51345553a626caf7b4a65f0afd1
```

### `dpkg` source package: `coreutils=8.25-2ubuntu2`

Binary Packages:

- `coreutils=8.25-2ubuntu2`

Licenses: (parsed from: `/usr/share/doc/coreutils/copyright`)

- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris coreutils=8.25-2ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/c/coreutils/coreutils_8.25-2ubuntu2.dsc' coreutils_8.25-2ubuntu2.dsc 2071 SHA256:8f2d6456701648072a4ed22142bcb8c0113d4488dd28acd1fc46e26952bbef91
'http://archive.ubuntu.com/ubuntu/pool/main/c/coreutils/coreutils_8.25.orig.tar.xz' coreutils_8.25.orig.tar.xz 5725008 SHA256:31e67c057a5b32a582f26408c789e11c2e8d676593324849dcf5779296cdce87
'http://archive.ubuntu.com/ubuntu/pool/main/c/coreutils/coreutils_8.25-2ubuntu2.debian.tar.xz' coreutils_8.25-2ubuntu2.debian.tar.xz 28040 SHA256:221f38aeb8e251c21edcdb93706deb61ac7619264c1e403609f67e13431e69bb
```

### `dpkg` source package: `curl=7.51.0-1ubuntu1`

Binary Packages:

- `curl=7.51.0-1ubuntu1`
- `libcurl3-gnutls:amd64=7.51.0-1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/curl/copyright`, `/usr/share/doc/libcurl3-gnutls/copyright`)

- `BSD-3-Clause`
- `BSD-4-Clause`
- `ISC`
- `curl`
- `other`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris curl=7.51.0-1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/c/curl/curl_7.51.0-1ubuntu1.dsc' curl_7.51.0-1ubuntu1.dsc 2775 SHA256:d6fbcff05e94e30944fa359ed9c4349b6d55257004680acda61f791357155388
'http://archive.ubuntu.com/ubuntu/pool/main/c/curl/curl_7.51.0.orig.tar.gz' curl_7.51.0.orig.tar.gz 3441753 SHA256:65b5216a6fbfa72f547eb7706ca5902d7400db9868269017a8888aa91d87977c
'http://archive.ubuntu.com/ubuntu/pool/main/c/curl/curl_7.51.0-1ubuntu1.debian.tar.xz' curl_7.51.0-1ubuntu1.debian.tar.xz 30180 SHA256:284cf62266b22abc4e262e095182188c84f730d94264ae3e7e51444a4a392f71
```

### `dpkg` source package: `cyrus-sasl2=2.1.27~72-g88d82a3+dfsg-1`

Binary Packages:

- `libsasl2-2:amd64=2.1.27~72-g88d82a3+dfsg-1`
- `libsasl2-modules-db:amd64=2.1.27~72-g88d82a3+dfsg-1`

Licenses: (parsed from: `/usr/share/doc/libsasl2-2/copyright`, `/usr/share/doc/libsasl2-modules-db/copyright`)

- `BSD-4-clause`
- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris cyrus-sasl2=2.1.27~72-g88d82a3+dfsg-1
'http://archive.ubuntu.com/ubuntu/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.27~72-g88d82a3+dfsg-1.dsc' cyrus-sasl2_2.1.27~72-g88d82a3+dfsg-1.dsc 3264 SHA256:9294e641367563534348e136100305a3eeefe74f597bd27cb5252c62059a81bf
'http://archive.ubuntu.com/ubuntu/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.27~72-g88d82a3+dfsg.orig.tar.xz' cyrus-sasl2_2.1.27~72-g88d82a3+dfsg.orig.tar.xz 687336 SHA256:ca36be5b3d4540ba902ee75f46c6a796fa4fc10590c75a4abaf65593a09e7bf0
'http://archive.ubuntu.com/ubuntu/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.27~72-g88d82a3+dfsg-1.debian.tar.xz' cyrus-sasl2_2.1.27~72-g88d82a3+dfsg-1.debian.tar.xz 94076 SHA256:a17ba54371a0838ca38e38afa367ed077024b9191471fdb6841d9f1d14f82086
```

### `dpkg` source package: `dash=0.5.8-2.3ubuntu1`

Binary Packages:

- `dash=0.5.8-2.3ubuntu1`

Licenses: (parsed from: `/usr/share/doc/dash/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris dash=0.5.8-2.3ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/d/dash/dash_0.5.8-2.3ubuntu1.dsc' dash_0.5.8-2.3ubuntu1.dsc 1882 SHA256:97c31601cd0cd910dbe95127c3abd6e43b09c9bffbaba18165166929a0545f82
'http://archive.ubuntu.com/ubuntu/pool/main/d/dash/dash_0.5.8.orig.tar.gz' dash_0.5.8.orig.tar.gz 223028 SHA256:c6db3a237747b02d20382a761397563d813b306c020ae28ce25a1c3915fac60f
'http://archive.ubuntu.com/ubuntu/pool/main/d/dash/dash_0.5.8-2.3ubuntu1.diff.gz' dash_0.5.8-2.3ubuntu1.diff.gz 73758 SHA256:9c09d7737ff18f084335ffcd9e8c2a106a2c8ad512d4a9967f2912be1dfa2aee
```

### `dpkg` source package: `db5.3=5.3.28-12`

Binary Packages:

- `libdb5.3:amd64=5.3.28-12`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)
  If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris db5.3=5.3.28-12
'http://archive.ubuntu.com/ubuntu/pool/main/d/db5.3/db5.3_5.3.28-12.dsc' db5.3_5.3.28-12.dsc 3199 SHA256:1c4d6149f83a798e69f6d8e7444711d963c31d649284357135ea33b319c71bba
'http://archive.ubuntu.com/ubuntu/pool/main/d/db5.3/db5.3_5.3.28.orig.tar.xz' db5.3_5.3.28.orig.tar.xz 24154920 SHA256:e1f85c8b6ebd0ed3ca72fa0ae97b65006f6d0bd0cd6f4ac24bed103cb5497bf5
'http://archive.ubuntu.com/ubuntu/pool/main/d/db5.3/db5.3_5.3.28-12.debian.tar.xz' db5.3_5.3.28-12.debian.tar.xz 27812 SHA256:7907d8ad4c408857a71782436283a7ab67d7fe0f38ae15782f08077bdfd55c03
```

### `dpkg` source package: `debconf=1.5.59ubuntu1`

Binary Packages:

- `debconf=1.5.59ubuntu1`

Licenses: (parsed from: `/usr/share/doc/debconf/copyright`)

- `BSD-2-clause`

Source:

```console
$ apt-get source -qq --print-uris debconf=1.5.59ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/d/debconf/debconf_1.5.59ubuntu1.dsc' debconf_1.5.59ubuntu1.dsc 2002 SHA256:38e2a4c8567eb9b6d1e499b61ff474b1f484709e4060a4808552406a0a86b19c
'http://archive.ubuntu.com/ubuntu/pool/main/d/debconf/debconf_1.5.59ubuntu1.tar.xz' debconf_1.5.59ubuntu1.tar.xz 574620 SHA256:000d80d932b871eca0534fa0d7463da5f0c99f1a9e0dc4f07c1d44f045d3e618
```

### `dpkg` source package: `debianutils=4.8.1`

Binary Packages:

- `debianutils=4.8.1`

Licenses: (parsed from: `/usr/share/doc/debianutils/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris debianutils=4.8.1
'http://archive.ubuntu.com/ubuntu/pool/main/d/debianutils/debianutils_4.8.1.dsc' debianutils_4.8.1.dsc 1693 SHA256:0f187e087a9c96a70e672f58fa324d4b65f60f1e13ee8219de7e58f061ae7c9e
'http://archive.ubuntu.com/ubuntu/pool/main/d/debianutils/debianutils_4.8.1.tar.xz' debianutils_4.8.1.tar.xz 156072 SHA256:2c395c0bdcfe89de30828b1d25cc5549ded5225a6d3625fbcb2cc0881ef5f026
```

### `dpkg` source package: `diffutils=1:3.5-3`

Binary Packages:

- `diffutils=1:3.5-3`

Licenses: (parsed from: `/usr/share/doc/diffutils/copyright`)

- `GFDL`
- `GPL`

Source:

```console
$ apt-get source -qq --print-uris diffutils=1:3.5-3
'http://archive.ubuntu.com/ubuntu/pool/main/d/diffutils/diffutils_3.5-3.dsc' diffutils_3.5-3.dsc 1453 SHA256:8b8e4d9d48ab35fd2c5759a3d0854e7d85c33b3fa09a185c20865793090feff9
'http://archive.ubuntu.com/ubuntu/pool/main/d/diffutils/diffutils_3.5.orig.tar.xz' diffutils_3.5.orig.tar.xz 1360996 SHA256:dad398ccd5b9faca6b0ab219a036453f62a602a56203ac659b43e889bec35533
'http://archive.ubuntu.com/ubuntu/pool/main/d/diffutils/diffutils_3.5-3.debian.tar.xz' diffutils_3.5-3.debian.tar.xz 10796 SHA256:5c8464482951de1dcf3c1c53643cd7d0939cd8f7568a7ef84982d368c5cb6695
```

### `dpkg` source package: `dpkg=1.18.10ubuntu1`

Binary Packages:

- `dpkg=1.18.10ubuntu1`

Licenses: (parsed from: `/usr/share/doc/dpkg/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`
- `public-domain-md5`
- `public-domain-s-s-d`

Source:

```console
$ apt-get source -qq --print-uris dpkg=1.18.10ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/d/dpkg/dpkg_1.18.10ubuntu1.dsc' dpkg_1.18.10ubuntu1.dsc 2137 SHA256:ef17d9b5009c9f85595ce153592b8aa37f5400459a25144d3325df618b3f6c9e
'http://archive.ubuntu.com/ubuntu/pool/main/d/dpkg/dpkg_1.18.10ubuntu1.tar.xz' dpkg_1.18.10ubuntu1.tar.xz 4589592 SHA256:f10472271ec9cadf37588bdbcee090ed292408b58595cab91ca37368c622d73c
```

### `dpkg` source package: `e2fsprogs=1.43.3-1`

Binary Packages:

- `e2fslibs:amd64=1.43.3-1`
- `e2fsprogs=1.43.3-1`
- `libcomerr2:amd64=1.43.3-1`
- `libss2:amd64=1.43.3-1`

Licenses: (parsed from: `/usr/share/doc/e2fslibs/copyright`, `/usr/share/doc/e2fsprogs/copyright`, `/usr/share/doc/libcomerr2/copyright`, `/usr/share/doc/libss2/copyright`)

- `GPL-2`
- `LGPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!


### `dpkg` source package: `findutils=4.6.0+git+20161106-1`

Binary Packages:

- `findutils=4.6.0+git+20161106-1`

Licenses: (parsed from: `/usr/share/doc/findutils/copyright`)

- `GFDL-1.3`
- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris findutils=4.6.0+git+20161106-1
'http://archive.ubuntu.com/ubuntu/pool/main/f/findutils/findutils_4.6.0+git+20161106-1.dsc' findutils_4.6.0+git+20161106-1.dsc 2188 SHA256:af0f002e72ae1aa83f3325321513c56f9260ba94b06e0954e5c0d0e3c0210a43
'http://archive.ubuntu.com/ubuntu/pool/main/f/findutils/findutils_4.6.0+git+20161106.orig.tar.xz' findutils_4.6.0+git+20161106.orig.tar.xz 1828956 SHA256:96a3aa120d7300863f39fe56ccb6674d8cde4730b485f4f81083c1a6d33097e3
'http://archive.ubuntu.com/ubuntu/pool/main/f/findutils/findutils_4.6.0+git+20161106-1.debian.tar.xz' findutils_4.6.0+git+20161106-1.debian.tar.xz 26052 SHA256:6d387541054a47185216adfeced73748f4b1b45c16fae18da5471bf67a33609d
```

### `dpkg` source package: `gcc-6=6.3.0-2ubuntu1`

Binary Packages:

- `gcc-6-base:amd64=6.3.0-2ubuntu1`
- `libgcc1:amd64=1:6.3.0-2ubuntu1`
- `libstdc++6:amd64=6.3.0-2ubuntu1`

Licenses: (parsed from: `/usr/share/doc/gcc-6-base/copyright`, `/usr/share/doc/libgcc1/copyright`, `/usr/share/doc/libstdc++6/copyright`)

- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-2`
- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris gcc-6=6.3.0-2ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-6/gcc-6_6.3.0-2ubuntu1.dsc' gcc-6_6.3.0-2ubuntu1.dsc 31021 SHA256:85f867ae92e2f9efe1282fa37eb2b1fc632301c7ce4a65094bd7f61da245bcd0
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-6/gcc-6_6.3.0.orig.tar.gz' gcc-6_6.3.0.orig.tar.gz 77161407 SHA256:067c2840b1a52ebab9232fa3c70f1422ff3f7b1be98ffb335807c9817491817e
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-6/gcc-6_6.3.0-2ubuntu1.diff.gz' gcc-6_6.3.0-2ubuntu1.diff.gz 1513948 SHA256:476eb1bb6272196123700320462339b2231ccd3a61d7641166d000cf0ae9972b
```

### `dpkg` source package: `glibc=2.24-3ubuntu1`

Binary Packages:

- `libc-bin=2.24-3ubuntu1`
- `libc6:amd64=2.24-3ubuntu1`
- `locales=2.24-3ubuntu1`
- `multiarch-support=2.24-3ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libc-bin/copyright`, `/usr/share/doc/libc6/copyright`, `/usr/share/doc/locales/copyright`, `/usr/share/doc/multiarch-support/copyright`)

- `GPL-2`
- `LGPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!


### `dpkg` source package: `gmp=2:6.1.1+dfsg-1`

Binary Packages:

- `libgmp10:amd64=2:6.1.1+dfsg-1`

Licenses: (parsed from: `/usr/share/doc/libgmp10/copyright`)

- `GPL`
- `GPL-2`
- `GPL-3`
- `LGPL-3`

Source:

```console
$ apt-get source -qq --print-uris gmp=2:6.1.1+dfsg-1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gmp/gmp_6.1.1+dfsg-1.dsc' gmp_6.1.1+dfsg-1.dsc 2161 SHA256:3f501a907c0357de8e9dd5325471c409ec493ab2007cfe4e761e52fd3646fec9
'http://archive.ubuntu.com/ubuntu/pool/main/g/gmp/gmp_6.1.1+dfsg.orig.tar.xz' gmp_6.1.1+dfsg.orig.tar.xz 1802176 SHA256:1c34c3c0c89c4f1270f6e3e579e7b7f9190eca6713311f0167bb9fee5b3750ee
'http://archive.ubuntu.com/ubuntu/pool/main/g/gmp/gmp_6.1.1+dfsg-1.debian.tar.xz' gmp_6.1.1+dfsg-1.debian.tar.xz 20600 SHA256:270a0ee22dc3da83356bf32c22d5657580c26daf931d82fa3b06ea2abdffd4ed
```

### `dpkg` source package: `gnupg2=2.1.15-1ubuntu6`

Binary Packages:

- `gnupg=2.1.15-1ubuntu6`
- `gnupg-agent=2.1.15-1ubuntu6`
- `gpgv=2.1.15-1ubuntu6`

Licenses: (parsed from: `/usr/share/doc/gnupg/copyright`, `/usr/share/doc/gnupg-agent/copyright`, `/usr/share/doc/gpgv/copyright`)

- `BSD-3-clause`
- `GPL-3`
- `GPL-3+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`
- `RFC-Reference`
- `TinySCHEME`
- `permissive`

Source:

```console
$ apt-get source -qq --print-uris gnupg2=2.1.15-1ubuntu6
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.1.15-1ubuntu6.dsc' gnupg2_2.1.15-1ubuntu6.dsc 2815 SHA256:fca1d0e148edb8bdda38972c584947490e7638067397232918ae67ceabf36fe8
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.1.15.orig.tar.bz2' gnupg2_2.1.15.orig.tar.bz2 5723689 SHA256:c28c1a208f1b8ad63bdb6b88d252f6734ff4d33de6b54e38494b11d49e00ffdd
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.1.15-1ubuntu6.debian.tar.bz2' gnupg2_2.1.15-1ubuntu6.debian.tar.bz2 42239 SHA256:c63b7b237087d1ee5899897d29536d0a211549b66e49245bb30531136d57dba6
```

### `dpkg` source package: `gnutls28=3.5.6-4ubuntu2`

Binary Packages:

- `libgnutls30:amd64=3.5.6-4ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libgnutls30/copyright`)

- `CC0 license`
- `GFDL-1.3`
- `GPL`
- `GPL-3`
- `LGPL`
- `LGPL-3`
- `LGPL2.1`
- `The MIT License (MIT)`
- `The main library is licensed under GNU Lesser`

Source:

```console
$ apt-get source -qq --print-uris gnutls28=3.5.6-4ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.5.6-4ubuntu2.dsc' gnutls28_3.5.6-4ubuntu2.dsc 3245 SHA256:0472148d655649eced387b10f4f8a14b6d8454be6eef212c249b039d6da78c25
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.5.6.orig.tar.xz' gnutls28_3.5.6.orig.tar.xz 7087388 SHA256:6338b715bf31c758606ffa489c7f87ee1beab947114fbd2ffefd73170a8c6b9a
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.5.6.orig.tar.xz.asc' gnutls28_3.5.6.orig.tar.xz.asc 287 SHA256:64a5adbe0671d31f5c59b1244f4febb7b86b30e5669c64c6818d50538ab6d983
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.5.6-4ubuntu2.debian.tar.xz' gnutls28_3.5.6-4ubuntu2.debian.tar.xz 116032 SHA256:eef546632734a250fcc02466bf4d180678a3a97a4cade47c26a096d3c6c2ffa7
```

### `dpkg` source package: `grep=2.27-1`

Binary Packages:

- `grep=2.27-1`

Licenses: (parsed from: `/usr/share/doc/grep/copyright`)

- `GPL-3`
- `GPL-3+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!


### `dpkg` source package: `gzip=1.6-4ubuntu1`

Binary Packages:

- `gzip=1.6-4ubuntu1`

Licenses: (parsed from: `/usr/share/doc/gzip/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris gzip=1.6-4ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gzip/gzip_1.6-4ubuntu1.dsc' gzip_1.6-4ubuntu1.dsc 1907 SHA256:77c1d15c52947d50656365597802c586249d26a4f56c8075f5d94b4634d11465
'http://archive.ubuntu.com/ubuntu/pool/main/g/gzip/gzip_1.6.orig.tar.gz' gzip_1.6.orig.tar.gz 1074924 SHA256:97eb83b763d9e5ad35f351fe5517e6b71521d7aac7acf3e3cacdb6b1496d8f7e
'http://archive.ubuntu.com/ubuntu/pool/main/g/gzip/gzip_1.6-4ubuntu1.debian.tar.xz' gzip_1.6-4ubuntu1.debian.tar.xz 14932 SHA256:9a3e558c87a78bf65f9b9c48d718b3ef0bb69e0cf07617f44e37f41ba5f7b006
```

### `dpkg` source package: `heimdal=1.7~git20160703+dfsg-1ubuntu1`

Binary Packages:

- `libasn1-8-heimdal:amd64=1.7~git20160703+dfsg-1ubuntu1`
- `libgssapi3-heimdal:amd64=1.7~git20160703+dfsg-1ubuntu1`
- `libhcrypto4-heimdal:amd64=1.7~git20160703+dfsg-1ubuntu1`
- `libheimbase1-heimdal:amd64=1.7~git20160703+dfsg-1ubuntu1`
- `libheimntlm0-heimdal:amd64=1.7~git20160703+dfsg-1ubuntu1`
- `libhx509-5-heimdal:amd64=1.7~git20160703+dfsg-1ubuntu1`
- `libkrb5-26-heimdal:amd64=1.7~git20160703+dfsg-1ubuntu1`
- `libroken18-heimdal:amd64=1.7~git20160703+dfsg-1ubuntu1`
- `libwind0-heimdal:amd64=1.7~git20160703+dfsg-1ubuntu1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)
  If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris heimdal=1.7~git20160703+dfsg-1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/h/heimdal/heimdal_1.7~git20160703+dfsg-1ubuntu1.dsc' heimdal_1.7~git20160703+dfsg-1ubuntu1.dsc 3332 SHA256:cd662c9b6dd768e55b5344dd6af3e8d5446056b8ca4eb0d94ebcf8bb24bb9d14
'http://archive.ubuntu.com/ubuntu/pool/main/h/heimdal/heimdal_1.7~git20160703+dfsg.orig.tar.gz' heimdal_1.7~git20160703+dfsg.orig.tar.gz 9203662 SHA256:3e68467631944751c4d32d9af615c2b5745ebc43b19c4a76ac28520dc4e999f5
'http://archive.ubuntu.com/ubuntu/pool/main/h/heimdal/heimdal_1.7~git20160703+dfsg-1ubuntu1.debian.tar.xz' heimdal_1.7~git20160703+dfsg-1ubuntu1.debian.tar.xz 65788 SHA256:28324a097f558b34d34750eec3508a2c54b6ca36b0f104ba8745a8332b2e8b4b
```

### `dpkg` source package: `hostname=3.18`

Binary Packages:

- `hostname=3.18`

Licenses: (parsed from: `/usr/share/doc/hostname/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris hostname=3.18
'http://archive.ubuntu.com/ubuntu/pool/main/h/hostname/hostname_3.18.dsc' hostname_3.18.dsc 1446 SHA256:4d3d5c8ded08ffc2ebfb39817ba1994b5fc1966652b132ff3e16389b70af28d7
'http://archive.ubuntu.com/ubuntu/pool/main/h/hostname/hostname_3.18.tar.gz' hostname_3.18.tar.gz 13732 SHA256:5cc3ec120967b8f911e86b9561b53977bcc77191c84fe9c607177ccd09f8d207
```

### `dpkg` source package: `init-system-helpers=1.46`

Binary Packages:

- `init-system-helpers=1.46`

Licenses: (parsed from: `/usr/share/doc/init-system-helpers/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris init-system-helpers=1.46
'http://archive.ubuntu.com/ubuntu/pool/main/i/init-system-helpers/init-system-helpers_1.46.dsc' init-system-helpers_1.46.dsc 1912 SHA256:93c5998f5da7923ee30c8f706bac2c79d7bf831ff47386789f244fce93ffc96e
'http://archive.ubuntu.com/ubuntu/pool/main/i/init-system-helpers/init-system-helpers_1.46.tar.xz' init-system-helpers_1.46.tar.xz 42952 SHA256:f45c9736e1047089f60c316ab8ab978ea75b2903e0f3cf74407711ae77e8871d
```

### `dpkg` source package: `keyutils=1.5.9-9ubuntu1`

Binary Packages:

- `libkeyutils1:amd64=1.5.9-9ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libkeyutils1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2`
- `LGPL-2+`

Source:

```console
$ apt-get source -qq --print-uris keyutils=1.5.9-9ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/k/keyutils/keyutils_1.5.9-9ubuntu1.dsc' keyutils_1.5.9-9ubuntu1.dsc 2178 SHA256:3b023a7933535abae794c250be7dcd1bf39d9afaae5633e66fb394f3f048200c
'http://archive.ubuntu.com/ubuntu/pool/main/k/keyutils/keyutils_1.5.9.orig.tar.bz2' keyutils_1.5.9.orig.tar.bz2 74683 SHA256:4da2c5552c688b65ab14d4fd40fbdf720c8b396d8ece643e040cf6e707e083ae
'http://archive.ubuntu.com/ubuntu/pool/main/k/keyutils/keyutils_1.5.9-9ubuntu1.debian.tar.xz' keyutils_1.5.9-9ubuntu1.debian.tar.xz 17812 SHA256:7dc31901696b2afa98f1984c464e93f9c9a562158ba79ed7a84890109b319f42
```

### `dpkg` source package: `krb5=1.15~beta1-1`

Binary Packages:

- `libgssapi-krb5-2:amd64=1.15~beta1-1`
- `libk5crypto3:amd64=1.15~beta1-1`
- `libkrb5-3:amd64=1.15~beta1-1`
- `libkrb5support0:amd64=1.15~beta1-1`

Licenses: (parsed from: `/usr/share/doc/libgssapi-krb5-2/copyright`, `/usr/share/doc/libk5crypto3/copyright`, `/usr/share/doc/libkrb5-3/copyright`, `/usr/share/doc/libkrb5support0/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris krb5=1.15~beta1-1
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.15~beta1-1.dsc' krb5_1.15~beta1-1.dsc 3261 SHA256:fbded00e724725b7266a484629343d5a5b8aebc6178737ba461f2b9af2d298d2
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.15~beta1.orig.tar.gz' krb5_1.15~beta1.orig.tar.gz 9328801 SHA256:957ff239dc1d327cb4a0e8ec53ff619fef7dd1ecd5cec99004ca440f617974c2
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.15~beta1-1.debian.tar.xz' krb5_1.15~beta1-1.debian.tar.xz 141900 SHA256:2f506202acf5a09a38b3ddd8ebda5628517e13e27b7b9af3ad5ef62f5acb1370
```

### `dpkg` source package: `libassuan=2.4.3-2`

Binary Packages:

- `libassuan0:amd64=2.4.3-2`

Licenses: (parsed from: `/usr/share/doc/libassuan0/copyright`)

- `GAP`
- `GAP~FSF`
- `GPL-2`
- `GPL-2+`
- `GPL-2+ with libtool exception`
- `GPL-3`
- `GPL-3+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`

Source:

```console
$ apt-get source -qq --print-uris libassuan=2.4.3-2
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libassuan/libassuan_2.4.3-2.dsc' libassuan_2.4.3-2.dsc 2412 SHA256:fc057ff6bd548161cd978f7847682928222d31db96bd94d7ec0fc84b176bbcc7
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libassuan/libassuan_2.4.3.orig.tar.bz2' libassuan_2.4.3.orig.tar.bz2 559867 SHA256:22843a3bdb256f59be49842abf24da76700354293a066d82ade8134bb5aa2b71
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libassuan/libassuan_2.4.3-2.debian.tar.xz' libassuan_2.4.3-2.debian.tar.xz 15076 SHA256:16dd66909cf3b79c71d5169f35d94be64d079d882f027577c00c23bff3148012
```

### `dpkg` source package: `libcap-ng=0.7.7-3`

Binary Packages:

- `libcap-ng0:amd64=0.7.7-3`

Licenses: (parsed from: `/usr/share/doc/libcap-ng0/copyright`)

- `GPL-2`
- `GPL-3`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libcap-ng=0.7.7-3
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap-ng/libcap-ng_0.7.7-3.dsc' libcap-ng_0.7.7-3.dsc 1722 SHA256:6f5262f0ed2792c135e9b6bf7d30461cc3015249832f381505d21b9217a67685
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap-ng/libcap-ng_0.7.7.orig.tar.gz' libcap-ng_0.7.7.orig.tar.gz 420178 SHA256:615549ce39b333f6b78baee0c0b4ef18bc726c6bf1cca123dfd89dd963f6d06b
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap-ng/libcap-ng_0.7.7-3.debian.tar.xz' libcap-ng_0.7.7-3.debian.tar.xz 5248 SHA256:b7a0846dbd0451903bcbbe3a2696341f4e6000ebd64bed259c7fbf9dfc818363
```

### `dpkg` source package: `libffi=3.2.1-6`

Binary Packages:

- `libffi6:amd64=3.2.1-6`

Licenses: (parsed from: `/usr/share/doc/libffi6/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris libffi=3.2.1-6
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libffi/libffi_3.2.1-6.dsc' libffi_3.2.1-6.dsc 1923 SHA256:f901298b078c7d7f3f75459b5ff74cc804f6f2cfd65ed619d2082d5f77089954
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libffi/libffi_3.2.1.orig.tar.gz' libffi_3.2.1.orig.tar.gz 940837 SHA256:d06ebb8e1d9a22d19e38d63fdb83954253f39bedc5d46232a05645685722ca37
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libffi/libffi_3.2.1-6.debian.tar.xz' libffi_3.2.1-6.debian.tar.xz 11252 SHA256:477709fa90f8c7631fa226a48cdf38737c9f195f3686f62aa76714bcffaee512
```

### `dpkg` source package: `libgcrypt20=1.7.5-2`

Binary Packages:

- `libgcrypt20:amd64=1.7.5-2`

Licenses: (parsed from: `/usr/share/doc/libgcrypt20/copyright`)

- `GPL-2`
- `LGPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!


### `dpkg` source package: `libgpg-error=1.25-2`

Binary Packages:

- `libgpg-error0:amd64=1.25-2`

Licenses: (parsed from: `/usr/share/doc/libgpg-error0/copyright`)

- `GPL-2.1+`
- `LGPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!


### `dpkg` source package: `libidn=1.33-1`

Binary Packages:

- `libidn11:amd64=1.33-1`

Licenses: (parsed from: `/usr/share/doc/libidn11/copyright`)

- `GAP`
- `GFDL-1.3`
- `GFDL-1.3+`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `LGPL-2`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`

Source:

```console
$ apt-get source -qq --print-uris libidn=1.33-1
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn/libidn_1.33-1.dsc' libidn_1.33-1.dsc 1848 SHA256:f076f7dddc45717542a48123d7dddb638beebe8521f5fba29f2d148fdcf12bf0
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn/libidn_1.33.orig.tar.gz' libidn_1.33.orig.tar.gz 3501056 SHA256:44a7aab635bb721ceef6beecc4d49dfd19478325e1b47f3196f7d2acc4930e19
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn/libidn_1.33-1.debian.tar.xz' libidn_1.33-1.debian.tar.xz 60264 SHA256:a50ee1e2598670ca1166d218e546c4cc031c658188b1193b73d98175d4405ef0
```

### `dpkg` source package: `libksba=1.3.5-2`

Binary Packages:

- `libksba8:amd64=1.3.5-2`

Licenses: (parsed from: `/usr/share/doc/libksba8/copyright`)

- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris libksba=1.3.5-2
'http://archive.ubuntu.com/ubuntu/pool/main/libk/libksba/libksba_1.3.5-2.dsc' libksba_1.3.5-2.dsc 2526 SHA256:4fd08fd129f97ab1df86c220b88b7b2c6e4e04aa90bfd3ae364d18022256bef8
'http://archive.ubuntu.com/ubuntu/pool/main/libk/libksba/libksba_1.3.5.orig.tar.bz2' libksba_1.3.5.orig.tar.bz2 620649 SHA256:41444fd7a6ff73a79ad9728f985e71c9ba8cd3e5e53358e70d5f066d35c1a340
'http://archive.ubuntu.com/ubuntu/pool/main/libk/libksba/libksba_1.3.5.orig.tar.bz2.asc' libksba_1.3.5.orig.tar.bz2.asc 287 SHA256:a954b03144ee882c838853da24fd7b6868b78df72a18c71079217d968698a76f
'http://archive.ubuntu.com/ubuntu/pool/main/libk/libksba/libksba_1.3.5-2.debian.tar.xz' libksba_1.3.5-2.debian.tar.xz 13852 SHA256:98c985bff973be1aecc702fa15887ff1e5b8de481d1dc3e99423a587754eaabd
```

### `dpkg` source package: `libselinux=2.6-3`

Binary Packages:

- `libselinux1:amd64=2.6-3`

Licenses: (parsed from: `/usr/share/doc/libselinux1/copyright`)

- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libselinux=2.6-3
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libselinux/libselinux_2.6-3.dsc' libselinux_2.6-3.dsc 2217 SHA256:91bb53feba8031bfc7b0110fc4e0e1dae4a8e2906f4a524f83252a95ae0e639c
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libselinux/libselinux_2.6.orig.tar.gz' libselinux_2.6.orig.tar.gz 203119 SHA256:4ea2dde50665c202253ba5caac7738370ea0337c47b251ba981c60d24e1a118a
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libselinux/libselinux_2.6-3.debian.tar.xz' libselinux_2.6-3.debian.tar.xz 24396 SHA256:5a06841565e7907bc0dae9f8ed5940d040316192bd9662df59c79af7c212a171
```

### `dpkg` source package: `libsemanage=2.6-2`

Binary Packages:

- `libsemanage-common=2.6-2`
- `libsemanage1:amd64=2.6-2`

Licenses: (parsed from: `/usr/share/doc/libsemanage-common/copyright`, `/usr/share/doc/libsemanage1/copyright`)

- `GPL`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris libsemanage=2.6-2
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsemanage/libsemanage_2.6-2.dsc' libsemanage_2.6-2.dsc 2338 SHA256:2806bf3591dc7eb4c80d647a9e65df13d03657cfa6e049de1035165e0d8484d0
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsemanage/libsemanage_2.6.orig.tar.gz' libsemanage_2.6.orig.tar.gz 155897 SHA256:4f81541047290b751f2ffb926fcd381c186f22db18d9fe671b0b4a6a54e8cfce
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsemanage/libsemanage_2.6-2.debian.tar.xz' libsemanage_2.6-2.debian.tar.xz 17088 SHA256:3d1c4c5ea5d4f27a521b64ba3fc499c8b662257ffec773706501f466032db8cf
```

### `dpkg` source package: `libsepol=2.6-2`

Binary Packages:

- `libsepol1:amd64=2.6-2`

Licenses: (parsed from: `/usr/share/doc/libsepol1/copyright`)

- `GPL`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris libsepol=2.6-2
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsepol/libsepol_2.6-2.dsc' libsepol_2.6-2.dsc 1814 SHA256:197ddaf44a5139d7ca6c12ce6b29fca0589f72c59ac588a7fa39d11b2e65778a
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsepol/libsepol_2.6.orig.tar.gz' libsepol_2.6.orig.tar.gz 442549 SHA256:d856d6506054f52abeaa3543ea2f2344595a3dc05d0d873ed7f724f7a16b1874
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsepol/libsepol_2.6-2.debian.tar.xz' libsepol_2.6-2.debian.tar.xz 14320 SHA256:d7a1022d03eb53a8d30262e06f14f691e553b3db684ca0f3549cd17b93fb7465
```

### `dpkg` source package: `libtasn1-6=4.10-1`

Binary Packages:

- `libtasn1-6:amd64=4.10-1`

Licenses: (parsed from: `/usr/share/doc/libtasn1-6/copyright`)

- `GFDL-1.3`
- `GPL-3`
- `LGPL`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libtasn1-6=4.10-1
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.10-1.dsc' libtasn1-6_4.10-1.dsc 2673 SHA256:0d77069919fc8d3341f5ea95b666cd411b396c8690c0a215cd1957bbe3c79701
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.10.orig.tar.gz' libtasn1-6_4.10.orig.tar.gz 1887057 SHA256:681a4d9a0d259f2125713f2e5766c5809f151b3a1392fd91390f780b4b8f5a02
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.10.orig.tar.gz.asc' libtasn1-6_4.10.orig.tar.gz.asc 455 SHA256:bdf4ba66cfc97a2b712c6ad9a4c0940519fbe2b18fa5b4b003a6343d28a120fe
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.10-1.debian.tar.xz' libtasn1-6_4.10-1.debian.tar.xz 57832 SHA256:fc8e178ae59e0d3bcb4841a484d0bebb3d253ec9c928b4a2a99b4cb157b78dc8
```

### `dpkg` source package: `lsb=9.20160110ubuntu5`

Binary Packages:

- `lsb-base=9.20160110ubuntu5`

Licenses: (parsed from: `/usr/share/doc/lsb-base/copyright`)

- `BSD-3-clause`
- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris lsb=9.20160110ubuntu5
'http://archive.ubuntu.com/ubuntu/pool/main/l/lsb/lsb_9.20160110ubuntu5.dsc' lsb_9.20160110ubuntu5.dsc 2152 SHA256:eb7501d14d4aefb878b1a924d8f94b405f08084d43210d3c188e7dc586bf5efa
'http://archive.ubuntu.com/ubuntu/pool/main/l/lsb/lsb_9.20160110ubuntu5.tar.xz' lsb_9.20160110ubuntu5.tar.xz 58608 SHA256:e33aa59a709a1d278cf503f151ef46a39477e93a4519f4c90e01a1095444a724
```

### `dpkg` source package: `lz4=0.0~r131-2ubuntu2`

Binary Packages:

- `liblz4-1:amd64=0.0~r131-2ubuntu2`

Licenses: (parsed from: `/usr/share/doc/liblz4-1/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris lz4=0.0~r131-2ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/l/lz4/lz4_0.0~r131-2ubuntu2.dsc' lz4_0.0~r131-2ubuntu2.dsc 2007 SHA256:123f23834f83a4dca6d74a611cc0294491bd339d2e0be04d65783d6debbccc02
'http://archive.ubuntu.com/ubuntu/pool/main/l/lz4/lz4_0.0~r131.orig.tar.gz' lz4_0.0~r131.orig.tar.gz 133784 SHA256:9d4d00614d6b9dec3114b33d1224b6262b99ace24434c53487a0c8fd0b18cfed
'http://archive.ubuntu.com/ubuntu/pool/main/l/lz4/lz4_0.0~r131-2ubuntu2.debian.tar.xz' lz4_0.0~r131-2ubuntu2.debian.tar.xz 5224 SHA256:c0afb4a440b1e7b803e2d9dcf616be539c1d16baebc681cdf837000e4c5077b7
```

### `dpkg` source package: `mawk=1.3.3-17ubuntu2`

Binary Packages:

- `mawk=1.3.3-17ubuntu2`

Licenses: (parsed from: `/usr/share/doc/mawk/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris mawk=1.3.3-17ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/m/mawk/mawk_1.3.3-17ubuntu2.dsc' mawk_1.3.3-17ubuntu2.dsc 1843 SHA256:d9058945d45b0e9ee5dd1c9c2e16d8f28b96d5c2e777f743594096fa2a5e277b
'http://archive.ubuntu.com/ubuntu/pool/main/m/mawk/mawk_1.3.3.orig.tar.gz' mawk_1.3.3.orig.tar.gz 209942 SHA256:32649c46063d4ef0777a12ae6e9a26bcc920833d54e1abca7edb8d37481e7485
'http://archive.ubuntu.com/ubuntu/pool/main/m/mawk/mawk_1.3.3-17ubuntu2.diff.gz' mawk_1.3.3-17ubuntu2.diff.gz 63882 SHA256:670103046767474be29e80f2143dc67e3d0b958972f5942c3df94883f978eded
```

### `dpkg` source package: `ncurses=6.0+20160625-1ubuntu1`

Binary Packages:

- `libncurses5:amd64=6.0+20160625-1ubuntu1`
- `libncursesw5:amd64=6.0+20160625-1ubuntu1`
- `libtinfo5:amd64=6.0+20160625-1ubuntu1`
- `ncurses-base=6.0+20160625-1ubuntu1`
- `ncurses-bin=6.0+20160625-1ubuntu1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)
  If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris ncurses=6.0+20160625-1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.0+20160625-1ubuntu1.dsc' ncurses_6.0+20160625-1ubuntu1.dsc 4448 SHA256:8d60a8e3edaf5911d654e9bbc435647571cb398beb9030e9addbf093f9701d32
'http://archive.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.0+20160625.orig.tar.gz' ncurses_6.0+20160625.orig.tar.gz 3167182 SHA256:aaccc026de6f2f112dd56085ec7f38923429edc91a010ae1c8e68b5c53c60acd
'http://archive.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.0+20160625-1ubuntu1.debian.tar.xz' ncurses_6.0+20160625-1ubuntu1.debian.tar.xz 54936 SHA256:85bc1d5ff61390da5ebaf7d4674494ccaaa9d3ad0fa93b6b77f45cc75a2ba8ca
```

### `dpkg` source package: `nettle=3.3-1`

Binary Packages:

- `libhogweed4:amd64=3.3-1`
- `libnettle6:amd64=3.3-1`

Licenses: (parsed from: `/usr/share/doc/libhogweed4/copyright`, `/usr/share/doc/libnettle6/copyright`)

- `GAP`
- `GPL`
- `GPL-2`
- `GPL-2+`
- `GPL-2+ with Autoconf exception`
- `LGPL`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1+`
- `other`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris nettle=3.3-1
'http://archive.ubuntu.com/ubuntu/pool/main/n/nettle/nettle_3.3-1.dsc' nettle_3.3-1.dsc 2043 SHA256:3336bc6e8e5b1acad66afa97a05f934e4d758c614fd468d5650b5a38049f1161
'http://archive.ubuntu.com/ubuntu/pool/main/n/nettle/nettle_3.3.orig.tar.gz' nettle_3.3.orig.tar.gz 1887927 SHA256:46942627d5d0ca11720fec18d81fc38f7ef837ea4197c1f630e71ce0d470b11e
'http://archive.ubuntu.com/ubuntu/pool/main/n/nettle/nettle_3.3-1.debian.tar.xz' nettle_3.3-1.debian.tar.xz 19428 SHA256:42fef549318af6cfdf76336eb348501d09454a1d873a84f66440b9a791a0ff1b
```

### `dpkg` source package: `npth=1.3-1`

Binary Packages:

- `libnpth0:amd64=1.3-1`

Licenses: (parsed from: `/usr/share/doc/libnpth0/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-3`
- `LGPL-3+`

Source:

```console
$ apt-get source -qq --print-uris npth=1.3-1
'http://archive.ubuntu.com/ubuntu/pool/main/n/npth/npth_1.3-1.dsc' npth_1.3-1.dsc 1949 SHA256:63e2598a3aebe21ef7969a601906a719e923673e04a4d157b6dde605566079be
'http://archive.ubuntu.com/ubuntu/pool/main/n/npth/npth_1.3.orig.tar.bz2' npth_1.3.orig.tar.bz2 295998 SHA256:bca81940436aed0734eb8d0ff8b179e04cc8c087f5625204419f5f45d736a82a
'http://archive.ubuntu.com/ubuntu/pool/main/n/npth/npth_1.3-1.debian.tar.xz' npth_1.3-1.debian.tar.xz 10324 SHA256:4910e19597aea46841eaffc6df58ecf91d5d059130ecb1442fee9f5f963b229c
```

### `dpkg` source package: `openldap=2.4.42+dfsg-2ubuntu5`

Binary Packages:

- `libldap-2.4-2:amd64=2.4.42+dfsg-2ubuntu5`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)
  If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris openldap=2.4.42+dfsg-2ubuntu5
'http://archive.ubuntu.com/ubuntu/pool/main/o/openldap/openldap_2.4.42+dfsg-2ubuntu5.dsc' openldap_2.4.42+dfsg-2ubuntu5.dsc 3032 SHA256:5be414db7a42180003d0325e5d4b294dae8b91cd8233a9aa2a9a6b5744ab3fcf
'http://archive.ubuntu.com/ubuntu/pool/main/o/openldap/openldap_2.4.42+dfsg.orig.tar.gz' openldap_2.4.42+dfsg.orig.tar.gz 4813173 SHA256:5f56e4e3584f7a4b4c8437a2c985b2f519836946be77ef1aa43a5d20c02ea97b
'http://archive.ubuntu.com/ubuntu/pool/main/o/openldap/openldap_2.4.42+dfsg-2ubuntu5.debian.tar.xz' openldap_2.4.42+dfsg-2ubuntu5.debian.tar.xz 176952 SHA256:9d4a3189519b291327216c3503f7d7e50a5fe1aed842c5a2ecb4629cf787cd8a
```

### `dpkg` source package: `openssl=1.0.2g-1ubuntu10`

Binary Packages:

- `libssl1.0.0:amd64=1.0.2g-1ubuntu10`
- `openssl=1.0.2g-1ubuntu10`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)
  If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris openssl=1.0.2g-1ubuntu10
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssl/openssl_1.0.2g-1ubuntu10.dsc' openssl_1.0.2g-1ubuntu10.dsc 2146 SHA256:fc3ace5e4895e1557c3527977a3c10f2a4d9461e0ad7e4e5abdf8c2fe08e9835
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssl/openssl_1.0.2g.orig.tar.gz' openssl_1.0.2g.orig.tar.gz 5266102 SHA256:b784b1b3907ce39abf4098702dade6365522a253ad1552e267a9a0e89594aa33
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssl/openssl_1.0.2g-1ubuntu10.debian.tar.xz' openssl_1.0.2g-1ubuntu10.debian.tar.xz 106892 SHA256:5809084e5d8a56fd3f29c0a8ca7a69e3e88540e7ed0985920484c1d484c09b8b
```

### `dpkg` source package: `p11-kit=0.23.3-4`

Binary Packages:

- `libp11-kit0:amd64=0.23.3-4`

Licenses: (parsed from: `/usr/share/doc/libp11-kit0/copyright`)

- `BSD-3-Clause`
- `ISC`
- `ISC+IBM`
- `permissive-like-automake-output`
- `same-as-rest-of-p11kit`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!


### `dpkg` source package: `pam=1.1.8-3.2ubuntu2`

Binary Packages:

- `libpam-modules:amd64=1.1.8-3.2ubuntu2`
- `libpam-modules-bin=1.1.8-3.2ubuntu2`
- `libpam-runtime=1.1.8-3.2ubuntu2`
- `libpam0g:amd64=1.1.8-3.2ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libpam-modules/copyright`, `/usr/share/doc/libpam-modules-bin/copyright`, `/usr/share/doc/libpam-runtime/copyright`, `/usr/share/doc/libpam0g/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris pam=1.1.8-3.2ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.1.8-3.2ubuntu2.dsc' pam_1.1.8-3.2ubuntu2.dsc 2589 SHA256:b9ab28d75594ece90f12987b8926d5897fb994f1ea25a2ee03b09e2570785142
'http://archive.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.1.8.orig.tar.gz' pam_1.1.8.orig.tar.gz 1892765 SHA256:4183409a450708a976eca5af561dbf4f0490141a08e86e4a1e649c7c1b094876
'http://archive.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.1.8-3.2ubuntu2.diff.gz' pam_1.1.8-3.2ubuntu2.diff.gz 198851 SHA256:5b999640be4f2ffd0e200e7785d04089375635d2d0f2033b7668462f6207a35f
```

### `dpkg` source package: `pcre3=2:8.39-2`

Binary Packages:

- `libpcre3:amd64=2:8.39-2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)
  If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris pcre3=2:8.39-2
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcre3/pcre3_8.39-2.dsc' pcre3_8.39-2.dsc 2133 SHA256:8c5ba4886410322adb13986748280e95fb9334bb5b86aeee6b4ba9295144eb12
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcre3/pcre3_8.39.orig.tar.bz2' pcre3_8.39.orig.tar.bz2 1560758 SHA256:b858099f82483031ee02092711689e7245586ada49e534a06e678b8ea9549e8b
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcre3/pcre3_8.39-2.debian.tar.gz' pcre3_8.39-2.debian.tar.gz 23765 SHA256:375c8c6c746553dd3c7364d53c4e85f68694c58763e4bc541821060cbb52eef6
```

### `dpkg` source package: `perl=5.24.1~rc4-1`

Binary Packages:

- `perl-base=5.24.1~rc4-1`

Licenses: (parsed from: `/usr/share/doc/perl-base/copyright`)

- `Artistic`
- `Artistic,`
- `Artistic-2`
- `BSD-3-clause`
- `BSD-3-clause-GENERIC`
- `BSD-3-clause-with-weird-numbering`
- `BSD-4-clause-POWERDOG`
- `BZIP`
- `CC0-1.0`
- `DONT-CHANGE-THE-GPL`
- `Expat`
- `GPL-1`
- `GPL-1+`
- `GPL-2`
- `GPL-2+`
- `GPL-3+-WITH-BISON-EXCEPTION`
- `HSIEH-BSD`
- `HSIEH-DERIVATIVE`
- `LGPL-2.1`
- `REGCOMP`
- `REGCOMP,`
- `RRA-KEEP-THIS-NOTICE`
- `S2P`
- `SDBM-PUBLIC-DOMAIN`
- `TEXT-TABS`
- `Unicode`
- `ZLIB`

Source:

```console
$ apt-get source -qq --print-uris perl=5.24.1~rc4-1
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.24.1~rc4-1.dsc' perl_5.24.1~rc4-1.dsc 2383 SHA256:716cf5d2615ffd278e884fc43ce1306a33bb6555b5a9556711331ecf8b59bb7d
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.24.1~rc4.orig.tar.xz' perl_5.24.1~rc4.orig.tar.xz 11553836 SHA256:6da6333809eb2b35b17ee3c25b7f0327da32fad7214b296b662ccd9883b8bc59
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.24.1~rc4-1.debian.tar.xz' perl_5.24.1~rc4-1.debian.tar.xz 163412 SHA256:4fce5c9bb6768dac245e9c8f5fabbacf78b3dda9b0552716ca3d6000b1b2106b
```

### `dpkg` source package: `pinentry=1.0.0-1`

Binary Packages:

- `pinentry-curses=1.0.0-1`

Licenses: (parsed from: `/usr/share/doc/pinentry-curses/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-3`
- `LGPL-3+`
- `X11`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!


### `dpkg` source package: `procps=2:3.3.12-1ubuntu2`

Binary Packages:

- `libprocps6:amd64=2:3.3.12-1ubuntu2`
- `procps=2:3.3.12-1ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libprocps6/copyright`, `/usr/share/doc/procps/copyright`)

- `GPL-2`
- `GPL-2.0+`
- `LGPL-2`
- `LGPL-2.0+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris procps=2:3.3.12-1ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/p/procps/procps_3.3.12-1ubuntu2.dsc' procps_3.3.12-1ubuntu2.dsc 2243 SHA256:c8e72f65fdcadb40b13f35ce322b820eb3fec082fef153387cae78a33d8f144b
'http://archive.ubuntu.com/ubuntu/pool/main/p/procps/procps_3.3.12.orig.tar.xz' procps_3.3.12.orig.tar.xz 840540 SHA256:042fcc93e1850aee4c193c51c03f369293fb64fe47e37b38852be6693d12a3af
'http://archive.ubuntu.com/ubuntu/pool/main/p/procps/procps_3.3.12-1ubuntu2.debian.tar.xz' procps_3.3.12-1ubuntu2.debian.tar.xz 30724 SHA256:1b40d1519e0dd9965aa3faed306dfdb44a113e39a14a404ba5fd28ff3d6e42b8
```

### `dpkg` source package: `readline=7.0-0ubuntu2`

Binary Packages:

- `libreadline7:amd64=7.0-0ubuntu2`
- `readline-common=7.0-0ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libreadline7/copyright`, `/usr/share/doc/readline-common/copyright`)

- `GFDL`
- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris readline=7.0-0ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/r/readline/readline_7.0-0ubuntu2.dsc' readline_7.0-0ubuntu2.dsc 2533 SHA256:80cf79ab8bd7a3847d505b6efc4c97d6f3e4dcc4247c54ecc2d8cec8b2e6d7c6
'http://archive.ubuntu.com/ubuntu/pool/main/r/readline/readline_7.0.orig.tar.gz' readline_7.0.orig.tar.gz 2910016 SHA256:750d437185286f40a369e1e4f4764eda932b9459b5ec9a731628393dd3d32334
'http://archive.ubuntu.com/ubuntu/pool/main/r/readline/readline_7.0-0ubuntu2.debian.tar.xz' readline_7.0-0ubuntu2.debian.tar.xz 28524 SHA256:61334a69abb593401d775386f7616df20e7aaf8c571e91d5158c71546123ffa7
```

### `dpkg` source package: `rtmpdump=2.4+20151223.gitfa8646d.1-1`

Binary Packages:

- `librtmp1:amd64=2.4+20151223.gitfa8646d.1-1`

Licenses: (parsed from: `/usr/share/doc/librtmp1/copyright`)

- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris rtmpdump=2.4+20151223.gitfa8646d.1-1
'http://archive.ubuntu.com/ubuntu/pool/main/r/rtmpdump/rtmpdump_2.4+20151223.gitfa8646d.1-1.dsc' rtmpdump_2.4+20151223.gitfa8646d.1-1.dsc 2315 SHA256:e56822b88625bf6a51f06652fc36fa2a1348b4325ac76541800cd078192aa3d2
'http://archive.ubuntu.com/ubuntu/pool/main/r/rtmpdump/rtmpdump_2.4+20151223.gitfa8646d.1.orig.tar.gz' rtmpdump_2.4+20151223.gitfa8646d.1.orig.tar.gz 142213 SHA256:5c032f5c8cc2937eb55a81a94effdfed3b0a0304b6376147b86f951e225e3ab5
'http://archive.ubuntu.com/ubuntu/pool/main/r/rtmpdump/rtmpdump_2.4+20151223.gitfa8646d.1-1.debian.tar.xz' rtmpdump_2.4+20151223.gitfa8646d.1-1.debian.tar.xz 8044 SHA256:675847f5cddb860256cbf2e7d5b85918aa53b59b0fd97a466b39a5c77a399537
```

### `dpkg` source package: `sed=4.3-3`

Binary Packages:

- `sed=4.3-3`

Licenses: (parsed from: `/usr/share/doc/sed/copyright`)

- `GPL-3`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!


### `dpkg` source package: `sensible-utils=0.0.9`

Binary Packages:

- `sensible-utils=0.0.9`

Licenses: (parsed from: `/usr/share/doc/sensible-utils/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris sensible-utils=0.0.9
'http://archive.ubuntu.com/ubuntu/pool/main/s/sensible-utils/sensible-utils_0.0.9.dsc' sensible-utils_0.0.9.dsc 1405 SHA256:390c29b31a09ab7f31f8b5fc0fd82e47c25f15b22b17c614fb87f12d3b091070
'http://archive.ubuntu.com/ubuntu/pool/main/s/sensible-utils/sensible-utils_0.0.9.tar.gz' sensible-utils_0.0.9.tar.gz 74331 SHA256:6fcb5cc0f7f1cf80421840cfa17b1b3fa5afaf3fe852dc984a789023af2f70c6
```

### `dpkg` source package: `shadow=1:4.2-3.2ubuntu1`

Binary Packages:

- `login=1:4.2-3.2ubuntu1`
- `passwd=1:4.2-3.2ubuntu1`

Licenses: (parsed from: `/usr/share/doc/login/copyright`, `/usr/share/doc/passwd/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris shadow=1:4.2-3.2ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/s/shadow/shadow_4.2-3.2ubuntu1.dsc' shadow_4.2-3.2ubuntu1.dsc 2432 SHA256:a5d12dae23f17fa0ab7360b7164f1069e2df885a6d5139aead3ffac706b1c5b1
'http://archive.ubuntu.com/ubuntu/pool/main/s/shadow/shadow_4.2.orig.tar.xz' shadow_4.2.orig.tar.xz 1088696 SHA256:c5bd72c4ecb438b99289e4630b22ea0626987a378d084910dbe59eceaa34be1d
'http://archive.ubuntu.com/ubuntu/pool/main/s/shadow/shadow_4.2-3.2ubuntu1.debian.tar.xz' shadow_4.2-3.2ubuntu1.debian.tar.xz 504272 SHA256:8cf6c74b2c41c436e98ca63e229002363a5f62b31f3c5698cfdee49361a7bdf5
```

### `dpkg` source package: `sqlite3=3.15.2-2`

Binary Packages:

- `libsqlite3-0:amd64=3.15.2-2`

Licenses: (parsed from: `/usr/share/doc/libsqlite3-0/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!


### `dpkg` source package: `systemd=232-8`

Binary Packages:

- `libsystemd0:amd64=232-8`
- `libudev1:amd64=232-8`

Licenses: (parsed from: `/usr/share/doc/libsystemd0/copyright`, `/usr/share/doc/libudev1/copyright`)

- `CC0`
- `Expat`
- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris systemd=232-8
'http://archive.ubuntu.com/ubuntu/pool/main/s/systemd/systemd_232-8.dsc' systemd_232-8.dsc 4653 SHA256:3ca60d621830e7df68aff42fcd7e09ad3eeca54ce15cade2f5190ad5d9208581
'http://archive.ubuntu.com/ubuntu/pool/main/s/systemd/systemd_232.orig.tar.gz' systemd_232.orig.tar.gz 4529048 SHA256:1172c7c7d5d72fbded53186e7599d5272231f04cc8b72f9a0fb2c5c20dfc4880
'http://archive.ubuntu.com/ubuntu/pool/main/s/systemd/systemd_232-8.debian.tar.xz' systemd_232-8.debian.tar.xz 131676 SHA256:5dcb0e19e7a33e15ad5cea4b9806c4705b78ebe87a0478fbdf7d85c20fc29bab
```

### `dpkg` source package: `sysvinit=2.88dsf-59.8git1`

Binary Packages:

- `sysvinit-utils=2.88dsf-59.8git1`

Licenses: (parsed from: `/usr/share/doc/sysvinit-utils/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris sysvinit=2.88dsf-59.8git1
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysvinit/sysvinit_2.88dsf-59.8git1.dsc' sysvinit_2.88dsf-59.8git1.dsc 2264 SHA256:51ee31d15f05db999da562c0c26ea43075938c4d40eea42f878361c990526767
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysvinit/sysvinit_2.88dsf.orig.tar.gz' sysvinit_2.88dsf.orig.tar.gz 125330 SHA256:b016f937958d2809a020d407e1287bdc09abf1d44efaa96530e2ea57f544f4e8
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysvinit/sysvinit_2.88dsf-59.8git1.debian.tar.xz' sysvinit_2.88dsf-59.8git1.debian.tar.xz 132992 SHA256:46fdc9f8212692e75c6a3ef76c5acd1eb0f8d55779f98f05b57bbe41b98c4c66
```

### `dpkg` source package: `tar=1.29b-1.1`

Binary Packages:

- `tar=1.29b-1.1`

Licenses: (parsed from: `/usr/share/doc/tar/copyright`)

- `GPL-2`
- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris tar=1.29b-1.1
'http://archive.ubuntu.com/ubuntu/pool/main/t/tar/tar_1.29b-1.1.dsc' tar_1.29b-1.1.dsc 2057 SHA256:9474ed422017e23e8208785c071b9f7765d73d704b9bb19da22699c6581d73ef
'http://archive.ubuntu.com/ubuntu/pool/main/t/tar/tar_1.29b.orig.tar.xz' tar_1.29b.orig.tar.xz 1822008 SHA256:6a59706ebee384a6cd2fb3ee1dbfbfc20c5c66c7efd7cedb28edc054fca8ba00
'http://archive.ubuntu.com/ubuntu/pool/main/t/tar/tar_1.29b-1.1.debian.tar.xz' tar_1.29b-1.1.debian.tar.xz 28484 SHA256:380f80af0e87446796f05ba384c5d130ea2ad5978b8cfdcf315503966333ebb9
```

### `dpkg` source package: `tzdata=2016j-2`

Binary Packages:

- `tzdata=2016j-2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)
  If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris tzdata=2016j-2
'http://archive.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2016j-2.dsc' tzdata_2016j-2.dsc 2005 SHA256:f3d5625674688b1bde68ba3e258102d69979a00a65ad3d0a78007668f19327a3
'http://archive.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2016j.orig.tar.gz' tzdata_2016j.orig.tar.gz 321185 SHA256:f5ee4e0f115f6c2faee1c4b16193a97338cbd1b503f2cea6c5a768c82ff39dc8
'http://archive.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2016j-2.debian.tar.xz' tzdata_2016j-2.debian.tar.xz 100588 SHA256:04b8920c2b2116806bc5b86c161299827e303f4018aac233c01d2503a94e4a53
```

### `dpkg` source package: `ubuntu-keyring=2016.10.27`

Binary Packages:

- `ubuntu-keyring=2016.10.27`

Licenses: (parsed from: `/usr/share/doc/ubuntu-keyring/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris ubuntu-keyring=2016.10.27
'http://archive.ubuntu.com/ubuntu/pool/main/u/ubuntu-keyring/ubuntu-keyring_2016.10.27.dsc' ubuntu-keyring_2016.10.27.dsc 1174 SHA256:21538f4cea9fb0f7faa13277778b4548f9cc359ceaa5fa3fed36d8a75f5530b4
'http://archive.ubuntu.com/ubuntu/pool/main/u/ubuntu-keyring/ubuntu-keyring_2016.10.27.tar.gz' ubuntu-keyring_2016.10.27.tar.gz 19182 SHA256:dc0b83433b28e5acedf39330bedec2cd102547570d1ae135497b15bd6ac85abe
```

### `dpkg` source package: `ustr=1.0.4-6`

Binary Packages:

- `libustr-1.0-1:amd64=1.0.4-6`

Licenses: (parsed from: `/usr/share/doc/libustr-1.0-1/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`
- `LGPL-2+`
- `LGPL-2.1`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris ustr=1.0.4-6
'http://archive.ubuntu.com/ubuntu/pool/main/u/ustr/ustr_1.0.4-6.dsc' ustr_1.0.4-6.dsc 2029 SHA256:87a854fc03dc059d5d4f135dfd36353c8c09f88a6eb216c6dcea8adadbe6ba59
'http://archive.ubuntu.com/ubuntu/pool/main/u/ustr/ustr_1.0.4.orig.tar.gz' ustr_1.0.4.orig.tar.gz 301345 SHA256:4d293b6b9d9fe51d58441f4b09b1f0005fcad8256ae8048587789bf5dbefb62e
'http://archive.ubuntu.com/ubuntu/pool/main/u/ustr/ustr_1.0.4-6.debian.tar.xz' ustr_1.0.4-6.debian.tar.xz 25608 SHA256:75aa6be2c70eba632ac63078e55ecb4b5a45e6624501a8ed6d81b9a2014d149e
```

### `dpkg` source package: `util-linux=2.29-1ubuntu2`

Binary Packages:

- `bsdutils=1:2.29-1ubuntu2`
- `libblkid1:amd64=2.29-1ubuntu2`
- `libfdisk1:amd64=2.29-1ubuntu2`
- `libmount1:amd64=2.29-1ubuntu2`
- `libsmartcols1:amd64=2.29-1ubuntu2`
- `libuuid1:amd64=2.29-1ubuntu2`
- `mount=2.29-1ubuntu2`
- `util-linux=2.29-1ubuntu2`

Licenses: (parsed from: `/usr/share/doc/bsdutils/copyright`, `/usr/share/doc/libblkid1/copyright`, `/usr/share/doc/libfdisk1/copyright`, `/usr/share/doc/libmount1/copyright`, `/usr/share/doc/libsmartcols1/copyright`, `/usr/share/doc/libuuid1/copyright`, `/usr/share/doc/mount/copyright`, `/usr/share/doc/util-linux/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `BSD-4-clause`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `LGPL`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`
- `MIT`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris util-linux=2.29-1ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.29-1ubuntu2.dsc' util-linux_2.29-1ubuntu2.dsc 3596 SHA256:b9b235f38f2d8de9ef173ef3424ef85345257beaea771585332d19f4593cf949
'http://archive.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.29.orig.tar.xz' util-linux_2.29.orig.tar.xz 4249020 SHA256:2c59ea67cc7b564104f60532f6e0a95fe17a91acb870ba8fd7e986f273abf9e7
'http://archive.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.29-1ubuntu2.debian.tar.xz' util-linux_2.29-1ubuntu2.debian.tar.xz 74316 SHA256:6fbd3bc9c911eebf3a37588a25431d04bf0fd4f59ae21e5aac442f9368676816
```

### `dpkg` source package: `wget=1.18-2ubuntu1`

Binary Packages:

- `wget=1.18-2ubuntu1`

Licenses: (parsed from: `/usr/share/doc/wget/copyright`)

- `GFDL-1.2`
- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris wget=1.18-2ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/w/wget/wget_1.18-2ubuntu1.dsc' wget_1.18-2ubuntu1.dsc 1927 SHA256:910ca159da97ce9e49203cd67885c899ffd4a045d0c03f91baeeb311b59898fb
'http://archive.ubuntu.com/ubuntu/pool/main/w/wget/wget_1.18.orig.tar.gz' wget_1.18.orig.tar.gz 3865525 SHA256:a00a65fab84cc46e24c53ce88c45604668a7a479276e037dc2f558e34717fb2d
'http://archive.ubuntu.com/ubuntu/pool/main/w/wget/wget_1.18-2ubuntu1.debian.tar.xz' wget_1.18-2ubuntu1.debian.tar.xz 22852 SHA256:9ff6d524f520fcd308cfbb971086f1f769ccb9d1d717a559a5337c5eca765542
```

### `dpkg` source package: `xz-utils=5.2.2-1.2`

Binary Packages:

- `liblzma5:amd64=5.2.2-1.2`

Licenses: (parsed from: `/usr/share/doc/liblzma5/copyright`)

- `Autoconf`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `LGPL-2`
- `LGPL-2.1`
- `LGPL-2.1+`
- `PD`
- `PD-debian`
- `config-h`
- `noderivs`
- `none`
- `permissive-fsf`
- `permissive-nowarranty`
- `probably-PD`

Source:

```console
$ apt-get source -qq --print-uris xz-utils=5.2.2-1.2
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.2.2-1.2.dsc' xz-utils_5.2.2-1.2.dsc 2550 SHA256:13c8d8d0c243af78dc89b6e2cd670c8d8a2522379e1fcd196957c95d988d5961
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.2.2.orig.tar.xz' xz-utils_5.2.2.orig.tar.xz 1016404 SHA256:f341b1906ebcdde291dd619399ae944600edc9193619dd0c0110a5f05bfcc89e
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.2.2.orig.tar.xz.asc' xz-utils_5.2.2.orig.tar.xz.asc 543 SHA256:2cc0575556e1331b3f468e6e7dca5969ce86efcc315d62672279b4e68b2e449f
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.2.2-1.2.debian.tar.xz' xz-utils_5.2.2-1.2.debian.tar.xz 108632 SHA256:231c08d5c2c4e5c8ef5d6d58cac91aaeb2e4fcddc35e1ed3c69d730a2375c948
```

### `dpkg` source package: `zlib=1:1.2.8.dfsg-2ubuntu5`

Binary Packages:

- `zlib1g:amd64=1:1.2.8.dfsg-2ubuntu5`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)
  If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!

