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
sha512sums=('7b959fc6a8839fb0dab6471b13e866e11d5fefa072d6b135c7f621bd4b475765c2e8d0b471f074b6df7d6ccd8b5c33938e1143fb2e013986c4e8e5fada68c8ca'
            'f18613b9da9b4f31a317411e726def5122246087ff57887fba6b46f0a7a7fae7109388ecb2ce049bbe992cc6ef0a3fbbe0f5c5bc816705efd7583836cbd4e69d')

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
