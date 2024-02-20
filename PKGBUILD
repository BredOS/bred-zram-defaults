# Maintainer: Bill Sideris <bill88t@bredos.org>

pkgname="bredos-zram-defaults"
pkgver=1.0
pkgrel=2
arch=('any')
pkgdesc="BredOS Zram configuration defaults"
url="https://bredos.org/"
license=('MIT')
depends=('zram-generator')
backup=("etc/sysctl.d/swappiness.conf"
        "etc/systemd/zram-generator.conf")
source=("swappiness.conf"
        "zram-generator.conf")
md5sums=('0d4ccddbc957fd80629588cc32740be9'
         '55a8dce3eb86e8342063589ceba0cc20')

package() {
    mkdir -p $pkgdir/etc/sysctl.d $pkgdir/etc/systemd
    install -m644 "$srcdir/swappiness.conf" "$pkgdir/etc/sysctl.d/swappiness.conf"
    install -m644 "$srcdir/zram-generator.conf" "$pkgdir/etc/systemd/zram-generator.conf"
}
