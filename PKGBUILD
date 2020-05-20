# Maintainer: TildeHacker <contact@tildehacker.com>
pkgname=ideapad-cm
pkgver=0.1.0
pkgrel=1
epoch=
pkgdesc="A script to enable/disable battery conservation mode in Lenovo Ideapad laptops."
arch=('any')
url="https://github.com/tildehacker/ideapad-conservation-mode"
license=('GPL3')
groups=()
depends=()
makedepends=()
checkdepends=()
optdepends=()
provides=()
conflicts=()
replaces=()
backup=()
options=()
install=
changelog=
source=("$pkgname")
noextract=()
md5sums=('80d066fe75d54bc51756610350347259')
validpgpkeys=()

prepare() {
	cd "$pkgname-$pkgver"
	patch -p1 -i "$srcdir/$pkgname-$pkgver.patch"
}

build() {
	cd "$pkgname-$pkgver"
	./configure --prefix=/usr
	make
}

check() {
	cd "$pkgname-$pkgver"
	make -k check
}

package() {
	cd "$pkgname-$pkgver"
	make DESTDIR="$pkgdir/" install
}
