pkgname=libkeybinder3
pkgver=0.3.2
pkgrel=2
pkgdesc="A library for registering global keyboard shortcuts"
arch=('x86_64')
url="https://github.com/engla/keybinder/tree/keybinder-3.0"
license=('MIT')
depends=('gtk3')
makedepends=('gobject-introspection')
source=(https://github.com/kupferlauncher/keybinder/releases/download/keybinder-3.0-v$pkgver/keybinder-3.0-$pkgver.tar.gz)
sha1sums=('d23c12440b54cb0f40e7e876c22001dc7b5714b0')

build() {
  cd keybinder-3.0-${pkgver}
  ./configure --prefix=/usr
  make
}

package() {
  cd keybinder-3.0-${pkgver}
  make DESTDIR="$pkgdir" install
  install -Dm644 COPYING "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
