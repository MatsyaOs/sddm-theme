# Maintainer: MISTER NEGATIVE <misternegative21@gmail.com>

pkgname=matsya-sddm-theme-git
_pkgname=matsya-sddm-theme
pkgver=0.6
pkgrel=1
pkgdesc="Matysa SDDM Theme"
arch=('x86_64')
url="https://github.com/matsyaos/sddm-theme"
license=('GPLv3')
groups=('cutefish-git')
makedepends=('extra-cmake-modules' 'ninja' 'qt5-tools' 'git')
provides=("$_pkgname")
conflicts=("$_pkgname")
source=("git+$url.git")
sha512sums=('SKIP')

build() {
  cd sddm-theme

  cmake -DCMAKE_INSTALL_PREFIX=/usr .
  make
}

package() {
  cd sddm-theme
  make DESTDIR="$pkgdir" install
}
