# Maintainer: Anton Jongsma <anton@felrood.nl>
pkgname=ccbuild
pkgver=2.0.6
pkgrel=1
pkgdesc="Source scanning build utility for C++"
arch=('i686' 'x86_64')
url="http://www.logfish.net/pr/ccbuild/downloads/"
license=('GPL')
depends=('libbobcat' 'gnutls')
makedepends=('boost')
source=("http://www.logfish.net/pr/ccbuild/downloads/ccbuild-${pkgver}.tar.gz")

build() {
  #patch < configure.in.patch
  cd ${srcdir}/${pkgname}-${pkgver}
  ./configure --prefix=/usr
  make
}

package() {
	cd "${srcdir}/${pkgname}-${pkgver}"
	make DESTDIR="${pkgdir}" install
}

md5sums=('1b0ada1151643ff2779822825003d839')
