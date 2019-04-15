license=('GPL-2.0+')
arch=('x86_64')
pkgname=charmtimetracker
pkgver=1.12.0
pkgrel=0
pkgver_full=${pkgver}.${pkgrel}
pkgdesc="Charm is a program for OS X, Linux and Windows that helps to keep track of time"
depends=('qt5-base' 'qtkeychain')
makedepends=('qt5-tools' 'cmake')
url="https://github.com/KDAB/Charm"
source=("${pkgname}-${pkgver}.tar.gz::https://github.com/KDAB/Charm/archive/${pkgver}.tar.gz")
md5sums=('f0626708256dbb9fba771932f8d1c80f')

build() {
  mkdir -p build
  cd build

  cmake ../Charm-${pkgver} \
    -DCMAKE_BUILD_TYPE=Release \
    -DCMAKE_INSTALL_PREFIX=/usr \
    -DCharm_VERSION=${pkgver}
  make
}

package() {
  cd build

  make DESTDIR=${pkgdir} install
}
