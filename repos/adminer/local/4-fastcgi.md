# `adminer:4.2.5-fastcgi`

## Docker Metadata

- Image ID: `sha256:562ed9123fb18d8a0499b3e797d52627855565cda13cfdee06d59d7c1dfe759d`
- Created: `2017-01-30T17:35:00.854102437Z`
- Arch: `linux`/`amd64`
- Entrypoint: `["docker-php-entrypoint"]`
- Command: `["php-fpm"]`
- Environment:
  - `PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`
  - `PHPIZE_DEPS=autoconf 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c`
  - `PHP_INI_DIR=/usr/local/etc/php`
  - `PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data`
  - `PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2`
  - `PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2`
  - `PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie`
  - `GPG_KEYS=1A4E8B7277C42E53DBA9C7B9BCAA30EA9C0D5763 6E4F6AB321FDC07F2C332E3AC2BF0BC433CFC8B3`
  - `PHP_VERSION=7.0.15`
  - `PHP_URL=https://secure.php.net/get/php-7.0.15.tar.xz/from/this/mirror`
  - `PHP_ASC_URL=https://secure.php.net/get/php-7.0.15.tar.xz.asc/from/this/mirror`
  - `PHP_SHA256=300364d57fc4a6176ff7d52d390ee870ab6e30df121026649f8e7e0b9657fe93`
  - `PHP_MD5=dca23412f3e3b3987e582091b751925d`
  - `ADMINER_VERSION=4.2.5`
  - `ADMINER_DOWNLOAD_SHA256=a8d9f5df8a604e75e87670bc1d797bb49cc1047f722a8630bda514fdc407f84f`
