# Maintainer: Gut Andrey <u at airmail.cc>
_pkgname=pokoy
pkgname=${_pkgname}-git
pkgver=0.2.1
pkgrel=1
pkgdesc="Lightweight daemon that helps prevent RSI and other computer related stress"
arch=("i686" "x86_64")
url="https://github.com/ttygde/${_pkgname}"
license=("GPL2")
depends=("libxcb" "xcb-util-wm" "xcb-util-keysyms")
makedepends=("git")
provides=("${_pkgname}")
conflicts=("${_pkgname}")
source=("git://github.com/ttygde/${_pkgname}.git")
sha256sum='SKIP'

build() {
	cd "$srcdir/$_pkgname"
	make PREFIX=/usr
}

package() {
  cd "$srcdir/${_pkgname}"
  make PREFIX="/usr" DESTDIR="$pkgdir" install
}
md5sums=('SKIP')
