pkgname=pngcrush
pkgver=1.8.11
pkgrel=1
pkgdesc="Tool for optimizing the compression of PNG files"
url="http://pmt.sourceforge.net/pngcrush"
arch=('x86_64')
license=('custom')
depends=('libpng' 'zlib' 'glibc')
source=("pngcrush.tar.gz::https://github.com/glennrp/pmt/archive/v1.8.11.tar.gz")
md5sums=('60f5c5780574dde8b924936d55426a8b')

build() {
    cd "${srcdir}/pmt-1.8.11"
    make -f Makefile-nolib
}

package() {
    cd "${srcdir}/pmt-1.8.11"
    install -Dm755 "${srcdir}/pmt-1.8.11/pngcrush" "${pkgdir}/usr/bin/pngcrush"
    install -Dm644 "${srcdir}/pmt-1.8.11/LICENSE" "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}
