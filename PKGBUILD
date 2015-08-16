# Maintainer: Anton Bazhenov <anton.bazhenov at gmail>
# Contributor: Michael Krauss <hippodriver@gmx.net>
# Contributor: Jacek Poplawski <jacekpoplawski@gmail.com>

pkgname=lgeneral
pkgver=1.2.6
pkgrel=1
pkgdesc="A turn-based strategy engine heavily inspired by Panzer General"
arch=('i686' 'x86_64')
url="http://lgames.sourceforge.net/index.php?project=LGeneral"
license=('GPL')
depends=('sdl_mixer')
install="${pkgname}.install"
source=("http://downloads.sourceforge.net/${pkgname}/${pkgname}-${pkgver}.tar.gz")
md5sums=('7710241685620ce109d7295fa1e9dfc5')

build() {
  cd "${srcdir}/${pkgname}-${pkgver}"
  ./configure --prefix=/usr
  make
}

package() {
  cd "${srcdir}/${pkgname}-${pkgver}"
  make DESTDIR="${pkgdir}" install
}
