# Maintainer: hauptmech # Contributor: figo.zhang, chubtuff, lubosz
#
# Matlab bindings are not built by default to reduce dependencies.

pkgname=gl2ps
pkgver=1.3.8
pkgrel=2
pkgdesc="an OpenGL to PostScript printing library"
arch=('any')
url='http://geuz.org/gl2ps/'
license=('BSD')
makedepends=('cmake' 'texlive-core' )
optdepends=()
conflicts=()
source=("http://geuz.org/gl2ps/src/gl2ps-${pkgver}.tgz")

build() {
  cd "${srcdir}/gl2ps-$pkgver-source"

  mkdir build
  cd build

  cmake .. \
    -DCMAKE_BUILD_TYPE=Release \
    -DCMAKE_INSTALL_PREFIX=/usr \
    -DCMAKE_EXE_LINKER_FLAGS=-lm
  make

}

package() {
  cd "${srcdir}/gl2ps-$pkgver-source/build"

  make DESTDIR="$pkgdir/" install

}

md5sums=('05ae306fdad00a24ffcabf47d8ae363e')
sha256sums=('2fe58dd95df06688a8c188e70b1803093ebf0797954901f4a36a403dbc301ee5')
sha512sums=('76e90d675764196d249d87c6041088736a8b41d9b93620c6171a40362a259d50e34d5efc06e4ea17e6c147bc26b6a3a7356d95ea5e204193ef631fb48e0c0a4e')
