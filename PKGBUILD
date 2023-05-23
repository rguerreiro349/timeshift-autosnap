#
# Contribuidor: {{ nome_do_autor(); }}
#

pkgname=timeshift-autosnap
pkgver=0.9
pkgrel=1
pkgdesc="Script de instantâneo automático Timeshift que é um procedimento antes da atualização do plug usando a chamada Pacman."
arch=("any")
url="http://localhost/timeshift-autosnap"
license=('cIO')
depends=('timeshift')
optdepends=('grub-btrfs')
source=("timeshift-autosnap.tar.gz")
backup=('etc/timeshift-autosnap.conf')
md5sums=('SKIP')


package()
{
    cd ${srcdir}/timeshift-autosnap

    install -Dm644 00-timeshift-autosnap.hook ${pkgdir}/usr/share/libalpm/hooks/00-timeshift-autosnap.hook
    install -Dm644 timeshift-autosnap.conf ${pkgdir}/etc/timeshift-autosnap.conf
    install -Dm755 timeshift-autosnap ${pkgdir}/usr/bin/timeshift-autosnap
    install -Dm644 LICENSE ${pkgdir}/usr/share/licenses/${pkgname}/LICENSE
}
 
