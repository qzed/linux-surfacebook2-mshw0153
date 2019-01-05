pkgname="surfacebook2-shps"
pkgver="0.1.0"
pkgrel=1
pkgdesc="Experimental driver for surface hot-plug service"
license=('GPL v2')
arch=('x86_64' 'i686')
depends=('dkms')

source=(
    "src::git+https://github.com/qzed/linux-surfacebook2-mshw0153.git"
)

sha256sums=('SKIP')

package() {
    cd "${srcdir}/src"

    install -d "${pkgdir}/usr/src/sb2_shps-${pkgver}/"
    cp "${srcdir}/src/Makefile" "${pkgdir}/usr/src/sb2_shps-${pkgver}/"
    cp "${srcdir}/src/dkms.conf" "${pkgdir}/usr/src/sb2_shps-${pkgver}/"
    cp "${srcdir}/src/sb2_shps.c" "${pkgdir}/usr/src/sb2_shps-${pkgver}/"

    install -Dm644 "${srcdir}/src/sb2_shps.conf" "${pkgdir}/usr/lib/depmod.d/sb2_shps.conf"
}
