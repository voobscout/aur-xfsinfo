# Maintainer: Voobscout <voobscout+aur@gmail.com>
pkgname=xorg-xfs-xfsinfo
pkgver=1.0.5
pkgrel=1
pkgdesc="X Font Server - information"
arch=('i686' 'x86_64')
license=('GPL2')
makedepends=('git' 'pkg-config' 'autoconf' 'automake' 'gettext' 'xproto' 'xtrans' 'wget')
depends=('libfs')
url="http://xorg.freedesktop.org/archive/individual/app"
provides=('xorg-xfs-xfsinfo')
optdepends=('xorg-xfs' 'xorg-xfstt')
source=("http://xorg.freedesktop.org/archive/individual/app/xfsinfo-$pkgver.tar.gz")
sha256sums=('56a0492ed2cde272dc8f4cff4ba0970ccb900e51c10bb8ec62747483d095fd69')
options=(!strip)

build() {
  cd ${srcdir}/xfsinfo-${pkgver}
  msg "Configuring xfsinfo..."
  ./configure --prefix=/usr
  msg "Compiling xfsinfo... "
  make
}

package() {
  msg "Installing xfsinfo"
  cd ${srcdir}/xfsinfo-${pkgver}
  make DESTDIR=${pkgdir} install
}
# vim:set ts=2 sw=2 et:
