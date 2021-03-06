# `php:7.1.1-fpm-alpine`

## Docker Metadata

- Image ID: `sha256:8a87fcbea0c9cec03c2a31a341db552126ad57f37fc79abdd098f7f337885e39`
- Created: `2017-01-24T18:41:58.875957158Z`
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
  - `GPG_KEYS=A917B1ECDA84AEC2B568FED6F50ABC807BD5DCD0 528995BFEDFBA7191D46839EF9BA0ADA31CBD89E`
  - `PHP_VERSION=7.1.1`
  - `PHP_URL=https://secure.php.net/get/php-7.1.1.tar.xz/from/this/mirror`
  - `PHP_ASC_URL=https://secure.php.net/get/php-7.1.1.tar.xz.asc/from/this/mirror`
  - `PHP_SHA256=b3565b0c1441064eba204821608df1ec7367abff881286898d900c2c2a5ffe70`
  - `PHP_MD5=65eef256f6e7104a05361939f5e23ada`
