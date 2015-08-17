# Maintainer: Antonio Rojas <nqn1976@gmail.com>
# Contributor: Ronald van Haren <ronald.archlinux.org>
# Contributor: Daniel J Griffiths <ghost1227@archlinux.us>

pkgname=speedcrunch
pkgver=0.11
pkgrel=1
pkgdesc="Simple but powerful calculator using Qt"
arch=('i686' 'x86_64')
url="http://speedcrunch.org/"
license=('GPL2')
depends=('qt4')
makedepends=('cmake')
source=("https://github.com/speedcrunch/SpeedCrunch/archive/$pkgver.tar.gz")
md5sums=('0d4458d98a3630cc121ca04d5a36e38c')

build() {
	cd SpeedCrunch-$pkgver/src
	cmake . -DCMAKE_INSTALL_PREFIX=/usr -DQT_QMAKE_EXECUTABLE=qmake-qt4
	make
}

package() {
	cd SpeedCrunch-$pkgver/src
	make DESTDIR="$pkgdir" install
}
