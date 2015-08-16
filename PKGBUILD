# Contributor: Lucas Hermann Negri <kkndrox@gmail.com>
pkgname=luabitop
pkgver=1.0.1
pkgrel=1
pkgdesc="Lua BitOp is a C extension module for Lua 5.1 which adds bitwise operations on numbers."
arch=(i686 x86_64)
url="http://bitop.luajit.org/index.html"
makedepends=('gcc')
depends=('lua>=5.1')
source=(http://bitop.luajit.org/download/LuaBitOp-$pkgver.tar.gz)
md5sums=('39984456940aea838e0f500bececbd73')
license=('MIT')

build() {
	cd $startdir/src/LuaBitOp-$pkgver
	make || return 1
	mkdir -p $startdir/pkg/usr/lib/lua/5.1
	cp $startdir/src/LuaBitOp-$pkgver/bit.so $startdir/pkg/usr/lib/lua/5.1
}
