# Contributor: Kyle Keen <keenerd@gmail.com>
pkgname=rogue
pkgver=5.4.4
pkgrel=1
pkgdesc="The original dungeon crawl game."
arch=('i686' 'x86_64')
url="http://rogue.rogueforge.net/rogue-5-4/"
license=('custom')
depends=('ncurses')
makedepends=()
#source=(http://rogue.rogueforge.net/files/rogue5.4/$pkgname$pkgver-src.tar.gz)
source=(http://www.sourcefiles.org/Games/Role_Play/$pkgname$pkgver-src.tar.gz)
md5sums=('033288f46444b06814c81ea69d96e075')

build() {
  cd "$srcdir"/$pkgname$pkgver
  ./configure
  make
  install -Dm755 rogue "$pkgdir"/usr/bin/rogue
  install -Dm644 rogue.6 "$pkgdir"/usr/share/man/man6/rogue.6
  gzip "$pkgdir"/usr/share/man/man6/rogue.6
  install -Dm644 LICENSE.TXT "$pkgdir"/usr/share/licenses/$pkgname/LICENSE.TXT
}

