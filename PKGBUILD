pkgname=pngcrush
pkgver=1.7.85
pkgrel=1
pkgdesc="A tool for optimizing the compression of PNG files"
arch=('x86_64')
url="http://pmt.sourceforge.net/$pkgname"
license=('custom')
depends=('libpng')
source=("http://downloads.sourceforge.net/pmt/$pkgname-$pkgver-nolib.tar.xz"
        LICENSE)
sha512sums=('8022b23ddcbafac95c11d55affdfe64d'
         'e6446a786d939c98fcada57f9ae6de1f')

build() {
    cd "$srcdir"/$pkgname-$pkgver-nolib
    CFLAGS+=" -DPNGCRUSH_COUNT_COLORS" make
    }

package() {
    install -Dm755 "$srcdir"/$pkgname-$pkgver-nolib/$pkgname \
        "$pkgdir"/usr/bin/$pkgname
    install -Dm644 $srcdir/LICENSE \
        "$pkgdir"/usr/share/licenses/$pkgname/LICENSE
    }
