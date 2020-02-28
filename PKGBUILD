# Maintainer: Husam Bilal <me@husam.dev>

pkgname=clipman
pkgver=1.4.0
pkgrel=1
pkgdesc="A simple clipboard manager for Wayland"
url="https://github.com/yory8/clipman"
depends=("wl-clipboard>=2.0")
makedepends=("go")
provides=("clipman")
license=("GPL3")
arch=("x86_64" "i686")
md5sums=("140c72f92cd329d177fcbbd751253e59")
source=("https://github.com/yory8/${pkgname}/archive/v${pkgver}.tar.gz")

build() {
  cd $pkgname-$pkgver
  go build .
}

package() {
  cd $pkgname-$pkgver
  install -Dm755 $pkgname $pkgdir/usr/bin/$pkgname
  install -Dm644 docs/$pkgname.1 $pkgdir/usr/share/man/man1/$pkgname.1
  gzip $pkgdir/usr/share/man/man1/$pkgname.1
}
