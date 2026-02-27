# Maintainer: Bill Sideris <bill88t@bredos.org>

pkgname=smmu-evtq-fix
pkgver=1.0.0
pkgrel=1
pkgdesc="Disable SMMU event queue to mitigate CIX Sky1 firmware bug"
arch=('aarch64')
url="https://github.com/ErcinDedeoglu/orangepi-6plus-cix-sky1-smmu-fix"
license=('MIT')

depends=('bash' 'systemd' 'devmem')

source=(
  "smmu-evtq-fix.sh"
  "smmu-evtq-fix.service"
  "LICENSE"
)
sha256sums=('SKIP' 'SKIP' 'SKIP')

package() {
  install -d "$pkgdir/usr/bin" \
           "$pkgdir/usr/lib/systemd/system" \
           "$pkgdir/usr/share/doc/$pkgname" \
           "$pkgdir/usr/share/licenses/$pkgname"

  install -m755 "smmu-evtq-fix.sh" "$pkgdir/usr/bin/smmu-evtq-fix"

  install -m644 "smmu-evtq-fix.service" "$pkgdir/usr/lib/systemd/system/smmu-evtq-fix.service"

  install -m644 "LICENSE" "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
