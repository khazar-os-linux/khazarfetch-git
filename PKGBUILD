# Maintainer: OpenSourceGuy
pkgname=khazarfetch-git
pkgver=r23.da56901
pkgrel=1
pkgdesc="A system information fetch tool"
arch=('any')
url="https://github.com/khazar-os-linux/khazarfetch"
license=('GPL')
depends=()
source=("git+$url.git")
md5sums=('SKIP')

pkgver() {
  cd "$srcdir/$pkgname"
  local count hash
  count=$(git rev-list --count HEAD)
  hash=$(git rev-parse --short HEAD)
  echo "r${count}.${hash}"
}

build() {
  cd "$srcdir/$pkgname"
  make
}

package() {
  cd "$srcdir/$pkgname"
  make DESTDIR="$pkgdir/" install
}

