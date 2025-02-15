# Maintainer: Bill Sideris <bill88t@bredos.org>

pkgname="bredos-zram-defaults"
pkgver=1.1
pkgrel=1
arch=('any')
pkgdesc="BredOS Zram configuration defaults"
url="https://bredos.org/"
license=('MIT')
depends=('zram-generator')
backup=("etc/sysctl.d/swappiness.conf"
        "etc/systemd/zram-generator.conf")
source=("swappiness.conf"
        "zram-generator.conf")
md5sums=('488dc23efd5bde003869a8c6a3b938a3'
         'a21e61e0a2da629fd23ea7d2dc1f3430')

package() {
    mkdir -p $pkgdir/etc/sysctl.d $pkgdir/etc/systemd
    install -m644 "$srcdir/swappiness.conf" "$pkgdir/etc/sysctl.d/swappiness.conf"
    install -m644 "$srcdir/zram-generator.conf" "$pkgdir/etc/systemd/zram-generator.conf"
}
