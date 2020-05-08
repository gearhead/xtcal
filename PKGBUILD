pkgname=xtcal
pkgver=0.r6.8f238eb
pkgrel=1
pkgdesc="xt touchscreen calibration widget and application"
arch=('i686' 'x86_64' 'armv6h' 'armv7h')
url="https://github.com/kurtjacobson/xtcal"
license=('custom')
makedepends=('git')
provides=('xtcal')
source=("$pkgname::git+https://github.com/kurtjacobson/xtcal")
md5sums=('SKIP')

pkgver() {
  cd "$pkgname"
  printf "0.r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

build() {
  cd "${srcdir}"/"$pkgname"
  make -j4
}

package() {
  cd "$srcdir/$pkgname"
  install -Dm644 $pkgname "$pkgdir/usr/local/bin/$pkgname"
}
