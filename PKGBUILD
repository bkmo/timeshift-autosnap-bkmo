# Maintainer: gobonja <gobonja@gmail.com>

pkgname=timeshift-autosnap
pkgver=0.6
pkgrel=1
pkgdesc="Timeshift auto-snapshot script which runs before package upgrade using Pacman hook."
arch=("any")
url="https://gitlab.com/gobonja/timeshift-autosnap"
license=('MIT')
depends=('timeshift')
optdepends=('grub-btrfs')
source=("${pkgname}-${pkgver}.tar.gz::${url}/-/archive/${pkgver}/${pkgname}-${pkgver}.tar.gz")
backup=('etc/timeshift-autosnap.conf')
md5sums=('6bf845f3c8e44107c78920368dec6524')

package() {
    cd ${srcdir}/${pkgname}-${pkgver}
    install -Dm644 00-timeshift-autosnap.hook ${pkgdir}/usr/share/libalpm/hooks/00-timeshift-autosnap.hook
    install -Dm644 timeshift-autosnap.conf ${pkgdir}/etc/timeshift-autosnap.conf
    install -Dm755 timeshift-autosnap ${pkgdir}/usr/bin/timeshift-autosnap
    install -Dm644 LICENSE ${pkgdir}/usr/share/licenses/${pkgname}/LICENSE
}
 
