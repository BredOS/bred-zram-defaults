# Maintainer: Bill Sideris <bill88t@bredos.org>

pkgname="bred-zram-defaults"
pkgver=1.0
pkgrel=1
arch=('any')
pkgdesc="BredOS Zram configuration defaults"
url="https://bredos.org/"
license=('MIT')
depends=('zram-generator')
source=(
    "swappiness.conf"
    "zram-generator.conf"
    )
md5sums=('SKIP' 'SKIP')

package() {
    mkdir -p $pkgdir/etc/sysctl.d $pkgdir/etc/systemd
    install -m644 "$srcdir/swappiness.conf" "$pkgdir/etc/sysctl.d/swappiness.conf"
    install -m644 "$srcdir/zram-generator.conf" "$pkgdir/etc/systemd/zram-generator.conf"
}
