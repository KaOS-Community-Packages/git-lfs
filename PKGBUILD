license=('MIT')
arch=('x86_64')
pkgname=git-lfs
pkgver=2.7.1
pkgrel=0
pkgdesc="Git extension for versioning large files"
depends=()
makedepends=('go')
url="https://git-lfs.github.com/"
source=("${pkgname}-${pkgver}.tar.gz::https://github.com/git-lfs/git-lfs/archive/v${pkgver}.tar.gz")
md5sums=('c0a1968b70e92193017496ac028b8f82')

build() {
  cd ${pkgname}-${pkgver}
  make
}

package() {
  mkdir -p ${pkgdir}/usr/bin
  cp ${srcdir}/${pkgname}-${pkgver}/bin/git-lfs ${pkgdir}/usr/bin
}
